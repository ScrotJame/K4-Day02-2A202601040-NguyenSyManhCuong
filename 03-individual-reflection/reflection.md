# Individual Reflection — Day 02 Lab

## 1. Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| **Scan cá nhân** | Scan 8 problems từ trải nghiệm thực tế (BĐS sales, tra cứu giấy tờ SV, học từ vựng...) và lập Top 3 Problem Cards. | Đưa 3 candidate cards vào ngân hàng ý tưởng của nhóm, đóng góp góc nhìn về workflow lặp lại và tốn thời gian. |
| **Pitch Problem Card** | Trình bày Top 1 Card (Tư vấn viên BĐS cá nhân hóa nội dung) và Top 2 Card (Tra cứu trạng thái hồ sơ sinh viên). | Giúp nhóm có thêm lựa chọn ở mảng tra cứu quy trình và cá nhân hóa tư vấn. |
| **Challenge bài của bạn khác** | Phản biện candidate về chatbot học tập & app tập gym tổng quát (hỏi về data access, privacy và rủi ro nếu AI phán sai). | Giúp nhóm thu hẹp scope từ "app gym toàn năng" xuống chỉ một exercise cụ thể: bodyweight squat. |
| **Gom trùng / cluster** | Cùng nhóm gom 12 candidates thành 4 clusters: Core user feedback, Capture quality, Data & evaluation, và Scope/Privacy/Safety. | Định hình được cấu trúc các nhóm vấn đề chính để chuẩn bị cho bước shortlist. |
| **Chọn candidate problem** | Tham gia chấm điểm (Score 1-5) và thống nhất chọn candidate "AI feedback cho bodyweight squat". | Đồng thuận hạ bài tư vấn BĐS của mình để tập trung vào bài toán có input camera/pose rõ ràng và workflow dễ đo lường. |
| **Validation / research** | Tìm hiểu về MediaPipe Pose Landmarker, MoveNet và các nghiên cứu y khoa (NIAMS, PubMed) về nguy cơ sai kỹ thuật. | Đóng góp lập luận: AI chỉ hỗ trợ phát hiện lỗi kỹ thuật quan sát được, không claim "ngăn ngừa chấn thương". |
| **Workflow nhóm** | Thảo luận vẽ Current & Future State Workflow, xác định rõ điểm nghẽn ở bước không có feedback ngay sau từng rep. | Bổ sung bước Camera Quality Gate và Confidence Gate vào Future Workflow của nhóm. |
| **Problem Statement** | Tham gia góp ý xây dựng Problem Statement v0 và v1, đặc biệt ở phần Boundary và Success Metric. | Thống nhất metric precision/recall ≥80% theo nhãn HLV và 0 kết luận khi confidence dưới ngưỡng. |
| **Rule / Workflow / Agent** | So sánh 4 cấp độ giải pháp; phân tích lý do vì sao không nên dùng Agent tự động hoàn toàn. | Thống nhất chọn mức **Workflow có AI + deterministic safety rules**, tránh bẫy "Agent-first". |
| **Decision** | Thảo luận và thống nhất quyết định cuối: **Go** cho pilot MVP bodyweight squat, **Not Yet** cho full gym app, **No-Go** cho autonomous coach. | Đóng góp điều kiện Go/Rollback và thiết kế pilot nhỏ nhất (5 user + 1 HLV). |

## 2. Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| **Scan** | Hỏi gợi ý thêm problem theo 4 lăng kính sau khi đã tự list 5 ý tưởng. | Gợi ý thêm góc nhìn về các task lặp lại trong chăm sóc khách hàng và hỗ trợ thủ tục. | AI hay đưa ra ý tưởng quá rộng dạng "Trợ lý AI toàn năng" hoặc "App sức khỏe tổng thể". | Lọc bỏ các ý quá rộng, chỉ giữ lại các problem có actor và workflow quan sát được. |
| **Problem Card** | Dùng prompt "skeptical PM" để phản biện 3 Problem Cards cá nhân. | Bắt lỗi metric chưa đo được và cảnh báo việc mình nhảy sang gut "Agent" quá sớm. | AI chưa hiểu bối cảnh dữ liệu thực tế (ví dụ: dữ liệu BĐS bị phân tán/bảo mật). | Đưa Non-AI alternative (template/checklist) vào card và làm rõ bottleneck thực sự. |
| **Workflow** | Dùng AI chuyển đổi mô tả dạng chữ sang cú pháp Mermaid flowchart. | Tạo sơ đồ nhanh, chuẩn hóa format các bước before/after workflow. | AI tự động bỏ qua các bước kiểm tra điều kiện đầu vào (Camera quality) và bước Abstain. | Tự tay thêm các nhánh Fallback/Abstain và Human boundary vào sơ đồ Mermaid. |
| **Research** | Tìm các công nghệ pose estimation (MediaPipe, MoveNet) và paper liên quan (Pose Tutor). | Tổng hợp nhanh điểm mạnh/yếu của các pretrained model có sẵn. | AI hay "bịa" số liệu hiệu năng hoặc claim AI giúp triệt tiêu chấn thương 100%. | Tra cứu link chính thức từ Google/PubMed, xóa bỏ mọi claim vô căn cứ về chấn thương. |
| **Problem Statement** | Hỏi phản biện 6 fields của Problem Statement v0. | Chỉ ra câu từ trong phần Impact còn mơ hồ ("giúp tập tốt hơn" -> chưa đo được). | AI đề xuất viết lại PS theo hướng thương mại hóa quá đà, làm mất tính tập trung của lab. | Giữ nguyên form tự viết, chỉ sửa câu từ Metric thành số liệu cụ thể (≥80% precision/recall). |
| **Rule / Workflow / Agent** | Hỏi phản biện lý do tại sao không dùng Agent cho bài toán check form gym. | Cung cấp góc nhìn về rủi ro an toàn (health safety) và accountability khi dùng Agent. | AI hay xuôi theo hướng "Agent sẽ tự điều chỉnh bài tập thông minh hơn" nếu không nhắc rủi ro. | Nhất quyết chọn mức Workflow, định nghĩa boundary người thật (HLV) duyệt cue và label. |
| **Decision** | Tham khảo danh sách tiêu chí kiểm tra Go / Not Yet / No-Go. | Gợi ý cấu trúc cho kế hoạch Pilot nhỏ nhất (số lượng mẫu, quy trình thu thập). | AI đề xuất pilot quá lớn (cần 100+ người tập) không khả thi trong nguồn lực lab. | Rút gọn pilot xuống 5 người mới tập + 1 HLV để kiểm chứng nhanh trong 1-2 tuần. |

## 3. Reflection câu hỏi mở

### 3.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?
Khi nghe các bạn pitch (đặc biệt là ý tưởng về AI check form tập gym), tôi nhận ra một bài toán hay cho AI không phải là bài toán "cần chatbot trả lời hay", mà là bài toán có **actor rõ ràng**, **workflow quan sát được** và **bottleneck xảy ra ngay tại thời điểm thực hiện task**. Ý tưởng dùng camera quan sát bodyweight squat có ưu điểm vượt trội so với bài toán tư vấn BĐS hay tra cứu giấy tờ của tôi vì:
- Dữ liệu đầu vào (video/pose landmark) trực quan, có thể quan sát bằng mắt thường.
- Bottleneck "không có feedback ngay sau rep" là pain point trực tiếp, giải quyết bằng Computer Vision phù hợp hơn nhiều so với việc chỉ trò chuyện bằng chữ.

### 3.2. Nhóm có lúc nào bị solution-first không?
Có. Ở giai đoạn đầu, cả cá nhân tôi (chọn gut là "Agent" cho Problem Card BĐS) và một số bạn trong nhóm đều có xu hướng nghĩ ngay tới "Agent AI thông minh tự điều chỉnh giáo án tập luyện". Tuy nhiên, nhóm đã kịp thời nhận ra rủi ro khi đối chiếu với nguyên tắc **"Problem first, not AI first"**:
- Nhóm đã dừng lại để vẽ **Current Workflow** của người mới tập squat và thấy rằng điểm nghẽn thực sự chỉ là *thiếu feedback kỹ thuật tức thì*.
- Việc tự lập kế hoạch tập hay chỉnh mức tạ (Agent) vừa vượt quá scope vừa tạo rủi ro sức khỏe lớn. Từ đó, nhóm kiên quyết hạ mức xuống **Workflow có AI + Safety Rules**.

### 3.3. Tôi có thay đổi ý kiến sau khi bị challenge không?
Có. Ban đầu tôi rất muốn nhóm chọn bài toán "Tư vấn viên BĐS cá nhân hóa nội dung" của tôi vì nghĩ nó có giá trị thương mại cao. Nhưng khi bị nhóm challenge:
- *"Lấy đâu ra dữ liệu bảng giá, dự án và hồ sơ khách hàng thật để AI chạy?"*
- *"Bài này nếu làm không cẩn thận chỉ dừng lại ở mức Prompt Template cho ChatGPT chứ chưa cần AI System."*

Tôi nhận thấy phản biện này hoàn toàn chính xác. Tôi đã chủ động ủng hộ nhóm chuyển hướng sang candidate **Bodyweight Squat Form Check** vì bài này khả thi hơn trong phạm vi lab, có thể dựng prototype bằng MediaPipe và dễ dàng benchmark với nhãn của HLV.

### 3.4. Tôi đóng góp gì thật sự vào artifact cuối?
- **Về mặt lập luận:** Tôi đóng góp tích cực vào buổi thảo luận Phase 6, kiên trì phản biện để nhóm chọn giải pháp mức **Workflow** thay vì sa vào **Agent**, đồng thời bổ sung khái niệm **Confidence Gate / Abstention** (nếu camera mờ hoặc thiếu sáng thì thà từ chối đánh giá chứ không phán sai).
- **Về mặt nghiên cứu & nội dung:** Tham gia tra cứu tài liệu về MediaPipe Pose Landmarker, đóng góp phần biên soạn rủi ro kỹ thuật và xây dựng các tiêu chí cho **Pilot nhỏ nhất** (5 người tập + 1 HLV).

### 3.5. Điều khó nhất khi viết Problem Statement là gì?
Điều khó nhất là việc xác định **Boundary** (Phạm vi & Giới hạn an toàn) và **Success Metric**:
- Rất dễ bị rơi vào bẫy viết metric chung chung kiểu "giúp người tập ít chấn thương hơn" hoặc "tăng hiệu quả tập luyện" — những thứ không thể đo được trong ngắn hạn và chịu ảnh hưởng bởi quá nhiều biến số ngoài AI.
- Nhóm phải đấu tranh tư tưởng để ép Metric về các chỉ số đo được trong pilot: precision/recall ≥80% theo nhãn HLV, tỷ lệ setup camera thành công ≥4/5 người, và coverage pose hợp lệ ≥90%.

### 3.6. Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?
Nếu được làm lại, tôi sẽ challenge nhóm mạnh hơn ở phase **Quick Validation (Phase 4)** ngay từ đầu:
- Nhóm hiện tại chủ yếu dựa vào thảo luận nội bộ và kinh nghiệm prototype cũ, chứ chưa phỏng vấn trực tiếp 5 người mới tập thật xem họ có **thực sự sẵn sàng dựng điện thoại quay clip khi tập một mình tại nhà/phòng gym hay không**.
- Yếu tố rủi ro về UX và Privacy (ngại quay camera) có thể làm vỡ toàn bộ giả định của sản phẩm, do đó cần làm micro-interview/poll người dùng ngay trước khi chốt Go cho pilot.