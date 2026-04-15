# Kế hoạch triển khai Blog cá nhân Hugo cho badpaybad.github.io

Dựa trên các yêu cầu chi tiết trong `yeucau.md`, tôi đề xuất kế hoạch nâng cấp Blog như sau:

## 1. Công nghệ & Giao diện (Theme)
- **Framework**: **Hugo** (đảm bảo tốc độ và tính linh hoạt).
- **Theme**: **Blowfish** (Thiết kế sáng, sạch sẽ, hỗ trợ tốt hiển thị hình ảnh và mô tả bài viết ngay trên trang chủ).
- **Deployment**: **GitHub Actions** (Tự động build và deploy từ branch `master` lên GitHub Pages).

## 2. Cấu trúc Menu & Trang Web
Tôi sẽ thiết lập hệ thống menu linh hoạt theo thư mục như sau:

- **Trang Home**: Hiển thị danh sách **10 bài viết mới nhất** theo thứ tự thời gian giảm dần. Mỗi bài bao gồm: Tiêu đề, Ngày đăng, Ảnh đại diện (nếu có), và đoạn trích mô tả (Description).
- **Menu "Blogs"**: Trang tổng hợp toàn bộ bài viết, có phân trang (Pagination) **10 bài mỗi trang**.
- **Menu "Me?"**: Nội dung sẽ được chuyển từ file `index.html` hiện tại sang trang giới thiệu trong Hugo để giữ nguyên thông tin cá nhân.
- **Menu Thư mục (Categories)**: Tự động tạo menu dựa trên cấu trúc folder trong thư mục `content/`. Ví dụ:
  - `content/pc-ai-agentic/` -> Menu "PC AI Agentic"
  - `content/sharing/` -> Menu "Sharing"

## 3. Quy trình thực hiện (Workflow)
1. **Khởi tạo Hugo**: Dọn dẹp các file cũ và khởi tạo cấu trúc Hugo mới.
2. **Cấu hình `hugo.toml`**: Thiết lập menu, phân trang (pagination size = 10), và các thông số SEO.
3. **Chuyển đổi dữ liệu**: Di chuyển nội dung từ `index.html` cũ sang trang "Me?".
4. **Thiết lập CI/CD**: Tạo file `.github/workflows/hugo.yml` để tự động hóa việc xuất bản blog mỗi khi commit lên branch `master`.
5. **Kiểm tra**: Tạo bài đăng mẫu để đảm bảo mọi thứ hoạt động đúng như yêu cầu.

## 4. Cam kết kết quả
- Trang web sẽ cực kỳ nhẹ và nhanh.
- Giao diện chuyên nghiệp, hiện đại, phù hợp với chủ đề Công nghệ/AI.
- Bạn chỉ cần thêm file `.md` vào thư mục tương ứng, hệ thống sẽ tự động cập nhật.

---
**Tôi sẽ bắt đầu triển khai ngay khi bạn xác nhận "OK" hoặc có thêm góp ý.**
