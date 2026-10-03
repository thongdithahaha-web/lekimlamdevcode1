HƯỚNG DẪN ĐƯA LÊN GITHUB PAGES (lekimlam.github.io)
=====================================================

Sau khi xong, bạn có các địa chỉ:
  lekimlam.github.io/              trang chọn nhanh 3 trang
  lekimlam.github.io/vuihoc/       trang Vuihoc.vn (+ mã QR)
  lekimlam.github.io/sachhayonline/
  lekimlam.github.io/hoclieuso/
  lekimlam.github.io/admin/        trang quản trị (đăng nhập)

BƯỚC 1 - GitHub
  1. Đăng nhập GitHub, tạo repository tên đúng là  lekimlam.github.io  (Public).
     (Nếu tên tài khoản GitHub khác, đổi thành  <tên-tài-khoản>.github.io)
  2. Add file -> Upload files: kéo TOÀN BỘ thư mục/ file trong gói này vào, bấm Commit.
  3. Settings -> Pages: chọn Deploy from a branch -> main -> / (root) -> Save. Đợi 1-2 phút.

BƯỚC 2 - Firebase (miễn phí) để admin lưu và đồng bộ trực tiếp
  1. Vào console.firebase.google.com -> Add project (tắt Google Analytics cũng được).
  2. Build -> Realtime Database -> Create database (chọn Singapore) -> Start in locked mode.
  3. Tab Rules: dán nội dung file firebase-rules.json -> Publish.
  4. Build -> Authentication -> Get started -> Sign-in method -> Email/Password -> Enable.
  5. Tab Users -> Add user:  Email  lekimlam@lekimlam.com   Mật khẩu: (mật khẩu bạn chọn)
  6. Project settings (bánh răng) -> General -> copy "Web API Key".
     Realtime Database -> copy đường link ở đầu trang (dạng https://....firebasedatabase.app).
  7. Mở file config.js trên GitHub (biểu tượng bút), điền apiKey và dbUrl, Commit.

BƯỚC 3 - Dùng
  Vào lekimlam.github.io/admin -> đăng nhập tài khoản lekimlam -> sửa nội dung/ link -> Lưu.
  Các trang đang mở cập nhật ngay, mã QR đổi theo đường link mới.

LƯU Ý: Mật khẩu nằm ở Firebase (không nằm trong code), chỉ tài khoản đã đăng nhập mới ghi được dữ liệu.
Mã QR in ra nên trỏ tới lekimlam.github.io/vuihoc/ ... hoặc thẳng tới website đích (đổi trong admin).
