# MVP Scope — AI Bodyweight Squat Form Check

## In scope

- Người trưởng thành 18+ tự khai là khỏe mạnh và không đau/chấn thương hiện tại.
- Bodyweight squat, không thanh tạ/tạ đơn.
- Một người trong khung hình.
- Một góc quay được HLV chọn cho từng nhóm lỗi.
- Ánh sáng đủ, toàn thân nhìn thấy rõ.
- Pose estimation, rep counting, phase detection.
- Tối đa 2–3 error labels có thể quan sát từ góc quay MVP.
- Confidence gate và camera retake.
- Cue ngắn cố định do HLV duyệt.

## Out of scope

- Back squat/front squat hoặc bài dùng tải ngoài.
- Chẩn đoán đau, chấn thương hay bệnh lý.
- Rehabilitation/physical therapy.
- Tư vấn mức tạ, volume, lịch tập hoặc dinh dưỡng.
- Trẻ vị thành niên, người mang thai hoặc người có chỉ định y tế đặc biệt.
- Nhiều người trong khung hình.
- Mọi góc quay, mọi ánh sáng, mọi thiết bị.
- Cam kết phòng tránh chấn thương.

## Safety messages bắt buộc

- Công cụ chỉ hỗ trợ phản hồi kỹ thuật trong phạm vi thử nghiệm.
- Dừng tập nếu có đau, chóng mặt, khó thở bất thường hoặc cảm giác không an toàn.
- Không sử dụng kết quả thay cho đánh giá của HLV hoặc chuyên gia y tế.
- Khi app không đủ confidence, app phải nói “không thể đánh giá” thay vì đoán.

## Privacy defaults

- Ưu tiên inference on-device nếu khả thi.
- Không lưu video mặc định.
- Pilot chỉ lưu video khi người tham gia đồng ý rõ ràng.
- Mỗi file phải có participant ID ẩn danh, mục đích sử dụng và ngày xóa.
- Không dùng lại dữ liệu cho mục đích khác nếu chưa xin consent mới.
