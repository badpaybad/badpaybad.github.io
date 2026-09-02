# Hồ sơ năng lực kỹ thuật: Nguyễn Phan Du (@badpaybad)

Tài liệu này tổng hợp phân tích từ toàn bộ **170+ repositories** trên GitHub [@badpaybad](https://github.com/badpaybad) (Arctic Code Vault Contributor) nhằm xây dựng bản Profile định vị năng lực chuyên sâu, tạo dựng niềm tin tuyệt đối cho đối tác, khách hàng và cộng đồng kỹ thuật.

---

## 1. Định vị Bản thân & Năng lực Cốt lõi (Core Identity)

- **Danh tính**: **Nguyễn Phan Du** (GitHub handle: `@badpaybad`).
- **Vị trí**: **Senior Software Architect | Foundation Infra Engineer | AI Agentic Specialist**.
- **Địa bàn hoạt động**: Hà Nội, Việt Nam & Remote toàn cầu.
- **Dấu ấn chuyên môn**:
  - **Hơn 10 năm kinh nghiệm** thực chiến xuyên suốt các tầng công nghệ: từ lập trình nhúng/Low-level C/C++ FFI, Firmware, Computer Vision, Robotics (ROS), đến kiến trúc Backend phân tán quy mô lớn (CQRS, DDD, Event Sourcing, Microservices trên .NET/Dart/Node.js/Python), và tiên phong xây dựng **AI Agentic Workforce** chạy trực tiếp trên PC/Local.
  - Tác giả của **170+ open-source repositories**, được GitHub vinh danh là **Arctic Code Vault Contributor**.

---

## 2. Các Dịch vụ & Mô hình Hợp tác Giá trị Cao (Value Propositions)

Profile không chỉ liệt kê danh sách mà tập trung giải quyết chính xác nỗi đau của đối tác:

### 🏗️ 1. Thiết kế Foundation Infra & Xây dựng Hệ thống Chịu tải cao
- **Bài toán của khách hàng**: Hệ thống phình to, nghẽn hiệu năng, mã nguồn lộn xộn, chi phí cloud tăng phi mã, khó mở rộng tính năng mới.
- **Giải pháp của tôi**:
  - Thiết kế kiến trúc nền tảng chuẩn mực: **CQRS (Command Query Responsibility Segregation), Domain-Driven Design (DDD), Event Sourcing, Asynchronous Message Broker (Redis/Kafka)**.
  - Xây dựng tầng Core Runtime siêu nhẹ (`mini-mvc`, Dart Server, .NET Core Serverless) giúp giảm 50–70% chi phí hạ tầng so với các giải pháp thông thường.
  - Xử lý bài toán hiệu năng tận gốc bằng Native C/C++ bindings (Dart FFI, P/Invoke, Shared Libraries `.so`/`.dll`).
- **Minh chứng thực tế**: `cqrs-dot-net-core`, `opendotnet-ecommerce-platform`, `dart-run-as-httpserver-api-sse-ws`, `dotnetcore-message-buss-with-redis`.

### 🚀 2. Đồng hành Phát triển Sản phẩm (Product Co-founding / Technical Partner)
- **Bài toán của đối tác**: Cần đưa sản phẩm từ ý tưởng ra thị trường (Zero to One) nhanh nhất có thể, nhưng thiếu một Technical Lead bao quát được từ hạ tầng, backend, mobile đến AI.
- **Giải pháp của tôi**:
  - Đảm nhiệm vai trò kiến trúc sư và dẫn dắt kỹ thuật toàn diện (Full-stack Product Lead).
  - Tốc độ bàn giao MVP thần tốc bằng quy trình **AI-Accelerated Development**, đưa sản phẩm lên production trong vài tuần thay vì nhiều tháng.
  - Đảm bảo sản phẩm có nền móng vững chắc, không phải đập đi xây lại khi lượng người dùng tăng đột biến.

### 🤖 3. Tư vấn & Triển khai Giải pháp AI Agentic Workforce Thực chiến
- **Bài toán của doanh nghiệp**: Muốn ứng dụng AI để tăng năng suất nhưng chi phí token quá đắt, lo ngại bảo mật dữ liệu khi gửi lên Cloud, hoặc các giải pháp AI chung chung không giải quyết được việc.
- **Giải pháp của tôi**:
  - **PC AI Agentic Workforce (Local-first)**: Xây dựng hệ thống trợ lý AI tự động hóa vận hành ngay trên máy tính cá nhân/máy trạm, giao tiếp qua Telegram/Webhook riêng tư mà không cần thuê server cloud.
  - **Khung kỹ năng tối ưu Token (Skill Harness & Rules Engine)**: Thiết kế kỹ năng chuyên biệt theo từng bài toán/dự án, kích hoạt sức mạnh tối đa của AI IDE với lượng token tiêu thụ tối thiểu.
  - **Chạy LLM cục bộ (On-device & CPU LLM)**: Triển khai các mô hình ngôn ngữ lớn (llama.cpp, Vistral LLM, Ollama) tối ưu chạy mượt mà ngay trên CPU máy tính phục vụ trích xuất thực thể, xử lý dữ liệu nhạy cảm an toàn 100%.
- **Minh chứng thực tế**: `a.i-assistant-chatbot-telegram-serverles`, `Ner_Llm_Gpt`.

### 🌐 4. Cố vấn Kỹ thuật & Mạng lưới Chuyên gia (Technical Advisory & Network)
- Cố vấn kiến trúc công nghệ, thẩm định kỹ thuật (Tech Due Diligence) cho các dự án khởi nghiệp.
- Kết nối, chia sẻ và hợp tác cùng các kỹ sư tài năng trong cộng đồng.

---

## 3. Bản đồ Kỹ thuật & Dự án Thực chiến (Proof of Work)

| Lĩnh vực | Dự án minh chứng | Công nghệ chủ đạo | Giá trị giải quyết |
| :--- | :--- | :--- | :--- |
| **AI Agentic & Local LLM** | `a.i-assistant-chatbot-telegram-serverles`<br>`Ner_Llm_Gpt` | Node.js, Telegram Bot, llama.cpp, C++, Vistral | Trợ lý AI cá nhân trên PC, trích xuất thực thể tự động trên CPU không tốn server |
| **Native Interop & Vision** | `flutter-dart-ffi-dlib-opencv`<br>`rplayer`<br>`dlib-android` | C/C++, Dart FFI, OpenCV, dlib, RTSP | Xử lý hình ảnh, video stream độ trễ cực thấp không qua MethodChannel chậm chạp |
| **Enterprise Backend & Infra** | `cqrs-dot-net-core`<br>`opendotnet-ecommerce-platform`<br>`dart-run-as-httpserver-api-sse-ws` | C#, .NET Core, Dart, Redis PubSub, WebSockets | Kiến trúc CQRS/DDD chịu tải cao, Realtime SSE/WS, Message Queue phân tán |
| **Computer Vision & AI/ML** | `InsightFace_TF`<br>`pixel_link`<br>`OcrTesseract`<br>`darknet` | Python, TensorFlow, C, YOLOv4, Tesseract | Nhận diện khuôn mặt 2D/3D, phân đoạn phát hiện văn bản, phát hiện vật thể |
| **Robotics & IoT/Edge** | `ros_navigation_command_app`<br>`ros_nodes`<br>`rplidaropencv`<br>`jetson-nano-image` | ROS, Dart, C++, Jetson Nano, Lidar | Điều khiển robot tự hành bằng giọng nói, vẽ bản đồ Lidar, tối ưu Ubuntu cho Jetson |

---

## 4. Tối ưu SEO & AI Search Engine (Google, Perplexity, Claude, ChatGPT)

- **Semantic Content Structure**: Cung cấp đầy đủ ngữ cảnh để các Search Engine và LLM AI bot trích xuất chính xác hồ sơ năng lực của Nguyễn Phan Du khi người dùng tìm kiếm chuyên gia hệ thống, FFI, Dart/Flutter hay AI Agentic.
- **Schema.org Structured Data**: Cấu hình `Person`, `ProfilePage`, `WebSite` với `knowsAbout`, `sameAs`, `jobTitle`.
- **Chế độ Draft**: Cài đặt `draft: true` để bạn tự do kiểm tra và tinh chỉnh câu chữ trên máy cục bộ trước khi xuất bản.
