# Research Notes — AI Gym Form Feedback

## 1. Problem và an toàn tập luyện

| Nguồn | Claim được sử dụng | Ý nghĩa cho bài toán | Giới hạn |
|---|---|---|---|
| NIAMS — Sports Injuries: https://www.niams.nih.gov/health-topics/sports-injuries | Không sử dụng đúng kỹ thuật tập là một yếu tố có thể làm tăng nguy cơ chấn thương thể thao | Hỗ trợ relevance của problem | Không chứng minh app AI sẽ giảm chấn thương |
| PubMed — Technique and safety aspects of resistance exercises: https://pubmed.ncbi.nlm.nih.gov/20048516/ | Một số vị trí cơ thể trong resistance exercise có thể đặt cấu trúc giải phẫu vào nguy cơ; hiểu chuyển động giúp tránh rủi ro | Form/range of motion cần được xác định có cơ sở | Review không phải specification cho một app squat cụ thể |
| Integrative review về injuries trong fitness centers: https://pmc.ncbi.nlm.nih.gov/articles/PMC9565175/ | Injury có nhiều nguyên nhân, gồm kỹ thuật không phù hợp, tải nặng, overuse và phục hồi không đủ | App chỉ giải một phần nhỏ của risk | Không được quy mọi injury cho form |

## 2. Công nghệ pose estimation có sẵn

| Giải pháp | Nguồn | Giải quyết bước nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học |
|---|---|---|---|---|---|
| MediaPipe Pose Landmarker | https://developers.google.com/edge/mediapipe/solutions/vision/pose_landmarker | Trích xuất landmark cơ thể từ ảnh/video | Có thể chạy image/video/live stream; cung cấp landmark/confidence | Landmark không tự động đồng nghĩa với form đúng/sai | Dùng model có sẵn để tạo MVP trước khi tự train toàn bộ |
| MoveNet | https://www.tensorflow.org/hub/tutorials/movenet | Pose detection nhanh cho ứng dụng edge | Có hướng dẫn realtime và keypoint score | Vẫn cần rep logic, error labels và evaluation | So sánh với MediaPipe trên thiết bị mục tiêu |
| Google ML Kit pose classification pattern | https://developers.google.com/ml-kit/vision/pose-detection/classifying-poses | Pose classification và rep counting từ landmark | Pattern đơn giản cho MVP | k-NN/rule có thể kém generalization | Baseline rule/classifier trước model phức tạp |

## 3. Hệ thống nghiên cứu tương tự

| Nghiên cứu | Nguồn | Điều chứng minh | Cảnh báo / khoảng trống | Bài học |
|---|---|---|---|---|
| Pose Tutor, CVPR Workshops 2022 | https://openaccess.thecvf.com/content/CVPR2022W/CVSports/html/Dittakavi_Pose_Tutor_An_Explainable_System_for_Pose_Correction_in_the_CVPRW_2022_paper.html | Có thể xây hệ thống nhận diện và giải thích joint gây lỗi cho một số loại pose | Dataset/exercise khác gym squat thực tế | Feedback nên giải thích joint/lỗi thay vì label chung chung |
| ExerciseCheck, ICCV Workshops 2019 | https://openaccess.thecvf.com/content_ICCVW_2019/html/ACVR/Gu_Home-Based_Physical_Therapy_with_an_Interactive_Computer_Vision_System_ICCVW_2019_paper.html | Computer vision có thể hỗ trợ đánh giá exercise và feedback | Nghiên cứu ghi nhận khoảng cách hiệu năng giữa RGB deep models và RGB-D trong case phức tạp | Không overclaim single-RGB; cần controlled scope và abstention |
| M3GYM, CVPR 2025 | https://openaccess.thecvf.com/content/CVPR2025/html/Xu_M3GYM_A_Large-Scale_Multimodal_Multi-view_Multi-person_Pose_Dataset_for_Fitness_CVPR_2025_paper.html | Dữ liệu gym thực tế cần multi-view/multimodal và rất lớn để phản ánh môi trường phức tạp | MVP nhóm không thể bao phủ ngay real-world gym variability | Bắt đầu một người/một exercise/một góc, rồi mở rộng có evidence |

## 4. Research takeaway

Hướng phù hợp không phải là một Agent “huấn luyện viên toàn năng”. Kiến trúc hợp lý cho MVP là:

```text
Camera setup rule
→ Pose Landmarker/MoveNet
→ Rep & phase detection
→ Error rule/classifier trong scope
→ Confidence/visibility gate
→ Cue cố định do HLV duyệt
→ User thử lại
```

### Quyết định kỹ thuật sơ bộ

1. Bắt đầu bằng pretrained pose model để giảm nhu cầu dataset landmark từ đầu.
2. Dùng rule hoặc classifier nhỏ cho một số lỗi squat có ground truth rõ.
3. Tách pose failure khỏi “form đúng”; không coi model không thấy lỗi là động tác đúng.
4. Chia dữ liệu theo người ở train/test để tránh leakage.
5. Báo cáo per-class precision/recall và false-negative, không chỉ accuracy tổng.
6. Chỉ cân nhắc self-trained end-to-end model khi baseline trên landmark không đạt và nhóm có dữ liệu đủ đa dạng.
7. Không dùng LLM sinh cue tự do trong MVP; cue phải được HLV duyệt.
