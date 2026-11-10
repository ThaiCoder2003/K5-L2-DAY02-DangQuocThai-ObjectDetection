# Báo cáo cá nhân — Ngày 2 Object Detection

Đổi tên file theo `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md`. Điền kết quả thật, xóa dòng hướng dẫn khi nộp. Xem [quy định nộp](../../SUBMISSION.md).

## 1. Thông tin học viên

- Họ tên: Đặng Quốc Thái
- MSSV: 2A202603166
- Email: 26ai.thaidq@vinuni.edu.vn
- Lớp: C401
- Link repo bài làm: https://github.com/ThaiCoder2003/K5-L2-DAY02-DangQuocThai-ObjectDetection
- Link Colab đã chạy: https://colab.research.google.com/github/ThaiCoder2003/K5-L2-DAY02-DangQuocThai-ObjectDetection/blob/main/notebooks/day2_annotation_to_yolo.ipynb

## 2. Schema và mini guideline

Dẫn tới [GUIDELINE_MINI.md](../../GUIDELINE_MINI.md). Tóm tắt ba ca mơ hồ đã quyết định, cách áp dụng schema và phần cần giảng viên làm rõ.

## 3. Annotation và self-QC

- Số file nhãn train: 50
- Kết quả checker và lỗi đã xử lý: Không có lỗi checker
- Danh sách ít nhất 10 ảnh đã rà bằng mắt: drive_001, drive_004, drive_010, drive_013
- Lỗi bỏ sót/box/class phát hiện khi rà và cách sửa: Xác định nhầm 
- Commit khóa nhãn ban đầu: 9169aef47837f0cda67b57234e0a8c15f45731fb

## 4. Gold QC và rework

| Chỉ số | Trước sửa | Sau sửa nếu có |
|---|---:|---:|
| TP | 438 | |
| FP | 460 | |
| FN | 215 | |
| Precision | 0.4878 | |
| Recall | 0.6708 | |
| F1 | 0.5648 | |
| mean_iou_of_matches | 08548 | |
| passed | false | |

Dẫn tới `outputs/annotation_evaluation.json` trong repo. Nếu rework, ghi ảnh, lỗi đã kiểm, quyết định sửa/giữ và lý do. Không suy nguyên nhân chỉ từ FP/FN. Không có rework thì ghi rõ.

Không có rework
## 5. Kết quả YOLO

- Runtime, GPU/CPU, phiên bản Ultralytics và Torch:
- Các tham số thay đổi so với notebook nếu có và lý do:
- Đường dẫn best checkpoint trong phiên chạy:

| Chỉ số trên 10 ảnh eval | Giá trị |
|---|---:|
| Precision | 0.916 |
| Recall | 0.307 |
| mAP50 | 0.274 |
| mAP50–95 | 0.201 |

Đặt cả 2 folder `assets/eval_predictions/` và `assets/yolo26_runs/` (giải nén từ `day2_colab_outputs.zip`) cạnh báo cáo và dẫn link tương đối. Không chỉ ghi số; chỉ ra ít nhất một ảnh và vật thể cụ thể.

Trả lời bốn câu hỏi cuối notebook:

1. Lớp nào recall thấp nhất? Ảnh nào minh họa?
2. Nếu mAP50 cao nhưng mAP50–95 thấp, cần kiểm điều gì trên box?
3. Lỗi class nào có thể liên quan guideline? Dữ kiện nào hỗ trợ nhận xét?
4. Vì sao không dùng 10 ảnh eval để train? Vai trò validation của chúng trong notebook là gì?

## 6. Khó khăn và cách xử lý

| Bước/thời điểm | Lỗi quan sát | Cách đã thử | Kết quả/còn thiếu |
|---|---|---|---|
| 2 | Label khó các vị trí Van hay Car | Hỏi các bạn trong lớp/Nhờ công cụ AI phân tích | Đã sửa được hầu hết các label sai |

## 7. Tự đánh giá theo rubric

Đối chiếu [RUBRIC.md](../../RUBRIC.md): phần nào đã có kết quả, phần nào còn thiếu hoặc chưa kiểm được. Không tự nhận hoàn thành bước chưa chạy.

## 8. Công cụ AI và tài liệu tham khảo

Ghi công cụ đã dùng, dùng ở bước nào và phần đã tự kiểm tra; không dùng thì ghi rõ. Liệt kê nguồn ngoài repo được sử dụng. Không ghi mật khẩu/token hoặc đính kèm gold train.

Dùng AI ChatGPT ở các bước 1 (Hỗ trợ viết Guideline) và bước 6 (hỗ trợ phân tích các câu hỏi trong Notebook)
