# Trainer Labeling Guide — Bodyweight Squat Pilot

> Label schema cuối cùng phải được một HLV/domain expert xem và chốt. Tài liệu này là khung làm việc, không phải tiêu chuẩn y khoa.

## 1. Đơn vị gán nhãn

- Một sample chính là **một rep squat hoàn chỉnh**.
- Rep được đánh dấu: `valid_rep`, `incomplete_rep`, hoặc `cannot_assess`.
- `cannot_assess` dùng khi góc quay, che khuất hoặc chất lượng video không đủ.

## 2. Label đề xuất để HLV review

Chỉ giữ label mà HLV xác nhận có thể nhìn thấy đáng tin từ góc quay đã chọn.

| Label | Mô tả vận hành cần HLV chốt | Có thể dùng trong MVP? |
|---|---|---|
| `acceptable_within_scope` | Không thấy lỗi thuộc tập predefined trong video hợp lệ | Sau khi HLV chốt |
| `depth_out_of_target` | Độ sâu không nằm trong range HLV định nghĩa cho scope pilot | Cần góc quay phù hợp |
| `trunk_angle_out_of_target` | Góc thân vượt range HLV định nghĩa tại phase cụ thể | Cần side view |
| `knee_tracking_flag` | Pattern đầu gối cần chú ý theo definition của HLV | Có thể cần front/oblique view |
| `cannot_assess` | Không đủ visibility/confidence/góc quay | Bắt buộc |

Không dùng label chung chung `bad_form` vì không giải thích được lỗi và khó đánh giá.

## 3. Quy trình gán nhãn

1. HLV xem video không thấy output model.
2. Đánh dấu rep boundary.
3. Chọn `cannot_assess` nếu input không đủ.
4. Với rep hợp lệ, gán từng error label độc lập.
5. Ghi chú nguyên nhân khi không chắc.
6. Một tập con nên được người thứ hai review để đo agreement.

## 4. Evaluation

- Confusion matrix cho từng label.
- Precision, recall, F1 theo label.
- Recall đặc biệt quan trọng với lỗi nhóm coi là safety-relevant.
- Báo cáo tỷ lệ `cannot_assess` và low-confidence abstention.
- Tách kết quả theo người, thiết bị và góc quay.
- Không dùng frame accuracy để thay cho rep-level evaluation.

## 5. Cue mapping

Mỗi label chỉ map tới một cue đã được HLV duyệt. Cue cần:

- Ngắn, một ý mỗi lần.
- Không chẩn đoán nguyên nhân giải phẫu.
- Không yêu cầu tiếp tục tập khi người dùng báo đau.
- Có video/hình reference nếu lời nói dễ hiểu sai.
