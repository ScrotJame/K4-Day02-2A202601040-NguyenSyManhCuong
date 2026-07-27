# Pilot Scorecard — Bodyweight Squat MVP

## 1. Thông tin phiên thử

| Field | Giá trị |
|---|---|
| Participant ID | |
| Experience level | |
| Device | |
| Camera view | |
| Lighting | |
| Distance | |
| Consent recorded | Yes / No |
| Pain/injury exclusion checked | Yes / No |

## 2. Camera setup

| Metric | Kết quả |
|---|---:|
| Setup thành công không cần hỗ trợ | Yes / No |
| Số lần đặt lại camera | |
| Thời gian setup | |
| Full-body visibility pass | Yes / No |

## 3. Pose và rep detection

| Metric | Kết quả |
|---|---:|
| Tổng frame | |
| Frame hợp lệ | |
| Pose coverage | |
| Rep theo HLV | |
| Rep hệ thống nhận | |
| Rep detection error | |
| Median latency | |

## 4. Form-label evaluation

Điền một dòng cho mỗi label.

| Label | TP | FP | TN | FN | Precision | Recall | F1 |
|---|---:|---:|---:|---:|---:|---:|---:|
| | | | | | | | |

## 5. Safety gate

| Metric | Kết quả |
|---|---:|
| Low-confidence cases | |
| Hệ thống abstain đúng | |
| Confident wrong feedback | |
| `cannot_assess` theo HLV | |
| `cannot_assess` theo app | |

## 6. User feedback

| Câu hỏi | Điểm 1–5 / ghi chú |
|---|---|
| Dễ đặt camera | |
| Hiểu feedback | |
| Feedback đến đúng lúc | |
| Tin tưởng đúng mức | |
| Sẵn sàng dùng lại | |
| Privacy concern | |

## 7. Decision cho session

- [ ] Đạt điều kiện tiếp tục.
- [ ] Cần sửa camera setup.
- [ ] Cần sửa label/rule/model.
- [ ] Cần sửa cue/UX.
- [ ] Dừng pilot vì safety/privacy concern.

**Ghi chú:**
