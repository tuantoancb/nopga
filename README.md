NỘP GIÁO ÁN ONLINE V4.2

ĐÃ CẤU HÌNH SẴN:
- Google OAuth Client ID đã được gắn trong config.js.
- Domain dùng cho OAuth: https://nopga.vercel.app
- Giáo viên không cần nhập Client ID.

TRƯỚC KHI THỬ ĐĂNG NHẬP:
1. Google Auth Platform hiện đang ở Test mode.
2. Hãy thêm tài khoản Google muốn thử vào danh sách Test users.
3. Đảm bảo Authorized JavaScript origin của OAuth Client có:
   https://nopga.vercel.app
4. Google Drive API và Google Sheets API phải ở trạng thái Enabled.

CÁCH DEPLOY:
- Upload index.html
- Upload config.js
- Upload vercel.json
- Commit / Redeploy trên Vercel.

CÁCH DÙNG:
- Mở https://nopga.vercel.app
- ⚙ Nơi lưu > nhập link Google Sheet + link thư mục Google Drive
- Đăng nhập Google
- Chọn 1 trong 3 hồ sơ
- Nhập bài dạy
- Chọn file Word
- Bấm Nộp giáo án
