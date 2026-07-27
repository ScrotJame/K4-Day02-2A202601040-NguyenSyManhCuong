# Group Report — Day 02

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|-----|-----------|-------------|-------------------|
| 1 | Nguyễn Hoàng Hải | 2A202601426 | Trưởng nhóm — Điều phối thảo luận & chốt quyết định cuối |
| 2 | Phạm Quốc Bảo | 2A202601502 | Nghiên cứu & Kiểm chứng (Research & Validation) |
| 3 | Nguyễn Văn Thành | 2A202601030 | Phó nhóm — Tổng hợp nội dung & quản lý file nộp bài |
| 4 | Nguyễn Duy Khánh | 2A202601530 | Vẽ Workflow trước/sau (Current & Future State) |
| 5 | Ngô Xuân Ninh | 2A202601068 | Soạn thảo Problem Statement v0 & v1 |
| 6 | Trần Đức Bảo | 2A202601472 | Nghiên cứu & Kiểm chứng (Research & Validation) |
| 7 | Trần Hoàng Long | 2A202601646 | Phản biện (Devil's Advocate — Challenge bài toán & metric) |
| 8 | Phạm Công Đạt | 2A202601406 | Ghi chép & Thư ký (Meeting Notes & Nhật ký hội tụ) |
| 9 | Nguyễn Sỹ Mạnh Cường | 2A202601040 | Phân tích & So sánh phương án (No AI / Rule / Workflow / Agent) |
| 10 | Nguyễn Chiến Thắng | 2A202601734 | Trình bày & Kiểm tra checklist cuối (Presenter & QA) |

> **Ghi chú phân công:** Mỗi người chịu trách nhiệm chính vai trò của mình nhưng tất cả tham gia thảo luận, pitch và challenge trong các Phase 3–6. Bản nộp nhóm là sản phẩm chung của toàn nhóm.

## Phase 3 — Group Convergence: từ candidates về 1 (30')
 
**Mục tiêu:** Không vote ngay. Đi qua 4 bước hội tụ: Trình bày top 3 → gom trùng/cluster → shortlist → chấm nhanh + đồng thuận chọn 1 candidate problem. Nhóm lúc này **chỉ chọn candidate problem**, chưa viết Problem Statement hoàn chỉnh.
 
> *Lưu ý về dữ liệu:* nhóm ở đây chỉ có 3 candidate được phát triển đầy đủ (thay vì 9–12 của một nhóm 3–4 người), nên bảng bên dưới chỉ điền 3 dòng có dữ liệu thật; tên người đưa ra để trống theo yêu cầu.
 
### Bước 3.1 — Trình bày top 3
 
| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh |
|---|---|---|---|---|---|
| 1 | | Tài nguyên học tập, code mẫu và tài liệu nghiên cứu bị phân mảnh trên nhiều app, mỗi lần tìm mất 10–15 phút | Bản thân (Dev & Researcher) | Không có trung tâm định tuyến dữ liệu; tagging không đồng bộ giữa các app | Đau thật, xảy ra hằng ngày, nhưng giải pháp (RAG + vector DB) hơi nặng cho 1 buổi lab |
| 2 | | Ngồi làm việc/học liên tục 3–4 tiếng trước máy tính, ít vận động, mỏi vai gáy cuối ngày | Bản thân | Thiếu cơ chế ngắt nhịp chủ động khi đang tập trung cao độ (hyper-focus) | Đau thật nhưng dễ giải quyết bằng công cụ có sẵn (Pomodoro/Stretchly) — ít "chất" AI |
| 3 | | Người mới tập gym không biết mình đang tập sai form ở đâu, ngại chủ động hỏi PT/nhân viên để được chỉnh | Người mới tập gym (0–6 tháng kinh nghiệm) | Ngại chủ động hỏi (rào cản tâm lý) + thuê PT tốn 250K–1,5tr/buổi và phải chờ lịch (rào cản thực tế) | Có bằng chứng khảo sát thật (không phải đoán), actor cụ thể, tác động rõ (chấn thương, bỏ tập) |
 
### Bước 3.2 — Gom trùng / cluster
 
| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| A | Candidate 1 | Hiệu suất công việc trí óc (knowledge-work efficiency) — mất thời gian ở khâu "thao tác thông tin" quanh nghiên cứu/lập trình | Chỉ có 1 đại diện, không cần lọc thêm trong cluster này |
| B | Candidate 2, Candidate 3 | Sức khỏe & vận động thể chất — cả hai đều liên quan đến cơ thể khi vận động/ít vận động | Khác actor và khác chất lượng bằng chứng: Candidate 2 chỉ là quan sát cá nhân, Candidate 3 có khảo sát thị trường thật (OnePoll, ACE, HFA, NEISS) → Candidate 3 đủ sức đại diện cho cả cluster B |
 
### Bước 3.3 — Shortlist
 
| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|---|---|---|
| 1. Tài nguyên phân mảnh | Actor rõ, bottleneck cụ thể, đo được (thời gian tìm kiếm), vẽ before/after được | Phạm vi giải pháp (Agent + vector DB) có thể quá rộng cho 1 buổi lab |
| 2. Ít vận động khi ngồi máy tính | Actor rõ, dễ làm trong lab (Rule/Workflow đơn giản) | "Pain" chưa có bằng chứng ngoài bản thân; impact (cảm giác đau mỏi) khó đo khách quan |
| 3. Tập sai form ở gym | Actor cụ thể, bottleneck rõ (đúng 2 bước trong workflow), có evidence khảo sát thật, impact đo được qua baseline ngành | Nhóm chưa phải chuyên gia fitness/PT nên cần research thêm để hiểu đúng "form chuẩn"; giải pháp đầy đủ (Agent, camera real-time) khá phức tạp về kỹ thuật |
 
### Bước 3.4 — Score để đồng thuận
 
| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| 1. Tài nguyên phân mảnh | 4 | 5 | 3 | 5 | 2 | 4 | 4 | 27/35 |
| 2. Ít vận động | 4 | 5 | 2 | 3 | 5 | 3 | 5 | 27/35 |
| 3. Tập sai form ở gym | 5 | 5 | 5 | 5 | 3 | 5 | 3 | **31/35** |
 
Candidate nhóm chọn:
 
```text
Candidate 3 — Người mới tập gym không biết mình đang tập sai form ở đâu,
và né tránh việc chủ động hỏi PT/nhân viên để được chỉnh trực tiếp.
```
 
Vì sao chọn:
 
```text
- Điểm cao nhất và đồng đều nhất trên 7 tiêu chí (31/35), không có tiêu chí nào dưới 3.
- Là candidate duy nhất có "pain" được xác nhận bằng khảo sát thị trường thật
  (OnePoll/Isopure n=2.000, ACE, HFA, NEISS) thay vì chỉ dựa vào quan sát cá nhân —
  giảm rủi ro giải quyết một vấn đề tưởng tượng.
- Bottleneck định vị chính xác vào 2 bước cụ thể trong workflow (bước 4 và 5),
  không mơ hồ như "mệt mỏi" hay "thiếu thời gian".
- Impact có baseline ngành để so sánh trước/sau (50% bỏ tập 6 tháng đầu,
  22% bỏ ngay tháng đầu), nên success metric không phải số tự bịa.
- Điểm yếu duy nhất (Làm trong lab: 3/5, Nhóm hiểu domain: 3/5) có thể xử lý
  bằng cách thu hẹp MVP và research thêm ở Phase 4, không phải lý do loại bỏ.
```
 
Vì sao không chọn các candidate còn lại:
 
```text
- Candidate 1 (tài nguyên phân mảnh): điểm ngang Candidate 2 (27/35) nhưng yếu nhất
  ở "Làm trong lab" (2/5) — cần hạ tầng RAG + vector DB, rủi ro không xong trong buổi.
  Giữ lại làm backlog cho lab sau khi có nhiều thời gian hơn.
- Candidate 2 (ít vận động): dễ làm nhất (Làm trong lab: 5/5) nhưng yếu nhất ở
  "Pain có evidence" (2/5) và "Impact đo được" (3/5) — chỉ dựa cảm nhận cá nhân,
  chưa có gì để so sánh trước/sau một cách khách quan. Phù hợp làm bài tập cá nhân
  hơn là candidate đại diện cho cả nhóm.
```
 
Nếu có disagreement, nhóm xử lý thế nào:
 
```text
Ưu tiên candidate có điểm "Pain có evidence" và "Impact đo được" cao hơn khi các
tiêu chí khác gần bằng nhau, vì hai tiêu chí này quyết định việc Problem Statement
ở Phase 5 có đứng vững hay không. Nếu vẫn chia rẽ, dùng thời gian còn lại của
Phase 4 (Quick Validation) làm trọng tài — candidate nào được validate thực tế
tốt hơn thì đi tiếp.
```
 
---
 
## Phase 4 — Quick Validation + Research giải pháp (30')
 
**Mục tiêu:** Kiểm tra nhanh pain có thật không, người khác có gặp không, đã có giải pháp nào tương tự chưa, và bài toán có nên giải bằng AI không.
 
### Bước 4.1 — Quick validation
 
**Kết quả:**
 
| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Interview (Option A) | *chưa thực hiện* | — | — | Cần làm trong buổi lab: hỏi 2–3 người mới tập gym quen biết tại VN, vì toàn bộ khảo sát hiện có đều lấy mẫu ở Mỹ, chưa chắc đúng bối cảnh VN |
| Survey / poll (dữ liệu thứ cấp) | 2.000 người Mỹ (OnePoll/Isopure) + mẫu khảo sát ACE | 50% người tập gym vẫn thấy "gymtimidation"; 21% né tránh gym vì không biết phải làm gì, thêm 3% nói thẳng "sợ phải hỏi" | Chưa tìm thấy tín hiệu phản bác trực tiếp trong khảo sát đã có | Giữ nguyên problem, nhưng gắn nhãn "cần verify tại VN" cho các con số này trước khi dùng làm success metric chính thức |
| Log / review / ticket | Dữ liệu toàn quốc Mỹ (US CPSC — NEISS, 2020) | 1–2 triệu ca chấn thương liên quan hoạt động/thiết bị thể dục cần điều trị y tế mỗi năm; sai form là nguyên nhân hàng đầu được nhắc đến | Đây là dữ liệu thứ cấp cấp quốc gia, không phải log nội bộ — không đo được tỷ lệ chấn thương chỉ do "sai form không được sửa kịp" tách riêng khỏi các nguyên nhân khác | Dùng như bằng chứng bối cảnh (impact tối đa có thể xảy ra), không dùng làm baseline chính xác cho success metric |
 
### Bước 4.2 — Research giải pháp đã có
 
| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Gymscore | https://www.gymscore.ai/ | Người dùng quay video khi tập squat/deadlift, hệ thống <cite index="20-1">đánh giá kỹ thuật theo nhiều chỉ số chuyển động, chấm điểm số và đưa gợi ý cải thiện</cite>. <cite index="21-1">Được huấn luyện trên hàng nghìn lượt tập và nhận diện hơn 2.500 bài tập khác nhau</cite> | Đã giải quyết trọn vẹn đúng bước 4–5 mà nhóm nhắm tới: phản hồi form gần như tức thời, không cần hỏi người thật. <cite index="21-1">Có hướng dẫn cụ thể cách đặt camera (lệch 30–60 độ so với hướng chính diện) để tăng độ chính xác phân tích</cite> | Là sản phẩm thương mại đã trưởng thành — nhóm khó cạnh tranh trực diện; cần tìm ngách riêng (ví dụ: tập trung người *mới* thay vì người tập lâu năm, giá rẻ hơn cho thị trường VN) | Xác nhận bài toán khả thi về mặt kỹ thuật (đã có người làm được ở mức thương mại) — nhóm nên định vị lại: làm phiên bản tối giản, giá hợp túi tiền, hướng riêng cho người mới tại VN, thay vì làm lại một Gymscore thu nhỏ |
| QuickPose.ai (SDK) | https://quickpose.ai/lp/build-fitness-app/ | <cite index="4-1">Cung cấp SDK dựa trên MediaPipe để nhà phát triển tự thêm rep counter, timer và form feedback vào app của mình</cite>, tức là hạ tầng kỹ thuật, không phải sản phẩm end-user | <cite index="4-1">Tối ưu tốc độ xử lý camera feed, có thể mở rộng quy mô</cite> — giúp nhóm không cần tự xây pose estimation từ số 0 | Chỉ là dev tool — nhóm vẫn phải tự thiết kế UX, nội dung "form chuẩn" cho từng bài tập và logic phản hồi | Với phạm vi 1 buổi lab, nên dùng SDK có sẵn (QuickPose hoặc MediaPipe mở) làm lớp kỹ thuật nền, tập trung thời gian vào phần nhóm tạo khác biệt: nội dung phản hồi + trải nghiệm cho người mới |
| Dự án mã nguồn mở (ví dụ *fitness-trainer-pose-estimation*) | https://github.com/yakupzengin/fitness-trainer-pose-estimation | <cite index="6-1">Dùng pose estimation thời gian thực để đếm rep, theo dõi form và đưa phản hồi tức thì cho các bài squat, hít đất, gập tay</cite> | Miễn phí, mã nguồn mở, có thể tham khảo kiến trúc (frontend stream video, backend Flask, exercise engine) | Là dự án cá nhân/side-project, chưa production-ready, chưa được kiểm thử trên nhiều người dùng thật | Có thể dùng làm tài liệu tham khảo kiến trúc kỹ thuật miễn phí cho prototype, nhưng không nên dùng thẳng cho pilot có người dùng thật mà chưa kiểm tra lại |
 
**Nhận xét chung:** giới hạn kỹ thuật lớn nhất của cả ngành, kể cả các sản phẩm thương mại, là <cite index="14-1">ước lượng độ sâu từ một camera đơn (monocular) vốn là bài toán thiếu ràng buộc — sai số nhỏ trong ước lượng có thể dẫn tới kết quả độ sâu lệch đáng kể</cite>. Đây là rủi ro kỹ thuật thật, không phải giả định — nhóm nên đưa vào Boundary ở Phase 5/6 thay vì bỏ qua.
 
Không dùng số liệu AI đưa ra nếu không verify được — toàn bộ số liệu trong bảng trên đều có link nguồn kèm theo để nhóm tự kiểm tra lại.
 
---
 
## Phase 5 — Workflow + Problem Statement (45')
 
### Bước 5.1 — Current workflow bản nhóm
 
| Bước | Actor | Input | Output | Thời gian/tần suất | Ghi chú |
|---|---|---|---|---|---|
| 1. Xem hướng dẫn | Người mới tập | Video YouTube/TikTok | Kiến thức lý thuyết về động tác | 10–20 phút, trước mỗi buổi tập mới | Tự học, không có phản hồi |
| 2. Tự tập theo trí nhớ | Người mới tập | Trí nhớ từ video đã xem | Thực hiện động tác tại phòng gym | Mỗi buổi tập (2–4 lần/tuần) | Không ai kiểm tra |
| 3. Tự soi & tự đánh giá | Người mới tập | Gương phòng gym / video tự quay | Nghi ngờ đúng/sai nhưng không chắc chắn | Vài giây–vài phút mỗi hiệp | Thiếu chuyên môn để tự chỉnh |
| 4. Ngại chủ động hỏi | Người mới tập ↔ PT/nhân viên | Mong muốn được hỏi | Không hỏi, giữ nguyên form sai | Gần như mỗi buổi | **Bottleneck #1** — rào cản tâm lý |
| 5. Thuê PT & chờ lịch | Người mới tập ↔ PT | Đặt lịch + 250K–1,5tr/buổi | Phản hồi chỉnh form (nếu quyết định thuê) | Theo lịch hẹn, không tức thời | **Bottleneck #2** — rào cản chi phí + thời gian |
| 6. Lặp lại sai form | Người mới tập | Form sai chưa được sửa | Đau/chấn thương hoặc bỏ tập | Tích lũy qua nhiều buổi | Hệ quả cuối nếu không can thiệp ở bước 4–5 |
 
Bottleneck chính:
 
```text
Bước 4 và 5: người mới không nhận được phản hồi chỉnh form nào đúng lúc,
vì rào cản tâm lý (ngại chủ động hỏi) cộng rào cản thực tế (chi phí PT 250K–1,5tr/buổi
và phải chờ đúng lịch hẹn mới có phản hồi).
```
 
### Bước 5.2 — Future workflow bản nhóm
 
```text
1. Xem hướng dẫn (giữ nguyên — người tự học)
2. Tự tập theo trí nhớ (giữ nguyên — người tự làm)
3. [Thay bước "tự soi" + "ngại hỏi"] → Quay clip ngắn ngay tại chỗ, gửi vào
   AI Form-Check (Workflow: pose estimation + rule chấm theo từng bài tập)
4. Nhận điểm form + gợi ý chỉnh sửa cụ thể trong <1 phút (AI/Workflow xử lý)
5. [Boundary] Nếu điểm quá thấp nhiều lần liên tiếp, hoặc người dùng báo đau →
   hệ thống dẫn về gặp PT/chuyên gia y tế thật (con người xử lý, không để AI tự quyết)
6. Thuê PT & chờ lịch trở thành lựa chọn dự phòng cho case phức tạp,
   không còn là con đường duy nhất
```
 
Before/after impact:
 
| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Số bước | 6 | 4 | Gộp "tự soi" + "ngại hỏi" thành 1 bước quay clip gửi AI |
| Thời gian nhận phản hồi | Vài ngày–vài tuần (chờ lịch PT), hoặc không bao giờ | Dưới 1 phút sau khi quay clip | |
| Số bước thủ công / tự xử lý | 4/6 bước | 1–2 bước (quay clip, đọc gợi ý) | |
| Bottleneck chính | Ngại hỏi + chi phí/lịch PT (con người) | Độ chính xác của AI khi chỉ dùng 1 góc camera (kỹ thuật) | Bottleneck chuyển từ rào cản con người sang giới hạn kỹ thuật |
| Risk mới | — | AI chấm sai hoặc bỏ sót dấu hiệu chấn thương nếu thiếu boundary/fallback rõ | Cần người thật (PT) kiểm tra định kỳ |
 
### Bước 5.3 — Problem Statement v0
 
| Field | Nội dung |
|---|---|
| **Actor** | Người mới tập gym, 0–6 tháng kinh nghiệm — giai đoạn quyết định gắn bó lâu dài hay bỏ cuộc |
| **Workflow** | 6 bước: xem hướng dẫn → tự tập theo trí nhớ → tự soi/tự đánh giá → ngại chủ động hỏi → thuê PT & chờ lịch → lặp lại sai form |
| **Bottleneck** | Bước 4 & 5: rào cản tâm lý (ngại hỏi) + rào cản thực tế (chi phí 250K–1,5tr/buổi và thời gian chờ lịch PT) |
| **Impact** | 50% hội viên mới bỏ tập trong 6 tháng đầu, 22% bỏ ngay tháng đầu (nguồn Mỹ, cần verify tại VN); 1–2 triệu ca chấn thương/năm liên quan hoạt động thể dục tại Mỹ, sai form là nguyên nhân hàng đầu |
| **Success Metric** | ≥80% buổi tập có ít nhất 1 phản hồi chỉnh form cụ thể; giảm tỷ lệ bỏ tập 3 tháng đầu so với mức nền ngành — con số mục tiêu cần xác nhận qua pilot thực tế |
| **Boundary** | AI chỉ đưa gợi ý chỉnh form dựa trên hình ảnh/video, không chẩn đoán y tế; nếu điểm form thấp liên tục hoặc người dùng báo đau, hệ thống dẫn về gặp PT/chuyên gia y tế thật thay vì tự xử lý tiếp |
 
---
 
# Break (10')
 
---
 
## Phase 6 — Rule / Workflow / Agent + Decision (25')
 
### Bước 6.0 — Ma trận độ phù hợp với AI
 
Tự kiểm nhanh:
 
| Câu hỏi | Trả lời của nhóm | Kết luận |
|---|---|---|
| Output có thể khác nhau mỗi lần mà vẫn chấp nhận được không? | Có — phản hồi chỉnh form có thể diễn đạt khác nhau, miễn đúng ý và đúng động tác | Độ mơ hồ cao |
| Cần phối hợp 3+ bước hoặc 3+ nguồn dữ liệu không? | Có — nhận diện khớp, so sánh với chuẩn theo từng bài tập, sinh phản hồi ngôn ngữ tự nhiên, theo dõi tiến bộ theo thời gian | Độ phức tạp cao |
| AI có cần tự quyết định bước tiếp theo không? | Có thể cần — ví dụ khi phát hiện dấu hiệu bất thường (điểm form thấp liên tục), hệ thống cần tự đề xuất dừng bài tập / chuyển sang gặp PT | Có thể cần Agent |
 
Bài toán của nhóm nằm ở ô nào?
 
```text
Độ phức tạp cao × Độ mơ hồ cao
```
 
Vì sao?
 
```text
Không có một "form đúng" duy nhất áp dụng cho mọi cơ địa — chấp nhận nhiều cách
diễn đạt phản hồi miễn đúng ý (mơ hồ cao). Đồng thời cần phối hợp nhiều bước
(nhận diện khớp → so sánh chuẩn theo từng bài tập → sinh ngôn ngữ phản hồi →
theo dõi lịch sử) nên độ phức tạp cao. Theo ma trận, đây là ô mà "Agent có thể
phù hợp, nhưng cần boundary, người thật kiểm tra và phương án quay về rất rõ" —
tức là Agent không bị loại, nhưng cũng không được dùng nếu thiếu 3 điều kiện đó.
```
 
### Bước 6.1 — So sánh Rule / Workflow / Agent
 
| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Checklist tĩnh hiển thị sẵn trong app (vd: "đầu gối không vượt quá mũi chân" cho squat) | Chỉ đủ cho 1 bài tập rất cơ bản, không cá nhân hóa theo cơ địa | Không phát hiện lỗi thực tế của từng người, dễ bỏ sót | Không |
| **Workflow** | Người dùng quay clip ngắn → chạy pose estimation (SDK có sẵn như QuickPose/MediaPipe) theo bộ rule cố định cho từng bài tập → xuất điểm + gợi ý theo template | Đủ cho MVP: 1–2 bài tập phổ biến (squat, plank), phản hồi theo kịch bản có sẵn | Cứng nhắc với biến thể cơ thể/góc quay; giới hạn kỹ thuật về ước lượng độ sâu từ 1 camera | ✅ (chọn cho pilot) |
| **Agent** | Hệ thống tự nhận diện bài tập đang tập, tự chọn bộ tiêu chí phù hợp, tự sinh phản hồi theo từng lỗi cụ thể, tự đề xuất khi nào nên gặp PT thật | Cần khi mở rộng nhiều bài tập/mức độ và muốn phản hồi tự nhiên như PT thật | Chi phí phát triển/vận hành cao hơn; khó kiểm soát khi AI tự quyết định fallback (vd tự ý khuyên ngừng tập) | Chưa — để vòng sau |
 
Mức chọn:
 
```text
Workflow (cho pilot trong phạm vi lab hôm nay), có lộ trình nâng lên Agent
khi đã kiểm chứng nhu cầu và độ chính xác.
```
 
Vì sao chọn:
 
```text
Rule có giải được 70-80% case không? Không — mỗi cơ địa, mỗi góc quay khác nhau,
rule tĩnh sẽ bỏ sót nhiều lỗi thật. Workflow có đủ vì các bước khá rõ không? Có,
với phạm vi thu hẹp (1-2 bài tập, dùng SDK pose estimation có sẵn thay vì tự xây),
Workflow đã giải quyết đúng bottleneck (bước 4 & 5) mà không cần AI tự lập kế
hoạch nhiều bước. Đây là phương án đơn giản nhất vẫn giải quyết được bottleneck.
```
 
Vì sao không chọn mức đơn giản hơn:
 
```text
Rule tĩnh không đủ vì bài toán có độ mơ hồ cao (không có 1 form chuẩn cho mọi
cơ địa) — một checklist cố định sẽ báo sai hoặc bỏ sót phần lớn trường hợp thật,
khiến người dùng mất niềm tin ngay từ lần dùng đầu tiên.
```
 
### Bước 6.2 — Problem Statement v1
 
| Field | Nội dung |
|---|---|
| **Actor** | Người mới tập gym, 0–6 tháng kinh nghiệm |
| **Workflow** | Xem hướng dẫn → tự tập → quay clip ngắn → AI (Workflow) chấm form & phản hồi → (fallback) gặp PT nếu điểm thấp liên tục/báo đau |
| **Bottleneck** | Ngại chủ động hỏi (tâm lý) + chi phí/lịch PT (250K–1,5tr/buổi, thực tế) |
| **Impact** | 50% bỏ tập 6 tháng đầu, 22% bỏ ngay tháng đầu; 1–2 triệu ca chấn thương/năm tại Mỹ liên quan hoạt động thể dục |
| **Success Metric** | ≥80% buổi tập có ít nhất 1 phản hồi chỉnh form cụ thể; giảm tỷ lệ bỏ tập 3 tháng đầu so với mức nền — cần xác nhận qua pilot |
| **Boundary** | AI không chẩn đoán y tế; không tự ý khuyên dừng hẳn việc tập — chỉ gợi ý chỉnh động tác và dẫn về PT thật khi có dấu hiệu bất thường |
| **AI intervention point** | Ngay sau bước 3 (tự soi) — thay vì "ngại hỏi", người dùng quay clip ngắn và AI (Workflow: pose estimation + rule chấm theo bài tập) phản hồi tức thì |
| **Mức chọn** | Workflow (pilot) → Agent (mở rộng sau) |
| **Rủi ro & người thật kiểm tra** | Rủi ro: AI chấm sai do hạn chế ước lượng độ sâu từ 1 camera; bỏ sót chấn thương tiềm ẩn. Người thật kiểm tra: 1 PT cộng tác review định kỳ mẫu phản hồi của AI (vd 1 lần/tuần) để hiệu chỉnh rule |
 
### Bước 6.3 — Final decision
 
| Câu hỏi | Yes / Not Yet / No | Ghi chú |
|---|---|---|
| Actor và workflow đã rõ chưa? | Yes | Actor cụ thể (0–6 tháng), workflow 6 bước đã vẽ rõ |
| Baseline và success metric đã đo được chưa? | Not Yet | Có baseline ngành (Mỹ) nhưng chưa có baseline riêng cho thị trường VN; mục tiêu ≥80% là số tự đặt, cần pilot xác nhận |
| Có data/input đủ dùng chưa? | Not Yet | Có SDK pose estimation sẵn (QuickPose/MediaPipe) nhưng chưa có bộ "form chuẩn" cho từng bài tập do nhóm tự xây/kiểm chứng |
| Nếu AI sai, hậu quả có chấp nhận được không? | Not Yet | Cần boundary + cảnh báo fallback rõ ràng trước khi chấp nhận rủi ro AI chấm sai khiến người dùng chủ quan |
| Có người review/owner vận hành không? | Not Yet | Cần tìm 1 PT sẵn sàng cộng tác review định kỳ — hiện chưa có |
| Có cách non-AI đơn giản hơn không? | Yes | Thuê PT — nhưng đây chính là rào cản (chi phí + lịch) mà bài toán đang muốn giải, nên AI là phương án bổ sung chứ không thay thế hoàn toàn PT |
 
Decision:
 
```text
Not Yet
```
 
Lý do:
 
```text
Bài toán có bằng chứng thị trường mạnh và đã được chứng minh khả thi về kỹ thuật
(Gymscore, QuickPose, các dự án mã nguồn mở), nhưng nhóm còn 3 giả định quan
trọng chưa validate: (1) pain có đúng với người mới tập tại VN không — mọi khảo
sát hiện có đều lấy mẫu ở Mỹ, (2) độ chính xác thực tế của Workflow khi nhóm tự
build với dữ liệu ít, (3) ai sẽ là người thật review chất lượng phản hồi AI.
Go ngay khi chưa trả lời 3 câu này sẽ khiến success metric (≥80%) chỉ là số
mong muốn, không phải cam kết có cơ sở.
```
 
Nếu Not Yet, cần validate gì trước:
 
```text
1. Chạy Option A (2-3 interview thật với người mới tập gym tại VN) để xác nhận
   pain xảy ra đúng bối cảnh địa phương, không chỉ đúng ở mẫu Mỹ.
2. Build 1 prototype Workflow rút gọn (1 bài tập — squat, dùng SDK có sẵn) để
   tự đo độ chính xác thật, trước khi cam kết con số ≥80%.
3. Tìm 1 PT sẵn sàng cộng tác đóng vai "người thật kiểm tra" cho pilot.
```
 
Nếu No-Go, nên làm gì thay AI:
 
```text
Nếu sau khi validate mà pain không đủ mạnh tại VN hoặc không tìm được PT
cộng tác, phương án non-AI là: làm một checklist form chuẩn dạng poster/infographic
dán tại các trạm tập phổ biến (squat rack, bench), kèm QR code dẫn tới video
hướng dẫn ngắn — chi phí thấp, không cần AI, giải quyết một phần bước 1-3
của workflow dù không thay được phản hồi tức thời ở bước 4-5.
```
 
---