# 🎵 Trình Phát Âm Thanh - Dự Án NV8-STEM

Ứng dụng web trình phát âm thanh nhẹ nhàng, tích hợp giao diện **Light Glassmorphism** (kính mờ sáng hiện đại) cùng danh sách thành viên nhóm. Dự án được thiết kế tối ưu để đóng gói, mã hóa bảo vệ mã nguồn và triển khai nhanh chóng trên **GitHub Pages**.

---

## ✨ Tính năng nổi bật

- **Giao diện Light Glassmorphism:** Thiết kế hiện đại với hiệu ứng kính mờ tinh tế, bố cục trực quan chia làm 2 phần: Danh sách thành viên bên trái và Trình phát âm thanh trung tâm.
- **Tích hợp CSS trong JS:** Toàn bộ mã CSS được đóng gói tự động vào JavaScript, giúp giảm số lượng request và tối ưu hóa tệp tin.
- **Bảo mật mã nguồn (Obfuscation):** Tích hợp công cụ `javascript-obfuscator` trong quy trình build để mã hóa logic và giao diện trước khi xuất bản.
- **Tự động hóa đóng gói:** Chỉ cần một lệnh duy nhất để làm sạch, mã hóa và xuất bản toàn bộ tệp sẵn sàng triển khai vào thư mục `/dist`.

---

## 👥 Danh sách thành viên

1. **Bảo Khôi**
2. **Minh Đạt**
3. **Thanh Vân**
4. **Phương Anh**
5. **Hải Nguyên**
6. **Diễm Quỳnh**

---

## 📂 Cấu trúc thư mục

```text
NV8-STEM/
├── dist/                  # Thư mục chứa bản build hoàn chỉnh (được đẩy lên GitHub)
│   ├── index.html         # Tệp HTML chính đã tối ưu
│   ├── bundle.min.js      # Mã nguồn JS + CSS đã được mã hóa
│   └── all.mp3            # Tệp âm thanh nguồn
├── exec.html              # Mã nguồn HTML gốc (dùng để phát triển)
├── exec.js                # Mã nguồn JS gốc (tích hợp sẵn CSS Light Mode)
├── build.js               # Script tự động build và mã hóa mã nguồn
├── package.json           # Khai báo thư viện và thông tin dự án
├── .gitignore             # Cấu hình chỉ đẩy thư mục /dist lên Git
└── README.md              # Tài liệu hướng dẫn dự án
```

---

## 🚀 Hướng dẫn cài đặt & Sử dụng

### 1. Yêu cầu hệ thống
- Đã cài đặt [Node.js](https://nodejs.org/) (phiên bản 18 trở lên).
- Đã cài đặt [Git](https://git-scm.com/).

### 2. Cài đặt thư viện
Mở terminal tại thư mục gốc của dự án và chạy lệnh sau để cài đặt `javascript-obfuscator`:

```bash
npm install
```

### 3. Quy trình Build & Mã hóa
Mỗi khi bạn chỉnh sửa nội dung trong `exec.html`, `exec.js` hoặc thay thế file âm thanh `all.mp3`, hãy chạy lệnh sau để cập nhật bản build mới nhất vào thư mục `/dist`:

```bash
node build.js
```

### 4. Đẩy bản build lên GitHub
Nhờ cấu hình trong `.gitignore`, Git sẽ tự động bỏ qua mã nguồn thô và chỉ theo dõi các tệp trong thư mục `/dist`:

```bash
git add dist/
git commit -m "Cập nhật bản build mới"
git push
```

---

## 🌐 Triển khai lên GitHub Pages

1. Truy cập vào kho lưu trữ (Repository) của dự án trên GitHub.
2. Vào mục **Settings** $\rightarrow$ **Pages** ở thanh menu bên trái.
3. Tại phần **Build and deployment**:
   - **Source:** Chọn `Deploy from a branch`.
   - **Branch:** Chọn nhánh `main` (hoặc nhánh mặc định của bạn) và chọn thư mục gốc tương ứng.
4. Nhấn **Save** và chờ 1–2 phút để GitHub xuất bản trang web của bạn.

---

## 📄 Giấy phép

Dự án được phát hành theo giấy phép **Apache License 2.0** (chi tiết xem tại tệp `LICENSE`).