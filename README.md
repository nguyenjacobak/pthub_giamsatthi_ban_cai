<p align="center"><img src="logo.png" width="96" alt="PTExam"></p>

# PTExam - Bản cài đặt

Nơi phát hành file cài của **PTExam**, phần mềm giám sát thi trên máy tính (chỉ chứa file cài, không chứa mã nguồn).

**Tải bản mới nhất:** mục [Releases](https://github.com/nguyenjacobak/pthub_giamsatthi_ban_cai/releases/latest)

| File | Cài lên |
|---|---|
| `GiamSatThi-GiamThi_<phiên bản>_amd64.deb` | Máy giám thị |
| `GiamSatThi-ThiSinh_<phiên bản>_amd64.deb` | Từng máy thí sinh |

Yêu cầu: Ubuntu 24.04 trở lên hoặc Linux Mint 22 trở lên (Ubuntu 22.04 trở về trước không chạy được).

## Tự cập nhật

Từ bản 2.1.0, hai app tự kiểm tra bản mới mỗi ngày. Có bản mới thì app hiện nút **Cập nhật**
(app thí sinh: ở màn hình đăng nhập; app giám thị: ở thanh bên trái). Bấm nút, nhập mật khẩu máy là xong, app tự mở lại.
Không cập nhật trong giờ thi. Máy đang dùng bản 2.0.x cần cài tay bản 2.1.0 một lần.

## Cách cài

1. Tải file `.deb` đúng loại máy ở mục Releases.
2. Bấm đúp file `.deb` → **Install** (nhập mật khẩu máy nếu được hỏi).
   Nếu App Center báo "bên thứ ba" và không cho cài: mở Terminal ở thư mục chứa file và chạy
   `sudo apt install ./<tên file>.deb`
3. **Máy thí sinh:** cài xong **đăng xuất rồi đăng nhập lại máy một lần** (hoặc khởi động lại) để Ubuntu bật tiện ích giám sát.
4. Mở app trong menu ứng dụng: "PTExam Giám thị" / "PTExam Thí sinh".

## Sử dụng

- **Giám thị:** mở app → "Mở phòng thi trên máy này" → tạo tài khoản quản trị (lần đầu) → Kỳ thi → Tạo kỳ thi mới → nhập thí sinh → Giám sát trực tiếp. Bấm "Dừng thi cho tất cả" để kết thúc: app trên mọi máy thí sinh tự đóng.
- **Thí sinh:** mở app → app tự tìm máy giám thị trong cùng mạng → nhập số báo danh và mật khẩu → chụp mặt. Trong giờ thi thí sinh không tự thoát app được.

## Máy thí sinh không tìm thấy phòng thi

- Bản cài của máy giám thị tự mở tường lửa (máy hỏi mật khẩu lần đầu). Nếu vẫn không thấy, chạy trên máy giám thị:
  `sudo ufw allow 47900/udp` và `sudo ufw allow 8000:8020/tcp`
- Một số router chặn dò tìm giữa wifi và mạng dây: ở máy thí sinh bấm "Đổi" và nhập địa chỉ hiện ở góc dưới bên trái dashboard của giám thị (ví dụ `192.168.1.140:8003`).

## Mất điện / tắt máy giữa giờ thi

Bật lại máy → app tự mở và tiếp tục đúng bài thi cũ (thí sinh chụp mặt lại). Giám thị thấy rõ máy mất kết nối bao lâu.

---
© 2026 Công ty Cổ phần PTHub
