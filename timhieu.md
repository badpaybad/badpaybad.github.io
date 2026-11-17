# Hồ sơ năng lực kỹ thuật: Nguyễn Phan Du (@badpaybad)

Tài liệu này tổng hợp phân tích từ toàn bộ **170+ repositories** trên GitHub [@badpaybad](https://github.com/badpaybad) (Arctic Code Vault Contributor) cùng hệ sinh thái sản phẩm thương mại **[ToT Tech Ecosystem (`fossagentic.men`)](https://fossagentic.men/)** nhằm xây dựng bản Profile định vị năng lực chuyên sâu, tạo dựng niềm tin tuyệt đối cho đối tác, khách hàng và cộng đồng kỹ thuật.

---

## 0. Sản phẩm & Use Cases Thực chiến Đưa Lên Trên Cùng ([fossagentic.men](https://fossagentic.men/))

Dựa trên dự án thực tế tại `/work/a.i-foundation-boilerplate/landingpage`, phần đầu trang chủ (`content/_index.md` & `content/_index.en.md`) đặt trực tiếp **5 nhóm sản phẩm & Use Cases thương mại** lên trên cùng (trước phần Dịch vụ & Danh sách Repo) để đối tác thấy ngay năng lực triển khai từ phần cứng đến phần mềm:

1. **Kho RFID Tìm Đồ Không Quan Tâm Vị Trí (`https://fossagentic.men/#warehouse-rfid`)**: Súng UHF **Chainway SR160** (Impinj Gen2X, 865–928 MHz, Dual-Mode RFID + Barcode, BLE 5.0 / HID / USB-C OTG) + thẻ Anti-Metal + App Mobile **Flutter `tot-hub`** (Menu bán nguyệt 1 tay, SSO OIDC, đọc giọng nói Tiếng Việt miễn phí `flutter_tts` `vi-VN`, khử lỗi Telex Hex) + đồng bộ **Sapo POS** qua `.NET Core.Infra.WarehouseRfid` (`tracking_id`, Atomic Transfer). Video 4K demo: `https://fossagentic.men/videos/products/5.1.warehouse-rfid.webm`.
2. **A.I Agent Agentic Bán Hàng Đa Kênh (`https://fossagentic.men/#ai-sale-agent`)**: **Sales Cockpit 3 cột** (`https://app.fossagentic.men/workspaces/sale-agent/cockpit`, Webhook Facebook + Redis CQRS, 6 tab, Dual-Mode `AI_AUTO` <5s & `CO_PILOT`), PostgreSQL `pgvector` GraphRAG + Given-When-Then CoT, `Session Focus Product`, `Obsolete Guarding`, đồng bộ đơn **Sapo Multi-Store (`#DUNP`)**, và động cơ kéo Fanpage **Level 1 → Level 10** (~80% AI / ~20% nhân viên, Daily Triad `08:00 AM`, Lookalike 1%–2% từ Sapo giảm 30%–60% CPA, tự học `02:00 AM`).
3. **Hệ Điều Hành Nhúng `ESP32-OS` & 6 Bộ Embedded Kits Độc Lập (`https://fossagentic.men/#embedded-kits`)**: Trên nền `ESP32-S3 N16R8`: (1) Nhân `ESP32-OS` FreeRTOS EventBus + Captive Portal `esp32os_dunp` + ECDSA P-256 + Firestore, (2) Module màn hình cảm ứng `ILI9341` 2.8" `XPT2046` dựng chữ Tiếng Việt UTF-8 trực tiếp, (3) Dual-Mic I2S `INMP441` 16kHz + TFLite Wake-Word + VAD 60s, (4) Audio DAC `MAX98357A` 24kHz + 256KB OPI PSRAM RingBuffer, (5) Đọc thẻ RFID & **CCCD gắn chip (`PN532` ICAO Doc 9303 BAC/3DES)** cho ki-ốt eKYC, (6) **Chatbot A.I `ESP32 Mic Phone`** đàm thoại Gemini 3.1 Flash Live (Aoede `vi-VN`), Smart Barge-In & 8 Function Tools.
4. **Foundation & Enterprise Boilerplate (`https://fossagentic.men/#services`)**: Bộ khung Clean Architecture / Modular Monolith (`.NET 10` `Core.Infra`, `Angular Standalone + Signals`, `Flutter Monorepo tot-hub`, Redis Pub/Sub, Firebase, Nghị định 13/2023/NĐ-CP) rút ngắn 80% thời gian khởi tạo, phản hồi `< 100ms`, bàn giao 100% mã nguồn (`https://github.com/badpaybad/a.i-foundation-boilerplate`).
5. **Hệ Máy CNC Tự Động Hóa & AI Computer Vision (`https://fossagentic.men/#products`)**: Máy **CNC Touch Machine** (4 trục GRBL 0.05mm, giảm chấn lò xo bảo vệ kính, test 1M+ lượt bấm, auto call, QA/QC), **CNC Wooden & Plotter** (TB6600 4.0A, GRBL-HAL 32-bit, Single-Line Vector) và **AI Computer Vision Anti-Spoofing** (60FPS, 99.8% liveness) — trình diễn qua 10 video thực tế tại `https://fossagentic.men/#products` (không bao gồm `1.robot.mp4` theo đúng spec tại `landingpage/whattodo.md`).

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

---

## 5. Trang Giới Thiệu A.I PC Agentic Workforce (`/pc-ai-agentic/` & `/vi/pc-ai-agentic/`)

Bổ sung theo `yeucau.md` (mục hoàn thiện `/pc-ai-agentic/` và chuyển mặc định sang Tiếng Anh):

- **Layout riêng không hiển thị `"no articles"`**: Tạo `layouts/pc-ai-agentic/list.html` căn trái F-pattern (`text-left text-start`, `max-w-4xl`), hiển thị sơ đồ `/img/PC-A.I-Agentic-workforce.png` (`width="1016"`, `height="706"`, `fetchpriority="high"`), hỗ trợ ToC dính bên phải và ẩn danh sách con khi các bài nhánh (`intro-to-ai.md`, `hardware-setup.md`) còn ở trạng thái `draft = true`.
- **Nội dung song ngữ Anh (mặc định) / Việt (`_index.md` & `_index.vi.md`)**:
  - **SaaS (60%–90%) vs. Forward Developer + AI (99%–100% < 1 tuần)**: Nhấn mạnh kinh nghiệm triển khai thực chiến dưới 1 tuần khi ngồi sát nghiệp vụ cùng khách hàng.
  - **Tiến hóa thành Harness Worker → A.I PC Agentic Workforce**: Giải thích dễ hiểu cách hướng dẫn người dùng tiếp tục trao đổi và lặp quy trình cùng AI qua thời gian (kèm sơ đồ `/img/ai-agentic-spec-driven.png`).
  - **Dễ hiểu, dễ tiếp cận cho người dùng phổ thông**: Đưa ví dụ giao việc 3 bước trực tiếp qua **Telegram**, **Facebook Messenger** ngay trên PC cá nhân lên trước, tách phần kiến trúc kỹ thuật (`Cloudflare Tunnel`, `Ollama`/`llama.cpp`/`Gemma 4`, `Skills/`, `.md` RAG) xuống mục riêng kèm FAQ tối ưu SEO/GEO.

---

## 6. Ngôn ngữ Mặc định Tiếng Anh (`/`) & Song ngữ Tiếng Việt (`/vi/`)

Cập nhật theo `yeucau.md` dòng cuối:

- **Đổi `defaultContentLanguage = "en"` trong `config/_default/hugo.toml`**: Truy cập trực tiếp `https://badpaybad.github.io/` và `https://badpaybad.github.io/pc-ai-agentic/` mặc định dùng Tiếng Anh (`weight = 1`), bản Tiếng Việt phục vụ tại `/vi/` và `/vi/pc-ai-agentic/` (`weight = 2`).
- **Tổ chức file nội dung song ngữ**: Chuyển cặp trang chủ thành `content/_index.md` (EN) + `content/_index.vi.md` (VI) và `content/pc-ai-agentic/_index.md` (EN) + `content/pc-ai-agentic/_index.vi.md` (VI), kèm `aliases` chuyển hướng `/en/` → `/` và `/en/pc-ai-agentic/` → `/pc-ai-agentic/`.
- **Giữ nguyên `content/me.md` & bài viết chưa dịch**: Không chỉnh sửa `content/me.md`; cập nhật `layouts/partials/header/components/translations.html` (dùng `site.Home.AllTranslations`), `layouts/partials/recent-articles/cardview.html` + `main.html` (`site.Sites.Default`) và menu `[languages.vi.menu.main]` trỏ đúng `/posts/`, `/me/`, `/sharing/` để không bị gãy link khi chuyển ngôn ngữ.
- **Trình bày khoa học, có hệ thống & nhấn mạnh tính sẵn sàng sử dụng** (theo dòng 42 `yeucau.md`): Bổ sung bảng tổng hợp **6 Hệ thống Sản phẩm Sẵn sàng Vận hành** ngay đầu trang chủ (`_index.md` / `_index.vi.md`), chuẩn hóa từng sản phẩm theo 4 phần đồng nhất (*System Readiness / Mức độ sẵn sàng*, *Problem Solved / Bài toán giải quyết*, *Practical Application / Ứng dụng thực tế*, *Core Architecture & Access*), và bổ sung bảng thành phần sẵn sàng + lộ trình triển khai `< 1 tuần` trong `/pc-ai-agentic/` & `/vi/pc-ai-agentic/`.
