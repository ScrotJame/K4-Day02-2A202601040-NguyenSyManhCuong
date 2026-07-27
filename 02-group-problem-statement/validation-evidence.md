# Validation Evidence

## 1. Evidence log hiện có

| Ngày | Nguồn | Quan sát | Ý nghĩa | Giới hạn |
|---|---|---|---|---|
| 24–27/07/2026 | Thảo luận nhóm 4 người | Nhóm chọn app AI check form tập là problem lớn nhất muốn phát triển | Có sự đồng thuận nội bộ về hướng sản phẩm | Nhóm xây sản phẩm không thay thế user research |
| Trước Day 02 | Prototype của một thành viên | Đã từng xây hệ thống check form bằng model tự train; dữ liệu nhiều và đa dạng giúp cải thiện model | Feasibility kỹ thuật ban đầu; nhóm có kinh nghiệm liên quan | Không có benchmark, dataset card hay trainer-labeled test set được dùng trong bài này |
| 27/07/2026 | Research về injury risk | Kỹ thuật tập không đúng được liệt kê là một risk factor của sports injury | Problem có relevance về an toàn | Chấn thương đa yếu tố; không thể claim app sẽ ngăn chấn thương |
| 27/07/2026 | Research về pose correction | Có các hệ thống nghiên cứu dùng pose estimation để phân tích/correct exercise | Hướng kỹ thuật khả thi | Nghiên cứu cũng cho thấy RGB pose có giới hạn ở bài phức tạp và môi trường thực tế |

## 2. Tín hiệu xác nhận

- Người mới là actor cụ thể và có workflow tập một mình quan sát được.
- Feedback form là vấn đề cần hiểu chuyển động, phù hợp với computer vision hơn chatbot.
- Nhóm có kinh nghiệm prototype ban đầu.
- Pose landmark models và các hệ thống pose correction đã tồn tại, nên không phải ý tưởng kỹ thuật vô căn cứ.
- Scope một exercise cho phép xây dataset, label schema và evaluation rõ.

## 3. Tín hiệu phản bác / điều chưa chắc

- Chưa phỏng vấn người mới để biết họ có thật sự muốn dùng camera hay không.
- Chưa biết họ đang giải quyết bằng gương, bạn tập, TikTok/YouTube hay HLV hiệu quả tới đâu.
- Chưa có HLV xác nhận lỗi nào có thể đánh giá đáng tin cậy từ một camera.
- Chưa có benchmark theo hình thể, quần áo, ánh sáng và góc quay khác nhau.
- Một camera 2D không quan sát đầy đủ mọi sai lệch 3D.
- Feedback sai có thể tạo rủi ro mới; vì vậy accuracy trung bình là chưa đủ, cần confidence/abstention.

## 4. Problem thay đổi sau validation

**Trước:** “Xây AI chỉnh form cho mọi người tập gym để tránh chấn thương.”

**Sau:**

> “Kiểm tra liệu một AI Workflow dùng camera có thể hỗ trợ người trưởng thành mới tập nhận feedback đáng tin cậy về một tập lỗi bodyweight squat đã định nghĩa trước, trong điều kiện quay kiểm soát, mà không đưa ra chẩn đoán hoặc thay thế HLV.”

Thay đổi quan trọng:

- Không claim “tránh chấn thương”.
- Không hỗ trợ mọi bài tập.
- Không dùng cho rehab hoặc người đang đau.
- Bắt buộc HLV gán nhãn và confidence gate.
- Pilot đo kỹ thuật và usability trước khi mở rộng.

## 5. Quick validation cần thực hiện trong lab/pilot

### Interview 5 người mới

Dùng `pilot/user-interview-guide.md`, tập trung vào lần gần nhất họ không chắc form, workaround hiện tại và willingness to use camera.

### Review với 1 HLV/domain expert

- Chốt definition của một rep hợp lệ.
- Chọn 2–3 lỗi có thể quan sát từ góc quay MVP.
- Loại lỗi không thể kết luận đáng tin từ một camera.
- Duyệt cue và stop conditions.

### Dataset/evaluation nhỏ

- Thu video có consent.
- Tách train/validation/test theo người, tránh frame của cùng một người xuất hiện ở cả train và test.
- Báo cáo confusion matrix, precision, recall, F1 cho từng label.
- Báo cáo pose failure/abstention riêng, không loại bỏ âm thầm.

## 6. Bằng chứng cần ghi cho mỗi pilot session

- Người dùng setup thành công sau bao nhiêu lần.
- Thiết bị, góc quay, ánh sáng và khoảng cách.
- Số frame/rep hợp lệ và bị từ chối.
- Nhãn HLV và output hệ thống.
- Confidence, latency và feedback hiển thị.
- Người dùng có hiểu đúng cue không.
- Có discomfort/pain report không; nếu có, dừng session và không dùng app để chẩn đoán.
