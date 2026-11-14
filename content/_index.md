---
title: "Nguyễn Phan Du (badpaybad) | Senior Software Architect & AI Agentic Specialist"
description: "Hồ sơ năng lực & Use Cases thực chiến của Nguyễn Phan Du (@badpaybad) - Founder ToT Tech Ecosystem (fossagentic.men), Senior Software Architect & AI Agentic Specialist. Từ Kho UHF RFID (tot-hub + Chainway SR160), AI Sales Agent, ESP32-OS, Foundation Boilerplate (.NET 10 / Angular / Flutter) đến CNC Automation & Native C/C++ FFI."
draft: false
---

Chào bạn! Tôi là **Nguyễn Phan Du** ([@badpaybad](https://github.com/badpaybad)), **Senior Software Architect, Foundation Infra Engineer & AI Agentic Specialist** tại Hà Nội, Việt Nam — đồng thời là Founder & Kiến trúc sư trưởng hệ sinh thái công nghệ **[ToT Tech Ecosystem (`fossagentic.men`)](https://fossagentic.men/)**.

Với hơn **10 năm kinh nghiệm thực chiến** xuyên suốt từ phần cứng nhúng, Native C/C++ FFI, hệ thống phân tán chịu tải cao đến **AI Agentic Workforce**, tác giả **170+ open-source repositories** và danh hiệu **Arctic Code Vault Contributor**, tôi trực tiếp thiết kế và bàn giao các sản phẩm phần mềm – phần cứng đầu-cuối đang vận hành thực tế cho doanh nghiệp và đối tác.

{{< button href="https://fossagentic.men/" target="_blank" rel="noopener noreferrer" >}}🌐 Khám phá Hệ sinh thái Sản phẩm tại fossagentic.men →{{< /button >}}

- **Cổng sản phẩm & Demo Video**: [https://fossagentic.men/](https://fossagentic.men/)
- **Live AI Sales Workspace**: [https://app.fossagentic.men/workspaces/sale-agent/cockpit](https://app.fossagentic.men/workspaces/sale-agent/cockpit)
- **Foundation Repo**: [github.com/badpaybad/a.i-foundation-boilerplate](https://github.com/badpaybad/a.i-foundation-boilerplate)

---

## 🚀 Sản phẩm & Use Cases Thực chiến ([fossagentic.men](https://fossagentic.men/))

{{< lead >}}
Các sản phẩm và hệ thống thực tế đã được nghiên cứu, đóng gói và triển khai trong hệ sinh thái ToT Tech Ecosystem — mỗi giải pháp giải quyết trực tiếp một bài toán vận hành cụ thể cho đối tác và doanh nghiệp.
{{< /lead >}}

### 1. [Kho RFID Tìm Đồ Không Quan Tâm Vị Trí (`Chainway SR160` + App Mobile Flutter `tot-hub`)](https://fossagentic.men/#warehouse-rfid)
- **Bài toán (Use Case)**: Kho thương mại điện tử, gia dụng và linh kiện có hàng nghìn mã SKU nhặt/trả liên tục — cách quy hoạch ô kệ cố định và soi mã vạch truyền thống dễ sai vị trí khi cao điểm và không tìm nhanh được hàng nằm khuất trong thùng carton.
- **Sản phẩm & Kiến trúc**: Súng đọc cầm tay **Chainway SR160** (chip Impinj E-Series Gen2X, chuẩn EPCglobal C1G2 / ISO 18000-6C, dải tần `865–928 MHz`, chế độ kép UHF RFID + Barcode 1D/2D, kết nối BLE 5.0 GATT MTU 247 + Bluetooth HID + USB Type-C OTG / Pogo-Pin) đi kèm thẻ cứng **Anti-Metal Hard Tag** và tem dẻo EPC; kết nối ứng dụng di động đa nền tảng **Flutter `tot-hub`** (Android/iOS, `shadcn_flutter`, Menu bán nguyệt xoay 1 tay, SSO OIDC) và đồng bộ trực tiếp trường `barcode` lên **Sapo POS** qua backend `.NET Core.Infra.WarehouseRfid` + CQRS `tracking_id`.
- **Giá trị thực tế**: Quét sóng UHF xuyên thùng hàng lọc giao cắt nhiều SKU/tên sản phẩm cùng lúc; phản hồi **giọng nói Tiếng Việt miễn phí (`flutter_tts` `vi-VN`)** (*khớp 1 món đọc tên hàng, ≥ 2 món đọc số lượng, 0 món báo "Không thấy"*) giúp nhân viên rảnh mắt di chuyển; tự động khử lỗi bộ gõ Telex biến đổi mã Hex (`DD→Đ`, `AA→Â`, `EE→Ê`); gán nhãn 1 chạm & chống trùng thẻ toàn kho với chuyển nhượng nguyên tử (Atomic Transfer).
- **Liên kết & Demo**: [Chi tiết giải pháp Kho RFID (`fossagentic.men/#warehouse-rfid`)](https://fossagentic.men/#warehouse-rfid) · [Video Demo thực tế 4K (`02:25`)](https://fossagentic.men/videos/products/5.1.warehouse-rfid.webm)

### 2. [A.I Agent Agentic Bán Hàng Đa Kênh — Sales Cockpit 3 Cột & Kéo Fanpage Level 10](https://fossagentic.men/#ai-sale-agent)
- **Bài toán (Use Case)**: Cửa hàng bán lẻ trên Facebook thường trực page chậm, sót comment/tin nhắn giờ cao điểm, tư vấn nhầm SKU hoặc chốt sai giá, và thiếu quy trình tự động hóa bài bản để đưa Fanpage đạt trạng thái đề xuất tự nhiên (*Recommendable*).
- **Sản phẩm & Kiến trúc**: Nền tảng **AI Sales Agent** kiến trúc Event-Driven CQRS (Webhook Facebook + Redis CQRS + Angular 19 + `.NET 10`) gồm **Sales Cockpit 3 cột** (6 tab: `Tất cả`, `Chờ xử lý`, `Cần tạo đơn`, `Messenger`, `Comment`, `Xử lý tin sót`) với **Dual-Mode** (`AI_AUTO` phản hồi `< 5 giây` 24/7 và `CO_PILOT` gợi ý `Duyệt & Gửi` / `Sửa` / `Sinh lại`); tri thức **PostgreSQL `pgvector` GraphRAG** + luật suy luận Given-When-Then Chain-of-Thought, `Session Focus Product`, `Obsolete Guarding` (chặn đơn 0đ hoặc hàng ngừng kinh doanh) và đồng bộ đơn **Sapo Multi-Store (`#DUNP`)** kèm chuẩn hóa địa chỉ Việt Nam trước/sau sáp nhập.
- **Giá trị thực tế**: Tự động chăm sóc, áp dụng Combo khuyến mãi và đồng bộ đơn hàng sang đa chi nhánh Sapo theo vòng khép kín *Hội thoại → Đơn hàng → Doanh thu → Giỏ hàng → Mua lặp lại*; kết hợp động cơ kéo Fanpage **Level 1 → Level 10** (~80% AI tự động / ~20% nhân viên) lập lịch `08:00 AM` Daily Triad (Google Trends + Zeigarnik copywriting + Bài ảnh + Story 9:16 + Reel 9:16 FFmpeg TTS Tiếng Việt), tạo tệp Lookalike 1%–2% từ dữ liệu Sapo (giảm 30%–60% CPA) và vòng tự học lúc `02:00 AM`.
- **Liên kết & Demo**: [Chi tiết AI Sales Agent (`fossagentic.men/#ai-sale-agent`)](https://fossagentic.men/#ai-sale-agent) · [Mở Live Workspace (`app.fossagentic.men`)](https://app.fossagentic.men/workspaces/sale-agent/cockpit)

### 3. [Hệ Điều Hành Nhúng `ESP32-OS` & 6 Bộ Embedded Kits Độc Lập (Touch, Audio, CCCD NFC, AI Mic Phone)](https://fossagentic.men/#embedded-kits)
- **Bài toán (Use Case)**: Doanh nghiệp cần triển khai thiết bị IoT công nghiệp, ki-ốt eKYC đọc căn cước công dân gắn chip, màn hình hiển thị Tiếng Việt hoặc thiết bị đàm thoại giọng nói AI độc lập mà không phải tự xử lý xung đột bus phần cứng hay kiến trúc đa luồng FreeRTOS.
- **6 sản phẩm phần cứng & firmware độc lập (nền `ESP32-S3 N16R8`, 16MB Flash / 8MB OPI PSRAM)**:
  1. **Nhân `ESP32-OS` & FreeRTOS EventBus**: Tách luồng Core 0 / Core 1 an toàn Mutex, Captive Portal (`esp32os_dunp`) lưu 5 mạng WiFi, xác thực bất đối xứng ECDSA P-256 & đồng bộ Firestore.
  2. **Module Màn Hình Cảm Ứng TFT Touch 2.8" Tiếng Việt UTF-8**: `ILI9341` 320×240 (SPI 40MHz) + `XPT2046`, dựng trực tiếp dấu Tiếng Việt Unicode UTF-8 (NFC/NFD) không cần nạp font bitmap nặng.
  3. **Module Thu Âm Số Kép Dual-Mic I2S `INMP441`**: 16kHz PCM, DSP khử DC-offset, tích hợp TFLite Micro Wake-Word (*"Du ơi"*) + VAD tự nghỉ sau 60s.
  4. **Module Âm Thanh Số I2S DAC `MAX98357A` 24kHz**: Chuẩn 24,000 Hz 16-bit khớp Gemini Live, bộ đệm vòng 256KB OPI PSRAM chống đứt tiếng + Self-Test loa/mic khi khởi động.
  5. **Thiết Bị Đọc Thẻ RFID & Căn Cước Công Dân Gắn Chip (`CCCD NFC PN532`)**: 13.56MHz chuẩn ISO/IEC 14443-4 & ICAO Doc 9303 (APDU BAC/3DES giải mã DG1, DG2 ảnh chân dung, DG13; bản vá bộ đệm FIFO 262B & UART 921600 baud) cho ki-ốt eKYC khách sạn, bệnh viện, ngân hàng.
  6. **Thiết Bị Chatbot A.I Đàm Thoại Giọng Nói — `ESP32 Mic Phone`**: Đàm thoại 2 chiều thời gian thực qua WebSocket với **Gemini 3.1 Flash Live** (giọng nữ Aoede `vi-VN`), Smart Barge-In ngắt lời thông minh & 8 Function Calling Tools.
- **Liên kết & Demo**: [Chi tiết Embedded Kits & ESP32-OS (`fossagentic.men/#embedded-kits`)](https://fossagentic.men/#embedded-kits) · [Video Gateway IoT](https://fossagentic.men/videos/products/3.iot.mp4) · [Video Bo mạch IoT công nghiệp](https://fossagentic.men/videos/products/3.1.iotthbb.mp4)

### 4. [Foundation & Enterprise Boilerplate (`.NET 10` + `Angular Standalone` + `Flutter Monorepo`)](https://fossagentic.men/#services)
- **Bài toán (Use Case)**: Đội ngũ kỹ thuật thường mất 3–6 tháng đầu chỉ để dựng hạ tầng nền tảng, SSO OIDC, CQRS, realtime SSE/WebSocket, đa ngôn ngữ i18n và chuẩn bảo vệ dữ liệu trước khi làm được tính năng nghiệp vụ đầu tiên.
- **Sản phẩm & Kiến trúc**: Bộ khung **Clean Architecture, Modular Monolith & Microservices** thực chiến (`a.i-foundation-boilerplate`): Backend **C# .NET 10** (`Core.Infra` NuGet packages, `BaseDbContext`, MediatR CQRS, Redis Cache & Pub/Sub, Firebase Auth/Firestore), Web **Angular Standalone + Signals** (Vite + AnalogJS, TailwindCSS v4, i18n 3 tầng), Mobile **Flutter Monorepo (`tot-hub`)** (`shadcn_flutter`, `foundations/tot-flutter`) và tuân thủ bảo vệ dữ liệu cá nhân theo **Nghị định 13/2023/NĐ-CP**.
- **Giá trị thực tế**: Rút ngắn **80% thời gian khởi tạo dự án**, độ trễ phản hồi `< 100ms`, bàn giao 100% mã nguồn bản quyền (zero vendor lock-in).
- **Liên kết & Demo**: [Dịch vụ Foundation Boilerplate (`fossagentic.men/#services`)](https://fossagentic.men/#services) · [Kiến trúc 4 tầng (`fossagentic.men/#architecture`)](https://fossagentic.men/#architecture) · [Công cụ dự toán (`fossagentic.men/#estimator`)](https://fossagentic.men/#estimator) · [Mã nguồn nền tảng (`GitHub`)](https://github.com/badpaybad/a.i-foundation-boilerplate)

### 5. [Hệ Máy CNC Tự Động Hóa (`CNC Touch`, `CNC Wooden & Plotter`) & `AI Vision Anti-Spoofing`](https://fossagentic.men/#products)
- **Bài toán (Use Case)**: Tự động hóa kiểm thử độ bền và độ trễ màn hình cảm ứng trên thiết bị thật (thay thế bấm tay thủ công), điều khiển gọi điện/thao tác ứng dụng di động từ xa, gia công gỗ/vẽ vector kỹ thuật và phát hiện giả mạo khuôn mặt thời gian thực.
- **Sản phẩm & Video thực nghiệm**:
  - **CNC Touch Machine**: Khung 4 trục GRBL độ chính xác `0.05mm`, đầu chạm cao su dẫn điện giảm chấn lò xo bảo vệ mặt kính, điều khiển qua Python API — [Auto Call](https://fossagentic.men/videos/products/2.3.cnc.touch.mobi.call.mp4), [Multi-Touch tốc độ cao](https://fossagentic.men/videos/products/3.2.cnc.touch.mp4), [Thử nghiệm độ bền 1M+ lượt bấm](https://fossagentic.men/videos/products/4.cnc.toch.mp4), [QA/QC Touch Bot](https://fossagentic.men/videos/products/4.1.cnctouch.mp4).
  - **CNC Wooden Machine & Plotter**: Máy phay khắc gỗ dùng driver công nghiệp **TB6600** (4.0A, vi bước 1/32) + mainboard 32-bit **GRBL-HAL**; máy vẽ kỹ thuật & nghệ thuật chuyển vector sang nét vẽ đơn liền mạch — [Single-Line Plotter](https://fossagentic.men/videos/products/4.3.cnc.drawing.mp4) & [Vector Art](https://fossagentic.men/videos/products/4.4.cnc.drawing.mp4).
  - **AI Computer Vision Anti-Spoofing**: Nhận diện khuôn mặt & kiểm tra liveness thời gian thực `60FPS` (`99.8%`) chống deepfake/ảnh giả — [Video Demo](https://fossagentic.men/videos/products/2.fake.face.mp4).
- **Liên kết & Demo**: [Thư viện 10 Video Thực Nghiệm tại `fossagentic.men/#products`](https://fossagentic.men/#products)

---

## 💎 Giải pháp Hợp tác & Năng lực Cốt lõi

{{< lead >}}
Không chỉ viết code, tôi mang đến giải pháp kiến trúc toàn diện từ gốc rễ: Vững nền tảng – Tối ưu hiệu năng – Tiết kiệm chi phí – Bứt phá tốc độ cùng AI.
{{< /lead >}}

### 🏗️ 1. Thiết kế Foundation Infra & Xây dựng Hệ thống Chịu tải cao
*Dành cho doanh nghiệp cần xây dựng nền móng phần mềm chuẩn mực hoặc tái cấu trúc hệ thống nghẽn hiệu năng.*
- **Kiến trúc doanh nghiệp chuẩn mực**: Chuyên sâu về **CQRS (Command Query Responsibility Segregation), Domain-Driven Design (DDD), Event Sourcing, Asynchronous Event Brokers (Redis, Message Queues)** và **Microservices**.
- **Tối ưu hóa hiệu năng tầng sâu**: Giải quyết bài toán tốc độ và bộ nhớ bằng cách kết hợp **Native C/C++ (Shared Libraries `.so`/`.dll`)** tương tác trực tiếp qua **Dart FFI / CLR Interop**, loại bỏ hoàn toàn độ trễ của các cầu nối truyền thống.
- **Hạ tầng Runtime tinh gọn**: Xây dựng backend server siêu nhẹ (Dart Server, .NET Core Serverless, Custom Micro-frameworks) giúp hệ thống phản hồi tính bằng mili-giây và cắt giảm đến 70% chi phí server cloud.

### 🚀 2. Đồng hành Phát triển Sản phẩm (Product Co-founding / Technical Partner)
*Dành cho Founder/Doanh nghiệp cần hiện thực hóa sản phẩm từ 0 đến 1 (Zero-to-One) với tốc độ kỷ lục.*
- **Bao quát toàn diện vòng đời sản phẩm**: Từ thiết kế kiến trúc hạ tầng, cơ sở dữ liệu, API Gateway, Real-time Communication (SSE, WebSockets, WebRTC) đến ứng dụng người dùng (Flutter Mobile/Desktop).
- **Tốc độ bàn giao thần tốc nhờ AI-first Workflow**: Tận dụng AI Agentic và các kỹ năng tinh chỉnh để rút ngắn tối đa thời gian phát triển MVP, đưa sản phẩm ra thị trường kiểm chứng chỉ trong vài tuần.
- **Tư duy sản phẩm bền vững**: Xây dựng sản phẩm có khả năng mở rộng (scalable) ngay từ ngày đầu, không phải đập đi làm lại khi lượng người dùng tăng trưởng đột biến.

### 🤖 3. Tư vấn & Triển khai Giải pháp AI Agentic Workforce Thực chiến
*Dành cho doanh nghiệp/đội ngũ muốn tự động hóa công việc bằng AI với chi phí thấp và an toàn dữ liệu.*
- **PC AI Agentic Workforce (Local-first, Không tốn Server)**: Xây dựng hệ thống Agentic tự động hóa làm việc 24/7 trực tiếp trên máy tính cá nhân/máy trạm của bạn, điều khiển linh hoạt qua Telegram Bot/Webhook mà không phát sinh chi phí thuê máy chủ cloud đắt đỏ.
- **Khung Kỹ năng & Tối ưu hóa Token (Skill Harness & Rules Engine)**: Thiết kế các bộ quy tắc (rules) và kỹ năng chuyên biệt theo từng dự án, biến AI IDE thành một "Super Full-stack Developer" có kỷ luật cao, giúp tiết kiệm tối đa ngân sách token tiêu thụ.
- **Chạy LLM Cục bộ (On-device & CPU-optimized LLMs)**: Triển khai các mô hình ngôn ngữ lớn (`llama.cpp`, `Vistral`, `Ollama`) tối ưu trực tiếp trên CPU, phục vụ nhận diện thực thể (NER), xử lý văn bản và tài liệu nội bộ bảo mật 100%.

### 🌐 4. Cố vấn Kỹ thuật & Mạng lưới Chuyên gia (Technical Advisory & Network)
*Dành cho đối tác cần thẩm định công nghệ hoặc các kỹ sư muốn kết nối chuyên môn.*
- Cố vấn chiến lược công nghệ, đánh giá kiến trúc (Tech Due Diligence) và tháo gỡ các nút thắt kỹ thuật hóc búa.
- Giao lưu, chia sẻ kinh nghiệm về hành trình tiến hóa mã nguồn: *Punched Cards → Machine Code → Low-level/Assembly → High-level (C#, C++, Dart) → AI Agentic Workforce*.

---

## ⚡ Bằng chứng Năng lực qua 170+ Repositories Thực chiến

Dưới đây là một số dự án mã nguồn mở tiêu biểu được trích xuất từ [GitHub @badpaybad](https://github.com/badpaybad):

### 🤖 AI Agentic, Local LLMs & Computer Vision
- [**a.i-foundation-boilerplate**](https://github.com/badpaybad/a.i-foundation-boilerplate): Hệ sinh thái Foundation Boilerplate chuẩn Enterprise (.NET 10, Angular Standalone, Flutter `tot-hub`), AI Sales Agent, Kho UHF RFID, ESP32-OS & CNC Automation ([fossagentic.men](https://fossagentic.men/)).
- [**a.i-assistant-chatbot-telegram-serverles**](https://github.com/badpaybad/a.i-assistant-chatbot-telegram-serverles): Hệ thống PC AI Agentic Workforce – Trợ lý AI cá nhân hóa chạy trực tiếp trên máy tính, giao tiếp qua Telegram, hoạt động không cần cloud server.
- [**Ner_Llm_Gpt**](https://github.com/badpaybad/Ner_Llm_Gpt): Tối ưu hóa mô hình ngôn ngữ lớn Vistral LLM chạy qua `llama.cpp` hoàn toàn trên CPU phục vụ nhận dạng thực thể có tên (Named Entity Recognition).
- [**InsightFace_TF**](https://github.com/badpaybad/InsightFace_TF) & [**insightface**](https://github.com/badpaybad/insightface): Hệ thống phân tích và nhận diện khuôn mặt 2D/3D chuyên sâu trên nền tảng TensorFlow.
- [**pixel_link**](https://github.com/badpaybad/pixel_link) & [**OcrTesseract**](https://github.com/badpaybad/OcrTesseract): Phân đoạn phát hiện văn bản theo phân vùng đối tượng (Instance Segmentation) và OCR nâng cao.
- [**darknet**](https://github.com/badpaybad/darknet): Hệ thống mạng nơ-ron nhận diện vật thể thời gian thực YOLOv4 trên Linux/Windows.

### ⚡ Low-Level Native Interop & High-Performance Media
- [**flutter-dart-ffi-dlib-opencv**](https://github.com/badpaybad/flutter-dart-ffi-dlib-opencv): Biên dịch mã nguồn Native C/C++ (`dlib`, `OpenCV`) thành shared library (`.so`), giao tiếp trực tiếp qua Dart FFI trên Android/Flutter với hiệu năng tối đa.
- [**rplayer**](https://github.com/badpaybad/rplayer): Trình phát video luồng RTSP độ trễ cực thấp cho Flutter, dùng trực tiếp Dart FFI thay thế MethodChannel chậm chạp.
- [**cameraip2youtubelive**](https://github.com/badpaybad/cameraip2youtubelive): Tự động đọc luồng RTSP từ Camera IP bằng OpenCV và chuyển tiếp trực tiếp (Live Stream) lên YouTube qua FFmpeg.
- [**dlib-android**](https://github.com/badpaybad/dlib-android) & [**libuvc**](https://github.com/badpaybad/libuvc): Tối ưu thư viện thị giác máy tính và điều khiển thiết bị video USB đa nền tảng.

### 🏗️ Enterprise Foundation Architecture & Distributed Backend
- [**cqrs-dot-net-core**](https://github.com/badpaybad/cqrs-dot-net-core): Khung kiến trúc mẫu chuẩn mực ứng dụng CQRS trên .NET Core, sử dụng Redis làm Message Bus cho xử lý phân tán.
- [**opendotnet-ecommerce-platform**](https://github.com/badpaybad/opendotnet-ecommerce-platform): Nền tảng thương mại điện tử cấp doanh nghiệp thiết kế theo triết lý CQRS, DDD, Event Sourcing và Microservices.
- [**dart-run-as-httpserver-api-sse-ws**](https://github.com/badpaybad/dart-run-as-httpserver-api-sse-ws): Backend server hiệu năng cao viết bằng Dart hỗ trợ đầy đủ REST API, Server-Sent Events (SSE) và WebSockets realtime.
- [**mini-mvc**](https://github.com/badpaybad/mini-mvc): WebHost runtime siêu nhỏ gọn cho C# hỗ trợ HTTP và WebSocket không cần phụ thuộc framework nặng nề.
- [**dotnetcore-serverless**](https://github.com/badpaybad/dotnetcore-serverless): Kiến trúc Serverless chuẩn hóa sẵn sàng triển khai trên AWS, Azure và Google Cloud.

### 🛰️ Robotics, Real-time Streaming & Edge Computing
- [**ros_navigation_command_app**](https://github.com/badpaybad/ros_navigation_command_app): Ứng dụng điều khiển Robot ROS tự hành qua lệnh thoại, điều hướng trên bản đồ và joystick ảo.
- [**rplidaropencv**](https://github.com/badpaybad/rplidaropencv) & [**ros_nodes**](https://github.com/badpaybad/ros_nodes): Tích hợp cảm biến Lidar RPLIDAR A1 và giao tiếp ROS Node thời gian thực.
- [**webrtc-api-connect**](https://github.com/badpaybad/webrtc-api-connect) & [**webrtc-firebase-demo**](https://github.com/badpaybad/webrtc-firebase-demo): Giải pháp truyền dẫn video/âm thanh thời gian thực độ trễ thấp qua WebRTC.
- [**jetson-nano-image**](https://github.com/badpaybad/jetson-nano-image): Xây dựng bản phân phối Ubuntu tối giản cho phần cứng nhúng Nvidia Jetson Nano phục vụ AI Edge.

---

## 🎯 Tại sao Đối tác & Khách hàng Tin tưởng Tôi?

1. **Hiểu sâu từ phần cứng đến tầng ứng dụng**: Không chỉ làm việc ở tầng framework bề mặt, tôi có khả năng can thiệp trực tiếp vào bộ nhớ, CPU, vi điều khiển ESP32-S3, sóng UHF RFID, native C/C++ và tối ưu hóa hệ thống từ tầng nhân.
2. **Kỷ luật & Tư duy Kiến trúc dài hạn**: Mỗi dòng mã đều được tổ chức có cấu trúc rõ ràng, dễ bảo trì, dễ mở rộng và có tài liệu bàn giao đầy đủ.
3. **Tiên phong thực chiến**: Không chỉ lý thuyết, mọi giải pháp đều được kiểm chứng bằng 170+ dự án mã nguồn mở, hệ thống thương mại tại [fossagentic.men](https://fossagentic.men/) và áp dụng hiệu quả vào sản xuất.
4. **Tối ưu chi phí thực tế cho đối tác**: Luôn tư vấn giải pháp hiệu quả nhất về mặt chi phí vận hành (sử dụng AI trên PC, tối ưu token, giảm tải server cloud).

---

## 📬 Liên hệ & Khởi động Dự án

Hãy liên hệ trực tiếp với tôi để cùng thảo luận về kiến trúc hệ thống, ý tưởng sản phẩm mới hoặc giải pháp tự động hóa AI & phần cứng cho doanh nghiệp của bạn:

- 🌐 **ToT Tech Ecosystem**: [https://fossagentic.men/](https://fossagentic.men/) *(Sản phẩm, Video Demo & Đăng ký tư vấn)*
- 🚀 **Live AI Sales Workspace**: [app.fossagentic.men/workspaces/sale-agent/cockpit](https://app.fossagentic.men/workspaces/sale-agent/cockpit)
- 📞 **Hotline / Zalo Kỹ thuật**: [0778.384.849](tel:0778384849)
- ✉️ **Email**: [badpaybad@gmail.com](mailto:badpaybad@gmail.com)
- 🐙 **GitHub**: [@badpaybad](https://github.com/badpaybad) *(170+ Repositories | Arctic Vault Contributor)*
- 🐦 **X (Twitter)**: [@badpaybad](https://twitter.com/badpaybad)
- 💬 **Telegram**: [@badpaybad](https://t.me/badpaybad)
- 📱 **Skype**: `badpaybad`
- 🌐 **Facebook**: [facebook.com/badpaybad](https://facebook.com/badpaybad)
- 📍 **Địa điểm**: Hà Nội, Việt Nam (Nhận dự án Remote toàn cầu)
- ☕ **Sponsor / Ủng hộ**: [PayPal.me/dunp211284](https://www.paypal.com/paypalme/dunp211284)

---
