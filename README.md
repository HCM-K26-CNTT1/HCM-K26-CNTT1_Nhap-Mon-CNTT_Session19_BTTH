# BÀI TẬP TỔNG HỢP: RÀ SOÁT AN TOÀN THÔNG TIN DỰ ÁN SMARTCAMPUS

## PHẦN 1 – NHẬN DIỆN RỦI RO VÀ XỬ LÝ SỰ CỐ

### 1. Tình huống 1: Email giả mạo GitHub

- Loại tấn công: Phishing kết hợp Typosquatting.
- Dấu hiệu giả mạo:
  - Đường dẫn `githuh-security.com` giả mạo tên miền GitHub bằng cách thay chữ `b` thành `h`.
  - Email yêu cầu người dùng bấm vào liên kết và nhập lại mật khẩu để mở khóa tài khoản.
  - Tên miền không phải trang chính thức của GitHub.

Cách xử lý: Không nhấn vào liên kết, không nhập mật khẩu và báo cáo email đáng ngờ.

### 2. Tình huống 2: Phần mềm Crack Adobe Photoshop

- Loại cạm bẫy: Mã độc Crack (Malware Crack).
- Dấu hiệu nguy hiểm: Trang web yêu cầu tắt Windows Defender trước khi giải nén file.

Giải thích: Windows Defender có nhiệm vụ phát hiện và ngăn chặn mã độc. Việc tắt công cụ này khiến máy tính dễ bị virus, Trojan, spyware hoặc ransomware xâm nhập.

Cách xử lý: Không tải, không cài đặt và không chạy phần mềm Crack.

### 3. Áp dụng Quy tắc 5 KHÔNG

| Tình huống           | Quy tắc cần áp dụng                                                                                         |
| -------------------- | ----------------------------------------------------------------------------------------------------------- |
| Email giả mạo GitHub | Không nhấn vào liên kết lạ, không cung cấp mật khẩu hoặc thông tin cá nhân.                                 |
| Phần mềm Crack       | Không tải và cài đặt phần mềm không rõ nguồn gốc; không tắt phần mềm diệt virus theo yêu cầu của trang web. |

### 4. Quy trình Cấp cứu 4 Bước khi lỡ chạy file Crack

1. Ngắt kết nối mạng: Tắt Wi-Fi, rút dây mạng để hạn chế mã độc liên lạc với bên ngoài.
2. Cách ly thiết bị: Không tiếp tục sử dụng máy tính để đăng nhập tài khoản hoặc truy cập dữ liệu quan trọng.
3. Quét và xử lý mã độc: Bật Windows Defender, thực hiện quét toàn bộ (Full Scan) hoặc Microsoft Defender Offline Scan.
4. Khôi phục và bảo vệ tài khoản: Đổi mật khẩu từ một thiết bị sạch, thu hồi các phiên đăng nhập đáng ngờ và khôi phục dữ liệu từ bản sao lưu an toàn nếu cần.

## PHẦN 2 – CHUYỂN SANG PASSWORD MANAGER

### 1. Rủi ro khi dùng chung mật khẩu

Nếu email nhóm bị lộ mật khẩu, kẻ tấn công có thể dùng chính mật khẩu đó để đăng nhập vào GitHub và Vercel.

Đây là kiểu tấn công Credential Stuffing – sử dụng thông tin đăng nhập bị rò rỉ từ một dịch vụ để thử đăng nhập vào các dịch vụ khác.

Hậu quả:

- GitHub: Có thể bị đánh cắp mã nguồn dự án.
- Vercel: Có thể bị chiếm quyền triển khai và quản lý website.
- Email nhóm: Có thể bị sử dụng để tiếp tục chiếm các tài khoản khác.

### 2. Nguyên lý Zero-Knowledge Architecture

Zero-Knowledge Architecture là kiến trúc bảo mật trong đó nhà cung cấp dịch vụ không thể đọc được dữ liệu bí mật của người dùng.

Đối với Bitwarden:

- Dữ liệu được mã hóa trên thiết bị trước khi đồng bộ lên máy chủ.
- Khóa giải mã được bảo vệ bằng thông tin bí mật của người dùng.
- Máy chủ chỉ lưu trữ dữ liệu đã mã hóa.

Vì vậy: Ngay cả khi máy chủ Bitwarden bị hacker xâm nhập, hacker cũng khó đọc được mật khẩu nếu không có khóa giải mã của người dùng.

### 3. Cấu hình Password Generator

Sử dụng Bitwarden Password Generator để tạo 3 mật khẩu riêng biệt cho GitHub, Vercel và Email nhóm.

| Thông số         | Giá trị cấu hình |
| ---------------- | ---------------- |
| Độ dài           | 20 ký tự         |
| Chữ hoa (A–Z)    | Bật              |
| Chữ thường (a–z) | Bật              |
| Chữ số (0–9)     | Bật              |
| Ký tự đặc biệt   | Bật              |

Lưu ý: Mỗi tài khoản phải có một mật khẩu khác nhau. Không sử dụng lại mật khẩu cũ hoặc chia sẻ mật khẩu chung giữa các thành viên.

## PHẦN 3 – KÍCH HOẠT 2FA CHO TÀI KHOẢN GITHUB

### 1. Vì sao nên dùng Authenticator App thay cho SMS OTP?

Nên sử dụng Google Authenticator (TOTP) thay vì SMS OTP vì:

- Nhược điểm 1 – SIM Swapping: Kẻ xấu có thể giả mạo danh tính để chiếm quyền sử dụng SIM, từ đó nhận mã OTP.
- Nhược điểm 2 – Phụ thuộc mạng viễn thông: SMS OTP cần sóng điện thoại, có thể không nhận được mã khi đi nước ngoài hoặc ở nơi mất sóng.

Kết luận: Authenticator App tạo mã OTP trực tiếp trên điện thoại, không cần Internet hay SIM, giúp tăng khả năng bảo vệ tài khoản GitHub.

### 2. Các bước kích hoạt 2FA bằng Google Authenticator

Thực hiện trên tài khoản GitHub của từng thành viên.

Bước 1: Truy cập GitHub và đăng nhập tài khoản.

Bước 2: Nhấn ảnh đại diện góc trên bên phải → chọn Settings.

Bước 3: Chọn Password and authentication ở thanh menu bên trái.

Bước 4: Tìm mục Two-factor authentication → chọn Enable two-factor authentication.

Bước 5: Chọn phương thức Authenticator app.

Bước 6: Mở Google Authenticator trên điện thoại → nhấn dấu `+` → chọn Scan a QR code để quét mã QR trên GitHub.

Bước 7: Ứng dụng sẽ tạo mã OTP gồm 6 chữ số. Nhập mã này vào GitHub để xác nhận.

Bước 8: Lưu bộ 10 Backup Codes ở nơi an toàn và hoàn tất thiết lập.

### 3. Quản lý 10 mã khôi phục (Backup Codes)

Nơi NÊN lưu:

- Password Manager (Bitwarden) trong kho dữ liệu được mã hóa.
- Bản giấy được cất trong két sắt hoặc tủ khóa an toàn.

Nơi KHÔNG NÊN lưu:

- Ảnh chụp màn hình trong thư viện điện thoại.
- Tin nhắn Zalo, Messenger hoặc email.
- File README hoặc file công khai trên GitHub.

Lưu ý: Mỗi mã khôi phục chỉ sử dụng được một lần. Không chia sẻ mã này cho người khác.

## PHẦN 4 – BẢO VỆ SECRETS TRƯỚC KHI PUSH CODE

### 1. Xác định 2 giá trị Secrets bị hardcode

Trong file `config.js` ban đầu có 2 giá trị Secrets:

1. `API_KEY = "sk-proj-abc123456789"`: Khóa API dùng để xác thực khi truy cập dịch vụ.
2. `DB_PASSWORD = "SmartCampus@2026"`: Mật khẩu kết nối cơ sở dữ liệu.

Rủi ro: Nếu push lên GitHub Public, người khác có thể xem và sử dụng các thông tin này để truy cập trái phép.

### 2. Viết lại code sử dụng process.env

File: `config.js`

```
const API_KEY = process.env.API_KEY;
const DB_PASSWORD = process.env.DB_PASSWORD;

function connectDatabase() {
  return connect(DB_PASSWORD);
}
```

Code đã loại bỏ giá trị Secret trực tiếp và chuyển sang đọc biến môi trường thông qua `process.env`.

### 3. Tạo 3 file bảo mật

File 1: `.env`

Chứa giá trị Secret thật, chỉ lưu trên máy tính cá nhân và không push lên GitHub.

```
API_KEY=THAY_BANG_API_KEY_MOI
DB_PASSWORD=THAY_BANG_MAT_KHAU_MOI
```

Lưu ý: Đây là giá trị minh họa. Khi thực hiện, phải thay bằng API Key và mật khẩu mới được cấp hoặc tạo riêng. Không sử dụng lại các thông tin đã xuất hiện trong code ban đầu.

File 2: `.gitignore`

Đảm bảo Git bỏ qua file `.env`.

```
# Environment variables
.env
.env.*
!.env.example

# Dependencies
node_modules/

# Log files
*.log
```

File 3: `.env.example`

Chỉ chứa tên biến để các thành viên biết dự án cần những thông tin nào.

```
API_KEY
DB_PASSWORD
```



Kết quả

&#x20;Các thành viên có thể dựa vào `.env.example` để tự tạo file `.env` trên máy cá nhân mà không cần chia sẻ giá trị Secret thật.



### 4. Quy tắc 4 Bước Kiểm tra trước khi Push

Trước khi chạy `git push`, thực hiện 4 bước:

Bước 1: Kiểm tra mã nguồn

- Tìm kiếm API Key, mật khẩu và các thông tin nhạy cảm trong code.
- Đảm bảo không còn Secret bị hardcode.

Bước 2: Kiểm tra file `.gitignore`

- Đảm bảo đã thêm `.env` vào `.gitignore`.
- Kiểm tra Git có bỏ qua file `.env` hay không.

Lệnh kiểm tra:

```
git check-ignore -v .env
```

Bước 3: Kiểm tra các file chuẩn bị đưa lên Git

```
git status
```

Kiểm tra danh sách file được thêm, sửa hoặc xóa. Đảm bảo `.env` không xuất hiện trong danh sách file chuẩn bị commit.

Nếu đã đưa `.env` vào vùng theo dõi của Git trước đó, cần bỏ theo dõi bằng:

```
git rm --cached .env
```

Bước 4: Kiểm tra lần cuối và Push

```
git diff --cached
git add config.js .gitignore .env.example
git diff --cached
git commit -m "security: remove hardcoded secrets"
git push
```

Đảm bảo nội dung commit không chứa Secret thật trước khi push.

Lưu ý: Nếu Secret đã từng được push lên GitHub, chỉ xóa khỏi code là chưa đủ. Cần thu hồi hoặc thay mới API Key, mật khẩu và xử lý lịch sử Git nếu cần.

## KẾT LUẬN

Qua quá trình rà soát, dự án SmartCampus cần thực hiện các biện pháp sau trước khi bàn giao:

1. Nhận diện và tránh các cuộc tấn công Phishing, phần mềm Crack chứa mã độc.
2. Sử dụng Bitwarden để quản lý mật khẩu riêng biệt cho từng tài khoản.
3. Kích hoạt 2FA bằng Google Authenticator để tăng cường bảo mật GitHub.
4. Sử dụng `.env` và `.gitignore` để bảo vệ Secrets, tránh rò rỉ thông tin khi đưa mã nguồn lên GitHub Public.

Kết quả mong muốn: Mã nguồn SmartCampus được công khai an toàn, không chứa mật khẩu, API Key hoặc thông tin bí mật của dự án.
