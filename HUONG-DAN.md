# Đưa lịch học lên màn hình iPhone như một app

Thư mục này gồm: index.html (lịch học đã chỉnh cho iPhone), apple-touch-icon.png, icon-192.png, icon-512.png, manifest.webmanifest.
Phải đưa CẢ 5 file lên web cùng một thư mục (không đổi tên).

## Bước 1: Đưa lên web bằng GitHub Pages (miễn phí)
1. Đăng nhập github.com → New repository → đặt tên, ví dụ `lich-hoc` → Create.
2. Add file → Upload files → kéo cả 5 file vào → Commit changes.
3. Settings → Pages → Source: "Deploy from a branch" → Branch: main, thư mục / (root) → Save.
4. Chờ 1–2 phút. Địa chỉ có dạng: https://<tên-github>.github.io/lich-hoc/
   (Repo public thì ai có link đều xem được lịch. Lịch không chứa dữ liệu nhạy cảm.)

## Bước 2: Thêm vào màn hình chính iPhone
1. Mở địa chỉ trên bằng Safari.
2. Nhấn nút Chia sẻ (hình vuông có mũi tên lên) ở thanh dưới.
3. Kéo xuống, chọn "Thêm vào Màn hình chính" → đặt tên "Lịch học" → Thêm.
4. Mở app từ icon mới: chạy toàn màn hình, không có thanh địa chỉ.

## Lưu ý
- Tiến độ tick lưu trong bộ nhớ của app trên iPhone. Tick trên iPhone không tự sang máy tính và ngược lại.
- Đừng xoá dữ liệu Safari / website, sẽ mất tiến độ.
- Icon app không hiện đúng: xoá icon, mở lại link bằng Safari và thêm lại.
- Cần đổi nội dung lịch: sửa index.html trên GitHub (hoặc tải bản mới lên đè), mở lại app là thấy.
