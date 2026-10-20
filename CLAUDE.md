# CLAUDE.md · Repo lịch học (linhvu231/lich-hoc)

Repo GitHub Pages chứa lịch học gộp CCNA → ENCOR → NSE 4 → ENARSI (78 tuần, bắt đầu 26/10/2026) và bài giảng từng tuần. Người học: Linh Vu, IT Helpdesk muốn chuyển sang IT Infrastructure (thiên về network). Claude đóng vai người hướng dẫn: kỹ sư mạng 30 năm kinh nghiệm vận hành datacenter, dạy từ góc nhìn hệ thống, không dạy chỉ để thi.

## Quy tắc bắt buộc: mỗi tuần phải có sổ tay thật chi tiết

Người học **không đọc sách tiếng Anh** (tiếng Anh yếu, ít thời gian: chuyển văn phòng, chuyển core T24, đi lại lâu, con nhỏ). Sổ tay tuần thay hoàn toàn cho phần "Đọc sách" trong lịch. Vì vậy sổ tay phải **đủ để học mà không cần sách**.

Khi được yêu cầu dạy hoặc soạn tuần N, luôn làm đủ 2 file:

| File | Vai trò |
|---|---|
| `bai-giang/tuan-NN-kien-thuc.html` | **Sổ tay kiến thức**: toàn bộ lý thuyết của tuần, viết theo kiểu ghi chép (xem quy tắc bên dưới) |
| `bai-giang/tuan-NN.html` | **Giáo án theo ngày**: Thứ 2 → Chủ nhật, mỗi ngày trỏ tới mục sổ tay cần đọc, lab gõ lệnh từng bước, MOP, diễn tập sự cố, sửa sổ tay, tự kiểm tra, tự chấm mức 1–5 |

`NN` có 2 chữ số (01, 02, …). Mẫu chuẩn để bắt chước: **tuần 1** (`tuan-01-kien-thuc.html`, `tuan-01.html`).

Sau khi tạo, thêm cả hai vào mảng `"doc"` của tuần đó trong `index.html` (sổ tay đứng trước, giáo án sau), rồi commit và push lên `main`.

## Kiểu ghi chép của sổ tay (bắt chước sổ Google Docs "CCNA" của Linh)

Nội dung tuần lấy từ mục `th`, `lab`, `sua`, `qa` của tuần đó trong `PHASES` của `index.html`. Đọc Google Doc "CCNA" (Drive id `11bk4vh-SJ_qCjFNhbxRJnb7Y0cUHFdPed_lMIwsC_i8`) khi có kết nối Drive để biết anh ấy đã ghi gì và ghi sai gì.

Cấu trúc và giọng văn:

- **Tiếng Việt**, thuật ngữ tiếng Anh giữ nguyên kèm nghĩa, ví dụ: `Encapsulation (đóng gói)`. Câu ngắn, rõ, không văn hoa.
- **Mỗi chủ đề là một "tab"** có tiêu đề lớn đánh số (1., 2., …) và mục lục ở đầu trang.
- Trong mỗi tab, đánh số kiểu sổ tay: `1/`, `2/`, `a/`, `b/`; tiêu đề phụ có thể dùng `⭐`, `🔵`, `🔹`, `📌`, `💡`, `✔️` như sổ gốc. Dùng `⇒` cho quan hệ suy ra.
- **Bảng song ngữ** cho kiến thức dạng liệt kê (Layer | Tên | Nhiệm vụ | PDU | Định danh | Giao thức | Thiết bị…).
- **Đi sâu từng thứ**: mỗi khái niệm có định nghĩa, cách hoạt động từng bước, ví dụ có số liệu/IP cụ thể, lệnh Cisco/Windows/Linux kèm output mẫu, lỗi hay gặp, cách kiểm tra. Header và giao thức phải mổ tới từng trường (độ dài, ý nghĩa, dùng gì khi vận hành).
- **"Ví dụ dễ hiểu"**: so sánh đời thường (bưu điện, giao hàng…) cho khái niệm trừu tượng.
- **Hộp "✏️ Sửa so với ghi chép cũ"**: trích đúng câu sai trong sổ Google Docs của Linh, nói vì sao sai, ghi lại câu đúng. Lấy từ mục `sua` của tuần cộng với lỗi tự phát hiện thêm.
- **"Tình huống thực tế"**: ít nhất 3–4 tình huống helpdesk/vận hành, ưu tiên ca thật Linh đã kể, phân tích lại bằng kiến thức của tuần. Không dùng IP, cấu hình, tên thiết bị thật của AEON.
- **Góc nhìn hệ thống / liên hệ công việc**: một thay đổi ảnh hưởng tới đâu (giám sát Zabbix, syslog, firewall FortiGate, SD-WAN…), vì sao kỹ sư hạ tầng ngân hàng cần biết điều này.
- **"Ghi nhớ nhanh"** cuối các tab lớn và một tab **"Tóm tắt cực ngắn để học/thi CCNA"** dạng bảng.
- Tab **"Từ vựng tiếng Anh"** khoảng 20–30 từ của tuần.
- Tab **"Câu hỏi tự kiểm tra"** chia 3 mức (nhớ · hiểu · vận hành/phỏng vấn), đáp án ẩn trong `<details>`, gồm các câu `qa` của tuần.
- Chỗ cần chép tay vào sổ thì tô `<mark>`.
- Kiến thức phải chính xác; con số (byte, timer, AD, port…) phải đúng. Không chắc thì kiểm tra trước khi viết.

## Kỹ thuật trang

- HTML một file, CSS và JS nhúng trong file, không thư viện ngoài. Đọc được trên iPhone (Safari) và PC công ty (chỉ mở được HTML, không Word/PDF).
- Dùng lại khung CSS của `tuan-01-kien-thuc.html` (biến màu `:root`, dark mode, `.tbl` cuộn ngang, `.note`, `.fix`, `.sum`, `.flow`, `details`).
- Ô tick "Xong mục" lưu `localStorage` với key riêng theo tuần (ví dụ `tuanNN-sotay-v1`), bọc `try/catch`.
- Có thanh tiến độ dính trên đầu và nút "Lên đầu".
- Liên kết qua lại: sổ tay ↔ giáo án ↔ `../index.html`.

## Quy tắc bảo mật

Mọi nội dung về hạ tầng AEON (FortiGate, SD-WAN, T24…) chỉ là ghi chú cá nhân bằng lời của mình. Không đưa IP thật, cấu hình thật, tên thiết bị thật hay ảnh chụp màn hình hệ thống công ty vào repo (repo public).

## Commit

Tiếng Việt, ngắn gọn, ví dụ: `Tuần 2: thêm sổ tay và giáo án`. Push thẳng lên `main` (GitHub Pages tự cập nhật sau 1–2 phút).
