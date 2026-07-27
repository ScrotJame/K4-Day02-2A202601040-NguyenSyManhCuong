| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---|---|---|---|---|
|1| User Pain Points| Người học thiếu động lực, nhanh chán, khó duy trì thói quen, dẫn đến việc học bị gián đoạn | User | Mất động lực sau vài ngày hoặc vài tuần |
|2| User Pain Points |Sinh viên khi cần làm giấy tờ để nộp, bị phân tán thông tin. Không biết khi nào giấy hoành thành để lên nhận | User | Không biết khi nào đi lấy, đến thì hết giờ làm để nhận giấy|
|3|User Pain Points|Tư vấn viên không thể theo dõi và chăm sóc hiệu quả số lượng lớn khách hàng tiềm năng|Tư vấn viên|Lead bị bỏ quên; quên gọi lại; khách chuyển sang đối thủ; tỷ lệ chuyển đổi thấp|
|4|Time-consuming|Mất nhiều thời gian tổng hợp thông tin khách hàng từ nhiều kênh|Tư vấn viên|Phải mở nhiều ứng dụng để tìm lịch sử trao đổi; nhập liệu lặp lại; mất 10–20 phút để chuẩn bị trước mỗi cuộc gọi|
|5|AI Advantage|Khó xác định khách hàng nào có khả năng mua cao để ưu tiên chăm sóc|Tư vấn viên, Trưởng nhóm|Gọi khách theo cảm tính; nhiều khách tiềm năng bị bỏ lỡ; tỷ lệ chốt không ổn định|
|6|Time-consuming|Việc viết báo cáo và cập nhật CRM sau mỗi cuộc gọi chiếm nhiều thời gian|Tư vấn viên|Cuối ngày mới nhập dữ liệu; ghi chú thiếu; CRM không phản ánh đúng trạng thái khách hàng|
|7|AI Advantage|Khó cá nhân hóa nội dung tư vấn theo nhu cầu và khả năng tài chính của từng khách|Tư vấn viên, Khách hàng|Gửi cùng một nội dung cho mọi khách; đề xuất dự án không phù hợp; khách ít tương tác |
|8|Time-consuming|Mất nhiều thời gian tìm kiếm tài liệu dự án|Tư vấn viên|Hỏi đồng nghiệp liên tục; gửi nhầm phiên bản tài liệu; mất thời gian tìm file trong nhiều nhóm chat |

## Top 3
|Rank|	Problem|	Vì sao chọn|	Điều còn chưa chắc|
|---|---|---|---|
|1	|Tư vấn viên bất động sản khó cá nhân hóa nội dung tư vấn theo nhu cầu và khả năng tài chính của từng khách hàng |	Actor rõ, workflow rõ, AI tạo giá trị lớn (RAG + LLM + Agent), dễ so sánh No AI/Rule/Workflow/Agent |	Cần dữ liệu dự án, bảng giá, hồ sơ khách hàng để demo|
|2	|Sinh viên không biết trạng thái xử lý hồ sơ/giấy tờ và khi nào có thể đến nhậnnhận|	Quy trình hành chính rõ ràng, pain point phổ biến, dễ đo thời gian và số lượt hỏi |	Cần giả lập dữ liệu trạng thái hồ sơ nếu trường chưa có API |
|3	|Người học không duy trì được thói quen học từ vựng |	Đúng pain point, có thể làm AI Coach, dữ liệu dễ tạo |	Khó chứng minh hiệu quả trong thời gian ngắn; dễ bị đánh giá là chatbot thông thường nếu thiếu điểm khác biệt|

## Problem Card #1       

Problem 1 câu

Tư vấn viên mất nhiều thời gian để cá nhân hóa nội dung tư vấn cho từng khách hàng.

Actor

Tư vấn viên bất động sản

Thời điểm

Khi tiếp nhận khách hàng mới hoặc khách hỏi về dự án.
Current workflow
Nhận thông tin khách hàng.
Hỏi nhu cầu (khu vực, ngân sách...).
Tìm dự án phù hợp.
Viết nội dung tư vấn.
Gửi khách hàng.

Bottleneck

Tìm thông tin dự án và viết nội dung phù hợp.

Impact

Phản hồi chậm.
Đề xuất chưa sát nhu cầu.
Tỷ lệ chuyển đổi thấp.

Success metric

Thời gian chuẩn bị <5 phút.
Tăng tỷ lệ phản hồi.
Tăng tỷ lệ đặt lịch xem nhà.

Non-AI Alternative

Template.
Checklist.

AI hypothesis

AI đọc nhu cầu → tìm dự án phù hợp → sinh nội dung tư vấn → gợi ý sản phẩm.

Quick gut

☑ Agent
**Draft Workflow**

```text
Lead
→ Nhập nhu cầu
→ AI phân tích
   ── ngân sách
   ── vị trí
   ── mục đích mua
→ Tìm dự án phù hợp
→ Sinh nội dung tư vấn
→ Sales duyệt
→ Gửi khách
```
## Problem Card #2 

Problem

Sinh viên không biết hồ sơ đang ở trạng thái nào và khi nào nên đến nhận.

Actor

Sinh viên

Current workflow

Nộp giấy tờ.
Chờ xử lý.
Liên hệ phòng đào tạo.
Đến nhận.

Bottleneck

Không có nơi tra cứu trạng thái.

Impact

Đi lại nhiều lần.
Hỏi nhiều.
Tốn thời gian.

Success metric

Giảm lượt hỏi.
Giảm số lần đi nhận thất bại.

Non-AI Alternative

Website tra cứu.

AI hypothesis

AI Agent tra cứu trạng thái, trả lời câu hỏi và gửi thông báo khi hoàn thành.

Quick gut

☑ Workflow  ☑ Agent

**Draft Workflow**
```text
Sinh viên
→Hỏi chatbot
→AI tra trạng thái
→Đã xong?
   ├── Có → Báo thời gian nhận
   └── Chưa → Báo trạng thái hiện tại
```

## Problem Card #3  

Problem

Người học không duy trì được thói quen học từ vựng.

Actor

Người học ngoại ngữ.

Workflow

Mở app.
Học từ.
Quên.
Bỏ vài ngày.
Quay lại.

Bottleneck

Thiếu động lực và nội dung chưa phù hợp.

Impact

Hiệu quả học thấp.
Tốn thời gian.

Success metric

Streak học tăng.
Tỷ lệ hoàn thành bài học tăng.
Tỷ lệ quay lại ứng dụng tăng.

Non-AI Alternative

Flashcard.
Nhắc lịch.

AI hypothesis

AI Coach cá nhân hóa nội dung, nhắc học và tạo hội thoại theo trình độ.

Quick gut

☑ Agent
