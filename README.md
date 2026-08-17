# NỘP GIÁO ÁN ONLINE V4.0

## Chức năng
- Một app dùng chung cho nhiều người.
- Mỗi trình duyệt/người dùng tự cấu hình 1 Google Sheet + 1 thư mục Google Drive.
- 3 hồ sơ nhanh dùng chung nơi lưu đó.
- Đăng nhập Google bằng OAuth 2.0.
- Upload file Word thật vào Drive.
- Ghi dữ liệu thật vào Google Sheet.
- Không cần mở Google Form.

## Cấu hình Google Cloud (người quản trị app làm 1 lần)
1. Vào Google Cloud Console, tạo hoặc chọn Project.
2. Enable:
   - Google Drive API
   - Google Sheets API
3. Cấu hình OAuth consent screen.
4. Tạo OAuth Client ID loại **Web application**.
5. Thêm Authorized JavaScript origins:
   - URL Vercel production, ví dụ: https://ten-app.vercel.app
   - Có thể thêm http://localhost:3000 khi thử local.
6. Copy Client ID dạng `....apps.googleusercontent.com`.
7. Mở app > ⚙️ Nơi lưu > dán Client ID.
   Có thể dùng cùng Client ID cho tất cả người dùng của app.

## Mỗi người dùng làm 1 lần
1. Mở app.
2. ⚙️ Nơi lưu.
3. Nhập:
   - Link Google Sheet của mình.
   - Tên sheet/tab (mặc định: Câu trả lời biểu mẫu 1).
   - Link thư mục Google Drive của mình.
4. Lưu.
5. Đăng nhập Google.
6. Tạo 3 hồ sơ nhanh.
7. Chọn hồ sơ > nhập bài > chọn file Word > Nộp giáo án.

## Cột app ghi vào Sheet
A Dấu thời gian
B Họ và tên
C Môn/HĐGD
D Tổ chuyên môn
E Ngày/tháng/năm
F Tên bài học/chuyên đề/nội dung
G Lớp
H Số tiết
I Từ tiết đến tiết
J Link file giáo án
K Tên người duyệt
L Trạng thái = Chờ duyệt

Nếu Sheet thực tế có thứ tự cột khác, chỉnh mảng `row` trong hàm `submitLesson()` của index.html.

## Lưu ý OAuth
Nếu app dùng cho nhiều tài khoản bên ngoài tổ chức Google Workspace, Google có thể yêu cầu cấu hình/verification OAuth tùy loại tài khoản và phạm vi quyền.
