# Di sản Việt Nam 3D

Trang web tham quan trực tuyến 15 di tích – danh lam thắng cảnh của Việt Nam (mô hình 3D đơn giản + thông tin lịch sử + đố vui).
Toàn bộ nằm trong **một file** `index.html`; mở trực tiếp bằng trình duyệt (cần Internet để tải three.js, phông chữ và ảnh).

## Các trang

| Trang | Nội dung |
|---|---|
| Địa điểm · Bản đồ · Dòng thời gian | Chọn nơi cần xem theo danh sách, vị trí, hoặc mốc thời gian |
| Tham quan 3D | Xoay / zoom mô hình, bấm số trên mô hình để xem từng di tích nhỏ; nút **Nội dung** (lịch sử sơ bộ, mốc thời gian) và **Xem thêm** (liên kết Wikipedia, UNESCO, báo chí) |
| Đố vui | Đố vui 66 câu, có chế độ “ôn lại những gì đã xem”, giải thích đáp án và liên kết quay lại nơi chứa đáp án |
| Liên kết | Bảng điền link thông tin (cả địa danh), nội dung mô tả (di tích nhỏ) và ảnh; nút tải bản index.html đã gắn sẵn những gì đã điền |

## Chỉnh sửa dữ liệu (trong `index.html`)

* `SITES` – địa điểm và các điểm nhỏ (`spots`): tên, mô tả, mốc năm, vị trí máy quay, `link`.
* `INFO` – phần **Nội dung** (`p`, `tl`, `v`), danh sách **Xem thêm** (`more`), tên bài Wikipedia để lấy ảnh (`wp`, `sp`).
* `QUIZ` – câu hỏi: `[địa điểm, số thứ tự điểm nhỏ (-1: phần Nội dung), câu hỏi, 4 đáp án, vị trí đáp án đúng (0–3), giải thích]`.
* `LINKS` – link điền thêm (khóa `id-địa-điểm` hoặc `id-địa-điểm.số-điểm`); trang Liên kết có nút sao chép sẵn khối này.
* `TEXTS` – mô tả của từng di tích nhỏ (sửa ở trang Liên kết rồi dùng nút “Tải bản index.html…” để ghi vào đây).
* `IMGS` – ảnh điền tay (trang Liên kết cũng cho chọn file ảnh từ máy, lưu trong trình duyệt) (ưu tiên hơn ảnh tự tìm), ví dụ `'den-hung.2':'https://…/anh.jpg'`.
* `EDIT` – đặt `false` khi đưa cho người xem để ẩn ô nhập link, bảng quản lý và mục Liên kết.

## Ảnh thật

Ảnh được tự tìm từ Wikipedia / Wikimedia Commons **khi trang được mở có Internet** (kết quả lưu trong trình duyệt). Mỗi ảnh có ghi nguồn và liên kết giấy phép.
Ảnh từ bài Wikipedia là ảnh đại diện của bài; điểm nhỏ nào không có bài riêng được tìm trên Commons theo tên (có nhãn “ảnh tự tìm”, nên kiểm tra lại). Khi cần chắc chắn, điền ảnh vào `IMGS`.
Ảnh sẽ không hiện nếu môi trường hiển thị chặn truy cập tới `*.wikipedia.org` / `*.wikimedia.org` – khi đó trang vẫn hoạt động bình thường, chỉ không có ảnh.

## Ghi chú

* Mô hình 3D chỉ mang tính minh họa; thông tin được tổng hợp từ nguồn công khai, cần đối chiếu khi dùng cho mục đích học thuật.
* Tiến độ tham quan, điểm đố vui, giao diện sáng/tối, link, ảnh và nội dung đã sửa được lưu trong `localStorage` của trình duyệt đang dùng.
