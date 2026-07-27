# 02 — Group Problem Statement

## 1. Nhật ký hội tụ

Danh sách candidate được tổng hợp theo bốn vai trò của nhóm và problem scan cá nhân. Nhóm không chọn “làm app AI” ngay từ đầu mà so sánh các bottleneck cụ thể trong workflow của người tập.

### Candidate inventory

| # | Nguồn vai trò | Candidate problem | Actor | Bottleneck |
|---:|---|---|---|---|
| 1 | Product | Người mới không biết tự đánh giá form squat khi tập một mình | Người mới tập | Không có feedback kịp thời |
| 2 | Product | Người dùng không biết feedback AI đáng tin tới đâu | Người mới tập | Thiếu confidence/boundary rõ |
| 3 | Product | App quá rộng nếu hỗ trợ mọi bài tập ngay | Product team | Scope và evaluation bùng nổ |
| 4 | App Experience | Người dùng đặt camera sai vị trí | Người mới tập | Setup không được kiểm tra |
| 5 | App Experience | Feedback chữ khó hiểu trong lúc tập | Người mới tập | Cue không trực quan |
| 6 | App Experience | Overlay/feedback chậm làm gián đoạn set | Người tập | Latency và UX |
| 7 | AI & Data | Pose estimation sai khi thiếu sáng hoặc che khuất | Người dùng, ML owner | Keypoint quality |
| 8 | AI & Data | Dataset chưa đủ đa dạng hình thể/góc quay | ML owner | Generalization yếu |
| 9 | AI & Data | Chưa có ground truth do HLV gán nhãn | Evaluator | Không biết model đúng đến đâu |
| 10 | Platform | Upload video gây lo ngại privacy và chi phí | Người dùng, platform owner | Data governance |
| 11 | Platform | Real-time inference có thể chậm trên thiết bị yếu | Người dùng | Hiệu năng/deployment |
| 12 | Platform | Lưu lịch sử tập có thể chứa video nhạy cảm | Người dùng | Retention và access control |

### Cluster

| Cluster | Candidates | Pattern chung |
|---|---|---|
| Core user feedback | 1, 2, 5, 6 | Người mới cần feedback kịp thời, dễ hiểu và đáng tin |
| Capture quality | 4, 7, 11 | Input camera và latency quyết định chất lượng output |
| Data & evaluation | 8, 9 | Thiếu dữ liệu và ground truth làm model khó kiểm chứng |
| Scope, privacy & safety | 3, 10, 12 | Sản phẩm dễ vượt phạm vi hoặc tạo rủi ro mới |

### Shortlist

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|---|---|---|
| AI feedback cho bodyweight squat | User pain rõ; AI quan sát chuyển động; pilot một bài tập được | Chưa có user interview và benchmark HLV |
| Camera setup quality gate | Điều kiện bắt buộc cho mọi phân tích | Có thể chỉ là UX phụ, không phải problem chính |
| Trainer-labeled evaluation workflow | Cần để biết model có đủ tin cậy | Không trực tiếp tạo giá trị cho người dùng nếu đứng riêng |

### Score 1–5

| Candidate | Actor rõ | Workflow rõ | Evidence | Impact đo được | Làm trong lab | So sánh R/W/A | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| AI feedback cho bodyweight squat | 5 | 5 | 3 | 5 | 4 | 5 | 5 | **32** |
| Camera setup quality gate | 5 | 5 | 3 | 4 | 5 | 4 | 5 | 31 |
| Trainer-labeled evaluation | 4 | 5 | 2 | 5 | 4 | 4 | 4 | 28 |

## Candidate được chọn

**Ứng dụng AI hỗ trợ người mới kiểm tra form bodyweight squat bằng camera.**

### Vì sao chọn

1. Actor cụ thể: người trưởng thành mới tập và thường tập một mình.
2. Workflow hiện tại có thể quan sát và vẽ được.
3. Bottleneck nằm ở việc không có feedback form kịp thời, không phải ở việc “chưa có chatbot”.
4. AI pose estimation có vai trò rõ trong việc quan sát chuyển động.
5. Có thể thu nhỏ thành một bài tập, một người, điều kiện quay kiểm soát.
6. Một thành viên đã từng làm prototype tương tự, giúp nhóm có kinh nghiệm kỹ thuật ban đầu.

### Vì sao không chọn candidate khác làm problem chính

- Camera setup là bước quan trọng nhưng là điều kiện đầu vào của solution.
- Trainer labeling là workflow evaluation nội bộ, không phải pain chính của end user.
- Progress tracking chỉ có ý nghĩa sau khi form feedback đủ tin cậy.

---

## 2. Quick Validation

Chi tiết: `validation-evidence.md`.

### Kết quả hiện có

| Nguồn | Số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Problem được sửa thế nào |
|---|---:|---|---|---|
| Thảo luận nhóm | 4 thành viên | Nhóm thống nhất người mới tập sai form là problem đáng giải quyết | Nhóm không đại diện cho người dùng mục tiêu | Chưa claim market demand; cần interview người mới |
| Prototype trước đây của một thành viên | 1 prototype | Pose-based form checking có thể xây dựng | Hiệu quả phụ thuộc dữ liệu; chưa có benchmark chuẩn | Thu hẹp sang một exercise và evaluation có HLV |
| Nguồn y khoa/chuyên môn | Nhiều nguồn | Kỹ thuật không đúng là risk factor của chấn thương thể thao | Chấn thương có nhiều nguyên nhân, không thể quy hết cho form | Không claim app ngăn chấn thương; chỉ hỗ trợ feedback |
| Nghiên cứu computer vision | Nhiều hệ thống/paper | Pose correction bằng camera là khả thi | RGB một camera còn hạn chế, nhất là động tác phức tạp/che khuất | Bắt buộc confidence gate và controlled setup |

### Baseline hiện có

| Metric | Baseline khả dụng |
|---|---:|
| Phỏng vấn người mới tập | 0 |
| Video squat được HLV gán nhãn theo schema MVP | 0 |
| Benchmark precision/recall của MVP | Chưa có |
| Bài tập trong phạm vi MVP | 1 — bodyweight squat |
| Prototype kỹ thuật trước đây | Có, nhưng chưa dùng làm baseline chuẩn hóa |

Baseline cho thấy problem có cơ sở nhưng chưa đủ để Go với sản phẩm rộng. Nhóm chỉ Go với validation prototype.

---

## 3. Current Workflow

1. Người mới xem video/hướng dẫn hoặc bắt chước người khác.
2. Tự đặt chân, thân và đầu gối theo cách mình hiểu.
3. Dùng gương hoặc camera nhưng không quan sát được mọi góc trong lúc tập.
4. Thực hiện nhiều rep.
5. Tự đánh giá bằng cảm giác.
6. Nếu nghi ngờ, quay video và xem lại.
7. Có thể gửi cho bạn hoặc HLV để hỏi sau.
8. Nhận feedback muộn và thử sửa ở set/buổi sau.

**Bottleneck:** không có feedback form có cấu trúc ngay sau rep, trong khi người mới chưa đủ kinh nghiệm để tự đánh giá.

---

## 4. Future Workflow

1. Người dùng chọn bodyweight squat và đọc boundary an toàn.
2. App hướng dẫn đặt camera đúng góc, khoảng cách và ánh sáng.
3. Quality gate kiểm tra toàn thân/keypoint có đủ rõ không.
4. Pose model trích xuất landmark theo thời gian.
5. Workflow nhận diện rep và các phase của squat.
6. Rule/classifier đánh giá một tập lỗi predefined.
7. Confidence gate quyết định: feedback, yêu cầu quay lại hoặc không kết luận.
8. App đưa tối đa một cue ngắn đã được HLV duyệt.
9. Người dùng thử lại; app lưu metric tổng hợp nếu được đồng ý.

**Human boundary:** HLV/domain expert định nghĩa form reference, error labels và cue; nhóm đánh giá model với ground truth. App không chẩn đoán, không tư vấn phục hồi, không chọn mức tạ và không thay HLV.

---

## 5. Before / After Metrics

Các số “sau kỳ vọng” là target pilot, chưa phải kết quả.

| Metric | Trước | Sau kỳ vọng trong pilot | Cách đo |
|---|---:|---:|---|
| Thời điểm nhận feedback | Sau set/buổi hoặc không có | Sau mỗi rep hợp lệ | Timestamp |
| Người dùng tự hoàn thành camera setup | Chưa đo | ≥4/5 người | Usability test |
| Frame hợp lệ có pose ổn định | Chưa đo | ≥90% | Frame-level log |
| Precision/recall theo error label | Chưa có | Mỗi metric ≥80% | So với nhãn HLV |
| Trainer–system agreement | Chưa có | ≥85% trên label trong scope | Confusion matrix/agreement |
| Feedback khi confidence thấp | Không có cơ chế | 0 kết luận kỹ thuật; 100% chuyển sang retake | Event log |
| Latency sau rep | Chưa đo | <500 ms | Device profiling |
| Claim giảm chấn thương | Không có dữ liệu | Không đo/không claim trong pilot | Boundary |

---

## 6. Problem Statement v0

| Field | Nội dung |
|---|---|
| Actor | Người trưởng thành mới tập gym, thường tập một mình |
| Workflow | Xem hướng dẫn → tự tập → tự cảm nhận/quay lại → hỏi người khác sau |
| Bottleneck | Không có feedback form có cấu trúc ngay sau từng rep |
| Impact | Có thể lặp lại lỗi, giảm hiệu quả tập và làm tăng risk do kỹ thuật không đúng |
| Success Metric | Feedback kịp thời; pose ổn định; agreement với HLV; người dùng hiểu cue |
| Boundary | Một exercise; healthy adult; controlled setup; không chẩn đoán hay thay HLV |

---

## 7. Ma trận độ phù hợp

- **Độ mơ hồ:** trung bình. Các lỗi được định nghĩa trước có nhãn rõ, nhưng hình thể, góc quay và chuyển động thực tế tạo biến thiên.
- **Độ phức tạp:** trung bình–cao. Workflow gồm camera quality, pose estimation, temporal rep detection, form classification, confidence và feedback.
- **Ô phù hợp:** Workflow có AI và rule; không cần Agent tự lập kế hoạch.

---

## 8. So sánh No AI / Rule / Workflow / Agent

| Mức | Phương án | Khi nào đủ | Rủi ro | Quyết định |
|---|---|---|---|---|
| No AI / process fix | Video chuẩn, checklist, gương hoặc HLV | Khi người dùng chỉ cần học kiến thức chung | Không quan sát được form thực tế của từng rep | Giữ làm fallback |
| Rule | Checklist tự chấm + hướng dẫn camera + cue cố định | Khi không cần tự động quan sát | Phụ thuộc người dùng tự đánh giá | Dùng cho UX/safety nhưng chưa giải bottleneck |
| Workflow có AI | Pose model → rep phase → error rule/classifier → confidence gate → cue | Khi scope một exercise và có ground truth | Sai pose, bias dữ liệu, feedback sai | **Chọn MVP** |
| Agent | Tự chọn bài, mức tạ, kế hoạch và điều chỉnh buổi tập | Chỉ khi cần tự lập kế hoạch nhiều bước với dữ liệu sức khỏe đáng tin | Rủi ro sức khỏe, permission và accountability | **No-Go** |

### Vì sao không chọn mức đơn giản hơn

Video/checklist giúp học lý thuyết nhưng không phân tích chuyển động thực tế của người dùng. AI pose workflow bổ sung khả năng quan sát từng rep, là phần trực tiếp giải bottleneck.

### Vì sao không chọn Agent

MVP không cần AI tự quyết định bài tập, mức tạ hoặc kế hoạch. Các quyết định đó vượt dữ liệu hiện có và tăng rủi ro sức khỏe. Workflow tuyến tính, có input/output rõ và cần human-defined boundary.

---

## 9. Problem Statement v1

| Field | Nội dung |
|---|---|
| Actor | Người trưởng thành mới tập gym, không có HLV quan sát trực tiếp và đang thực hiện bodyweight squat |
| Workflow | Chọn squat → camera pre-check → thực hiện rep → pose/phase/error analysis → confidence gate → feedback/retake |
| Bottleneck | Người dùng không thể tự nhìn và đánh giá nhất quán một số lỗi form cơ bản ngay sau từng rep |
| Impact | Lặp lại lỗi, giảm confidence/hiệu quả tập và có thể làm tăng rủi ro liên quan đến kỹ thuật không đúng |
| Success Metric | ≥4/5 user setup thành công; ≥90% valid-frame pose coverage; precision/recall ≥80% cho label trong scope; agreement HLV ≥85%; 0 confident feedback khi dưới threshold |
| Boundary | Healthy adults 18+; bodyweight squat; một người; ánh sáng/góc quay kiểm soát; không đau/chấn thương; không chẩn đoán, rehab, load prescription hoặc injury-prevention claim |
| AI intervention point | Sau camera quality gate và trước feedback: pose estimation + temporal/error classification |
| Mức chọn | Workflow có AI + deterministic safety rules |
| Rủi ro & người thật kiểm tra | Pose sai do occlusion/góc quay; data bias; cue sai. HLV gán nhãn/duyệt cue; Product kiểm boundary; AI/Data đo confusion matrix; app abstain khi confidence thấp |

---

## 10. Final Decision

### Decision

**Go — pilot MVP kiểm tra bodyweight squat; Not Yet cho full gym app; No-Go cho medical/autonomous coach.**

### Pilot nhỏ nhất

- Mời `5` người mới tập và `1` HLV/domain reviewer.
- Mỗi người thực hiện squat trong điều kiện chuẩn hóa; thu khoảng `10–20` rep/người sau khi đồng ý tham gia.
- HLV gán nhãn theo `trainer-labeling-guide.md`.
- So sánh model/rule với nhãn HLV bằng confusion matrix, precision, recall và F1 theo từng lỗi.
- Test camera setup, latency, mức độ hiểu feedback và privacy consent.
- Không cho người có đau, chấn thương đang điều trị hoặc cần phục hồi tham gia pilot.

### Điều kiện Go tiếp

1. Người dùng xác nhận problem và sẵn sàng dùng camera.
2. HLV đồng ý schema lỗi có thể quan sát từ góc quay MVP.
3. Model đạt target trên test set tách biệt.
4. Không có confident wrong feedback vượt ngưỡng nhóm chấp nhận.
5. Người dùng hiểu feedback và biết app không thay HLV.

### Điều kiện Not Yet / rollback

- Pose coverage hoặc trainer agreement không đạt target.
- Kết quả thay đổi mạnh theo hình thể, quần áo, ánh sáng hoặc góc quay.
- Người dùng không sẵn sàng quay video.
- Feedback khiến người dùng hiểu sai hoặc bỏ qua cảm giác đau.
- Khi đó, hạ solution về camera setup + quay video + checklist/HLV review thay vì mở rộng AI.
