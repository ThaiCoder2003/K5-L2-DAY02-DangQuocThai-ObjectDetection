# Mini guideline — bài làm cá nhân

> Điền nội dung này trước khi bắt đầu gán nhãn. Giữ lại các quyết định sau khi self-QC.

## Định nghĩa lớp

| Lớp | Định nghĩa của bạn | Ví dụ/điểm phân biệt |
| --- | --- | --- |
| `car` | Phương tiện giao thông cỡ vừa/nhỏ, dùng để chở 1 hay 1 số người | Xe sedan, xe hatchback |
| `truck` | Phương tiện giao thông thiết kế cho việc vận chuyển hàng hóa | Xe tải thùng, xe container, xe bán tải |
| `bus` | Phương tiện giao thông cỡ lớn để chở khối lượng lớn hành khách | Xe buýt công cộng, xe buýt trường học |
| `van` | Phương tiện giao thông có hình dạng gần giống hình hộp, có thể vận chuyển hàng hóa vừa/nhỏ hay vận chuyển khách | Xe minivan, van hàng hóa, van hành khách |

## Quy tắc chung

- Box bám sát vật thể nghĩa là: Bounding box phải được vẽ sát nhất có thể xung quanh vật thể, tránh không gian background không cần thiết
- Vật thể bị che khuất: Annotate phần thấy được. Nếu phần bị che có thể định dạng được, box có thể bao gồm cả phần bị che
- Vật thể bị cắt bởi rìa ảnh: Vẽ box đến rìa ảnh và không được mở rộng vượt quá hình ảnh
- Vật thể rất nhỏ/mơ hồ: Chỉ annotate nếu hình ảnh nhìn đủ rõ để phân lớp. Nếu không, để nó không annotate

## Ghi lại quyết định cho ít nhất ba ca mơ hồ

| Ảnh | Tình huống | Quyết định cuối | Lý do theo schema |
| --- | --- | --- | --- |
| `drive_016` | Xe ở phía trước không rõ là car hay van | van | Hình khối hộp có vẽ gần nhất với van |
| `drive_021` | Đuôi xe bị khuất không rõ car hay van | car | Dựa theo đầu xe và tính năng chở khách loại nhỏ |
| `drive_026` | Một chiếc xe trắng và xanh quá mờ không thể xác định rõ | Escalate sau | Các tính chất xe không rõ ràng |
