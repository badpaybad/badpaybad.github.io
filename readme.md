# Nguyễn Phan Du (@badpaybad) Blog & Profile

Trang blog cá nhân và hồ sơ năng lực chuyên sâu của **Nguyễn Phan Du** ([@badpaybad](https://github.com/badpaybad)), được xây dựng trên nền tảng **Hugo** với giao diện **Blowfish Theme**, hỗ trợ song ngữ (Tiếng Việt & English), tối ưu SEO và triển khai tự động qua **GitHub Pages (GitHub Actions)**.

🌐 **Website chính thức**: [https://badpaybad.github.io/](https://badpaybad.github.io/)

---

## 🚀 1. Hướng Dẫn Chạy Preview Localhost

Hệ thống đã tích hợp sẵn binary Hugo extended (`hugo_bin`) bên trong thư mục dự án, bạn không cần cài đặt thêm môi trường phức tạp.

### Cách 1: Chạy bằng dòng lệnh Terminal (Cơ bản)
Mở Terminal tại thư mục gốc của dự án và chạy:

```bash
# Chạy local server hiển thị cả bài viết nháp (draft: true)
./hugo_bin server -D

# Hoặc chỉ định cổng và IP cụ thể:
./hugo_bin server -D --bind 0.0.0.0 --port 1313
```

Sau khi server khởi động thành công, mở trình duyệt:
- 🇻🇳 **Bản Tiếng Việt (Mặc định)**: [http://localhost:1313/](http://localhost:1313/)
- 🇬🇧 **Bản English**: [http://localhost:1313/en/](http://localhost:1313/en/)

> **Tính năng Live Reload**: Khi bạn thêm/sửa file `.md` hoặc đổi cấu hình, trình duyệt sẽ tự động cập nhật ngay lập tức.

---

### Cách 2: Chạy qua VS Code Tasks (Tiện lợi - 1 Phím tắt)

Dự án có sẵn file [.vscode/tasks.json](.vscode/tasks.json) giúp bạn chạy server hoặc build mà không cần gõ lệnh thủ công.

#### File `tasks.json` có bắt buộc không?
- **Không bắt buộc**: Đây là file cấu hình tiện ích mở rộng dành riêng cho trình soạn thảo VS Code. Nếu không dùng file này, bạn vẫn có thể chạy toàn bộ dự án bình thường thông qua dòng lệnh Terminal ở **Cách 1**.
- **Lợi ích khi có `tasks.json`**: Tiết kiệm thời gian, cho phép kích hoạt server ngầm hoặc build thử nghiệm chỉ với 1 phím tắt.

#### Các tác vụ (Tasks) được cấu hình sẵn trong `tasks.json`:
1. **`Start Hugo Dev Server (Preview)`** *(Mặc định)*: Khởi động máy chủ xem trước `localhost:1313` hiển thị cả bài nháp (`-D`).
2. **`Build Hugo Site (Production)`**: Chạy lệnh `./hugo_bin --minify` để kiểm tra kết quả đóng gói trước khi đẩy lên GitHub.
3. **`Clean Build Artifacts`**: Dọn dẹp thư mục tạm `public/` và `resources/_gen/`.

#### Cách sử dụng VS Code Tasks:
- **Phím tắt nhanh**: Nhấn **`Ctrl + Shift + B`** (hoặc `Cmd + Shift + B` trên macOS) $\to$ Task **Start Hugo Dev Server** sẽ tự động chạy.
- **Chạy các task khác**: Vào menu **Terminal** $\to$ **Run Task...** $\to$ chọn tác vụ mong muốn.
- **Dừng server**: Vào menu **Terminal** $\to$ **Terminate Task...** $\to$ chọn task đang chạy để tắt server.

---

## 📁 2. Cấu Trúc Thư Mục & Quản Lý Nội Dung

```text
├── .vscode/
│   └── tasks.json            # Cấu hình tiện ích chạy nhanh trong VS Code (Ctrl+Shift+B)
├── config/_default/
│   └── hugo.toml             # Cấu hình chính: menu, tác giả, SEO, đa ngôn ngữ
├── content/                  # Thư mục chứa toàn bộ bài viết và nội dung
│   ├── _index.md             # Trang chủ hồ sơ năng lực (Tiếng Việt)
│   ├── _index.en.md          # Trang chủ hồ sơ năng lực (English)
│   ├── me.md                 # Trang giới thiệu Me? (Nội dung cá nhân)
│   ├── pc-ai-agentic/        # Chuyên mục: PC AI Agentic Workforce
│   ├── posts/                # Chuyên mục: Các bài viết Blog kỹ thuật
│   └── sharing/              # Chuyên mục: Chia sẻ kinh nghiệm, tài liệu
├── layouts/                  # Giao diện tùy biến đè lên theme (Layout Overrides)
│   ├── 404.html              # Trang báo lỗi 404
│   ├── _default/
│   │   ├── rss.xml           # Cấu hình cấp phát tin RSS
│   │   └── sitemap.xml       # Sơ đồ trang web chuẩn SEO
│   └── partials/
│       ├── header/components/translations.html # Bộ chuyển đổi ngôn ngữ
│       ├── home/profile.html # Bố cục trang chủ căn trái (Left-aligned)
│       ├── recent-articles/  # Fallback bài viết mặc định cho tiếng Anh
│       └── schema.html       # Cấu trúc dữ liệu JSON-LD cho Google & AI Search
├── static/                   # Tài nguyên tĩnh (ảnh, icon, favicon, .nojekyll)
├── .github/workflows/
│   └── hugo.yml              # Quy trình CI/CD tự động build & deploy lên GitHub Pages
├── .nojekyll                 # Vô hiệu hóa trình build Jekyll mặc định của GitHub
└── hugo_bin                  # File thực thi Hugo Extended (Linux x64)
```

---

## ✍️ 3. Hướng Dẫn Thêm Bài Viết Mới

### Tạo bài viết Tiếng Việt:
Tạo một file `.md` mới trong thư mục tương ứng (ví dụ: `content/posts/ten-bai-viet.md`):

```markdown
---
title: "Tiêu đề bài viết của bạn"
date: 2026-09-02T19:00:00+07:00
description: "Mô tả ngắn gọn nội dung bài viết hiển thị ở trang chủ"
draft: false
tags: ["AI", "Architecture", "CSharp"]
categories: ["pc-ai-agentic"]
---

Nội dung bài viết viết bằng định dạng Markdown ở đây...
```

### Tạo bản dịch Tiếng Anh:
Để thêm bản dịch tiếng Anh cho bài viết, tạo thêm file cùng tên có hậu tố `.en.md` (ví dụ `content/posts/ten-bai-viet.en.md`):

```markdown
---
title: "Title of your article in English"
date: 2026-09-02T19:00:00+07:00
description: "Brief summary in English"
draft: false
---

Content in English goes here...
```

> **Lưu ý về Fallback**: Nếu bài viết chưa có file `.en.md`, trang web tiếng Anh sẽ tự động lấy danh sách bài viết mặc định tiếng Việt để trang chủ không bị trống.

---

## 🌐 4. Quản Lý Song Ngữ (Multilingual)

- **Ngôn ngữ mặc định**: Tiếng Việt (`vi`) tại URL gốc `/`.
- **Ngôn ngữ phụ**: English (`en`) tại URL con `/en/`.
- **Chuyển đổi ngôn ngữ**: Nút chọn ngôn ngữ có sẵn ở thanh menu điều hướng trên cùng (cả giao diện máy tính và điện thoại).

---

## 🚢 5. Cấu Hình Triển Khai GitHub Pages (CI/CD)

Quy trình xuất bản website được tự động hóa hoàn toàn mỗi khi bạn `git push` lên branch `master`.

### ⚠️ Cấu hình bắt buộc trên GitHub (Chỉ cần làm 1 lần):
1. Truy cập vào repo trên GitHub: **Settings** $\to$ **Pages** (hoặc truy cập `https://github.com/badpaybad/badpaybad.github.io/settings/pages`).
2. Tại mục **Build and deployment**:
   - Ở ô **Source**, chọn: **GitHub Actions** *(thay vì "Deploy from a branch")*.
3. Mỗi khi bạn commit và push lên branch `master`, GitHub Actions sẽ tự động chạy file [.github/workflows/hugo.yml](.github/workflows/hugo.yml), build mã nguồn và xuất bản lên GitHub Pages trong vòng chưa đầy 1 phút.

---

## 🛠️ 6. Các Lệnh Thường Dùng (Cheatsheet)

| Thao tác | Câu lệnh Terminal | Phím tắt VS Code (tasks.json) |
| :--- | :--- | :--- |
| **Xem trước cục bộ** | `./hugo_bin server -D` | Nhấn `Ctrl + Shift + B` |
| **Chạy server cố định port** | `./hugo_bin server -D --port 1313 --bind 0.0.0.0` | — |
| **Kiểm tra build thử nghiệm** | `./hugo_bin --minify` | Menu `Terminal -> Run Task... -> Build Hugo Site` |
| **Dọn dẹp thư mục build** | `rm -rf public resources/_gen` | Menu `Terminal -> Run Task... -> Clean Build Artifacts` |
