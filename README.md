# 🏠 Room Rental - Website Cho Thuê Phòng Trọ

> Nền tảng đăng tin và tìm kiếm phòng trọ trực tuyến được xây dựng với Django

## 📋 Giới Thiệu

**Room Rental** là một ứng dụng web cho phép người dùng đăng tin cho thuê phòng trọ và tìm kiếm phòng trọ phù hợp. Hệ thống hỗ trợ nhiều loại tin đăng (Normal, VIP, Pro) với các tính năng quản lý ví điện tử để thanh toán phí đăng bài.

## ✨ Tính Năng Chính

### 👤 Quản Lý Người Dùng
- Đăng ký / Đăng nhập tài khoản
- Quản lý thông tin cá nhân (Profile)
- Đổi mật khẩu
- Phân quyền người dùng (User, Poster, Admin)

### 🏡 Quản Lý Bài Đăng Phòng Trọ
- Đăng tin cho thuê phòng với hình ảnh và video
- Phân loại tin đăng: **Normal**, **VIP**, **Pro**
- Chỉnh sửa / Xóa bài đăng
- Tìm kiếm phòng trọ
- Xem chi tiết bài đăng

### 💰 Hệ Thống Ví Điện Tử
- Quản lý số dư ví
- Thanh toán phí đăng bài theo loại tin:
  - Normal: 5,000 VNĐ
  - VIP: 7,000 VNĐ
  - Pro: 10,000 VNĐ
- Theo dõi lịch sử chi tiêu

### 📧 Liên Hệ
- Gửi email liên hệ hỗ trợ

## 🛠️ Công Nghệ Sử Dụng

| Công nghệ | Mô tả |
|-----------|-------|
| **Python 3.x** | Ngôn ngữ lập trình chính |
| **Django 5.0** | Framework web backend |
| **SQLite** | Cơ sở dữ liệu |
| **HTML/CSS/JS** | Giao diện frontend |
| **Bootstrap** | CSS Framework |

## 📁 Cấu Trúc Dự Án

```
Room_Rental/
├── CNM/
│   ├── manage.py              # Django management script
│   ├── db.sqlite3             # Database
│   ├── CNM/                   # Project settings
│   │   ├── settings.py
│   │   ├── urls.py
│   │   └── wsgi.py
│   ├── app/                   # Main application
│   │   ├── models.py          # Database models
│   │   ├── views.py           # Views/Controllers
│   │   ├── urls.py            # URL routing
│   │   ├── forms.py           # Form definitions
│   │   ├── admin.py           # Admin configuration
│   │   ├── templates/         # HTML templates
│   │   │   ├── base.html
│   │   │   ├── home.html
│   │   │   ├── login.html
│   │   │   ├── signup.html
│   │   │   ├── post.html
│   │   │   ├── post_detail.html
│   │   │   ├── addroom.html
│   │   │   └── ...
│   │   └── static/            # Static files (CSS, JS, images)
│   └── media/                 # User uploaded files
└── README.md
```

## 🗃️ Database Models

### CustomUser
Quản lý thông tin đăng nhập người dùng với các quyền:
- `is_staff` - Nhân viên
- `is_posters` - Quyền đăng bài
- `is_superuser` - Quản trị viên

### Profile
Thông tin cá nhân người dùng:
- Họ tên, Email, Số điện thoại
- Giới tính, Ảnh đại diện

### Posts
Bài đăng cho thuê phòng:
- Tiêu đề, Mô tả, Giá thuê
- Địa chỉ, Hình ảnh, Video
- Loại tin (Normal/VIP/Pro)

### Wallet
Ví điện tử người dùng:
- Số dư hiện tại
- Tổng chi tiêu

## 🚀 Cài Đặt & Chạy Dự Án

### Yêu Cầu
- Python 3.8+
- pip (Python package manager)

### Các Bước Cài Đặt

1. **Clone repository**
```bash
git clone <repository-url>
cd Room_Rental/CNM
```

2. **Tạo môi trường ảo (khuyến nghị)**
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# Linux/Mac
source venv/bin/activate
```

3. **Cài đặt dependencies**
```bash
pip install django pillow
```

4. **Chạy migrations**
```bash
python manage.py migrate
```

5. **Tạo tài khoản admin (tùy chọn)**
```bash
python manage.py createsuperuser
```

6. **Chạy server**
```bash
python manage.py runserver
```

7. **Truy cập ứng dụng**
- Website: http://127.0.0.1:8000
- Admin: http://127.0.0.1:8000/admin

## 📱 Các Trang Chính

| Route | Mô tả |
|-------|-------|
| `/` | Trang chủ |
| `/home/` | Trang chủ (đã đăng nhập) |
| `/login/` | Đăng nhập |
| `/signup/` | Đăng ký |
| `/room/` | Danh sách phòng trọ |
| `/post/<id>/` | Chi tiết bài đăng |
| `/addroom/` | Đăng tin mới |
| `/yourpost/` | Quản lý bài đăng của bạn |
| `/profile/` | Tạo hồ sơ cá nhân |
| `/information/` | Xem thông tin cá nhân |
| `/wallet/` | Quản lý ví |
| `/contact/` | Liên hệ |
| `/about/` | Giới thiệu |

## 📝 License

Dự án này được phát triển cho mục đích học tập.

---
⭐ Nếu thấy hữu ích, hãy cho project một star nhé!


