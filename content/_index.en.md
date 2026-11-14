---
title: "Nguyen Phan Du (badpaybad) | Senior Software Architect & AI Agentic Specialist"
description: "Professional profile & real-world Use Cases of Nguyen Phan Du (@badpaybad) - Founder of ToT Tech Ecosystem (fossagentic.men), Senior Software Architect & AI Agentic Specialist. Spanning Location-Agnostic UHF RFID (tot-hub + Chainway SR160), AI Sales Agent, ESP32-OS, Enterprise Boilerplate (.NET 10 / Angular / Flutter), CNC Automation & Native C/C++ FFI."
draft: false
---

Hello! I am **Nguyen Phan Du** ([@badpaybad](https://github.com/badpaybad)), a **Senior Software Architect, Foundation Infra Engineer & AI Agentic Specialist** based in Hanoi, Vietnam — and Founder / Lead Architect of **[ToT Tech Ecosystem (`fossagentic.men`)](https://fossagentic.men/)**.

With **over a decade of hands-on engineering experience** spanning embedded hardware, Native C/C++ FFI, high-throughput distributed backends, and **AI Agentic Workforce**, author of **170+ open-source repositories**, and recognized as an **Arctic Code Vault Contributor**, I architect and ship end-to-end production software and hardware systems for enterprises and partners.

{{< button href="https://fossagentic.men/" target="_blank" rel="noopener noreferrer" >}}🌐 Explore ToT Tech Ecosystem at fossagentic.men →{{< /button >}}

- **Product & Video Portal**: [https://fossagentic.men/](https://fossagentic.men/)
- **Live AI Sales Workspace**: [https://app.fossagentic.men/workspaces/sale-agent/cockpit](https://app.fossagentic.men/workspaces/sale-agent/cockpit)
- **Foundation Repo**: [github.com/badpaybad/a.i-foundation-boilerplate](https://github.com/badpaybad/a.i-foundation-boilerplate)

---

## 🚀 Production Products & Real-World Use Cases ([fossagentic.men](https://fossagentic.men/))

{{< lead >}}
Real-world software and hardware systems engineered, packaged, and deployed under ToT Tech Ecosystem — each built to solve a concrete operational bottleneck for clients and partners.
{{< /lead >}}

### 1. [Location-Agnostic Warehouse UHF RFID Item Finder (`Chainway SR160` + Flutter `tot-hub`)](https://fossagentic.men/#warehouse-rfid)
- **Use Case (Problem Solved)**: E-commerce, homeware, and spare-parts warehouses managing thousands of active SKUs struggle with rigid fixed-bin shelving and slow line-of-sight barcode scanning, leading to misplacements during peak hours and wasted time digging through cartons.
- **Product & Architecture**: **Chainway SR160** handheld reader (Impinj E-Series Gen2X, EPCglobal C1G2 / ISO 18000-6C, `865–928 MHz`, Dual-Mode UHF RFID + 1D/2D Barcode, BLE 5.0 GATT MTU 247 + Bluetooth HID + USB Type-C OTG / Pogo-Pin) paired with **Anti-Metal Hard Tags** & EPC labels; connected to the cross-platform **Flutter `tot-hub`** mobile app (Android/iOS, `shadcn_flutter`, single-hand radial menu, SSO OIDC) and synced directly to **Sapo POS** `barcode` fields via `.NET Core.Infra.WarehouseRfid` + CQRS `tracking_id`.
- **Measured Value**: Scans through cartons to intersect multiple target SKUs or Vietnamese product names simultaneously; announces results via **free offline Vietnamese Voice TTS (`flutter_tts` `vi-VN`)** (*1 match speaks product name, ≥ 2 speaks match count, 0 speaks "Không thấy"*) for hands-free picking; automatically restores Hex EPC strings mangled by Vietnamese Telex keyboards (`DD→Đ`, `AA→Â`, `EE→Ê`); supports 1-tap tag assignment and cross-warehouse Atomic RFID Transfer.
- **Links & Demo**: [Warehouse RFID Solution (`fossagentic.men/#warehouse-rfid`)](https://fossagentic.men/#warehouse-rfid) · [4K Real-World Video Demo (`02:25`)](https://fossagentic.men/videos/products/5.1.warehouse-rfid.webm)

### 2. [A.I Agent Agentic Omnichannel Sales — 3-Column Sales Cockpit & Fanpage Level 10 Engine](https://fossagentic.men/#ai-sale-agent)
- **Use Case (Problem Solved)**: Retail shops selling on Facebook suffer from slow page response times, missed Messenger inquiries/comments at peak hours, SKU/pricing mistakes by staff, dropped orders, and lack of consistent execution to unlock Facebook's organic *Recommendable* distribution.
- **Product & Architecture**: Event-Driven CQRS **AI Sales Agent** platform (Facebook Webhook + Redis CQRS + Angular 19 + `.NET 10`) featuring a real-time **3-column Sales Cockpit** (6 session tabs: `All`, `Pending`, `Needs Order`, `Messenger`, `Comment`, `Missed Messages`) with **Dual-Mode** (`AI_AUTO` `< 5s` 24/7 response and `CO_PILOT` draft review with `Approve & Send` / `Edit` / `Regenerate`); **PostgreSQL `pgvector` GraphRAG** + Given-When-Then Chain-of-Thought rules, `Session Focus Product`, `Obsolete Guarding` (blocks 0-VND or discontinued SKUs), and **Sapo Multi-Store (`#DUNP`)** order sync with pre/post-merger Vietnamese address normalization.
- **Measured Value**: Automates consultation, combo campaign pricing, and multi-branch Sapo order creation in a closed loop (*Conversation → Order → Revenue → Cart → Repeat Purchase*); paired with a **Level 1 → Level 10 Fanpage Growth Engine** (~80% AI automated / ~20% human) scheduling `08:00 AM` Daily Triads (Google Trends + Zeigarnik copywriting + Photo + 9:16 Story + 9:16 FFmpeg Vietnamese TTS Reel), building 1%–2% Lookalike Audiences from Sapo order history (30%–60% lower CPA), and running `02:00 AM` self-learning cycles.
- **Links & Demo**: [AI Sales Agent Overview (`fossagentic.men/#ai-sale-agent`)](https://fossagentic.men/#ai-sale-agent) · [Open Live Workspace (`app.fossagentic.men`)](https://app.fossagentic.men/workspaces/sale-agent/cockpit)

### 3. [`ESP32-OS` Embedded Operating System & 6 Standalone Embedded Kits (Touch, Audio, Citizen ID NFC, AI Mic Phone)](https://fossagentic.men/#embedded-kits)
- **Use Case (Problem Solved)**: Teams building industrial IoT devices, eKYC chip-ID kiosks, Vietnamese-capable HMI touch panels, or standalone voice AI hardware need deterministic multi-threaded firmware and clean bus isolation without spending months debugging FreeRTOS interrupt conflicts.
- **6 Standalone Hardware & Firmware Modules (`ESP32-S3 N16R8`, 16MB Flash / 8MB OPI PSRAM)**:
  1. **`ESP32-OS` Micro-Kernel & FreeRTOS EventBus**: Mutex-safe Core 0 / Core 1 task separation, Captive Portal (`esp32os_dunp`) saving up to 5 WiFi profiles, ECDSA P-256 asymmetric authentication & Firestore sync.
  2. **Standalone TFT Touch 2.8" Vietnamese UTF-8 Module**: `ILI9341` 320×240 (40MHz SPI) + `XPT2046` with a native vector renderer for Vietnamese UTF-8 diacritics (NFC/NFD) without heavy bitmap font tables.
  3. **Standalone Dual-Mic I2S `INMP441` Module**: 16kHz PCM capture, DC-offset DSP filtering, on-chip TFLite Micro Wake-Word (*"Du ơi"*) + 60s VAD auto-standby.
  4. **Standalone Digital Audio I2S DAC `MAX98357A` (24kHz)**: 24,000 Hz 16-bit PCM matching Gemini Live audio output, 256KB OPI PSRAM ring buffer for stutter-free streaming + boot hardware self-test.
  5. **RFID & Vietnamese Chip-Based Citizen ID Reader (`CCCD NFC PN532`)**: 13.56MHz ISO/IEC 14443-4 & ICAO Doc 9303 (APDU BAC/3DES decoding DG1, DG2 portrait photo, DG13; custom 262-byte FIFO hotfix & 921600 baud UART) for hotel, hospital, and banking eKYC kiosks.
  6. **Voice AI Chatbot Hardware — `ESP32 Mic Phone`**: Full-duplex WebSocket voice conversation with **Gemini 3.1 Flash Live** (`Aoede` `vi-VN` voice), Smart Barge-In interruption & 8 AI Function Calling tools.
- **Links & Demo**: [Embedded Kits & ESP32-OS (`fossagentic.men/#embedded-kits`)](https://fossagentic.men/#embedded-kits) · [IoT Gateway Video](https://fossagentic.men/videos/products/3.iot.mp4) · [Industrial IoT PCB Video](https://fossagentic.men/videos/products/3.1.iotthbb.mp4)

### 4. [Foundation & Enterprise Boilerplate (`.NET 10` + `Angular Standalone` + `Flutter Monorepo`)](https://fossagentic.men/#services)
- **Use Case (Problem Solved)**: Startups and enterprises often burn 3–6 months building foundational plumbing — OIDC SSO, CQRS, real-time SSE/WebSockets, multi-tier i18n, and data-privacy compliance — before shipping their first business feature.
- **Product & Architecture**: Battle-tested **Clean Architecture, Modular Monolith & Microservices** boilerplate (`a.i-foundation-boilerplate`): **C# .NET 10** backend (`Core.Infra` NuGet packages, `BaseDbContext`, MediatR CQRS, Redis Cache & Pub/Sub, Firebase Auth/Firestore), **Angular Standalone + Signals** web frontend (Vite + AnalogJS, TailwindCSS v4, 3-tier i18n), **Flutter Monorepo (`tot-hub`)** (`shadcn_flutter`, `foundations/tot-flutter`), and built-in compliance with Vietnam Personal Data Protection Decree **13/2023/NĐ-CP**.
- **Measured Value**: Cuts project bootstrap time by **80%**, delivers `< 100ms` API latency, and hands over 100% source code ownership with zero vendor lock-in.
- **Links & Demo**: [Foundation Boilerplate Service (`fossagentic.men/#services`)](https://fossagentic.men/#services) · [4-Layer Architecture (`fossagentic.men/#architecture`)](https://fossagentic.men/#architecture) · [Project Estimator (`fossagentic.men/#estimator`)](https://fossagentic.men/#estimator) · [Source Repository (`GitHub`)](https://github.com/badpaybad/a.i-foundation-boilerplate)

### 5. [CNC Automation Machines (`CNC Touch`, `CNC Wooden & Plotter`) & `AI Vision Anti-Spoofing`](https://fossagentic.men/#products)
- **Use Case (Problem Solved)**: Automating physical touchscreen QA/QC durability and latency testing on real smartphones (replacing manual tapping), remote mobile call automation, precision woodworking/vector plotting, and real-time facial liveness verification.
- **Products & Video Proofs**:
  - **CNC Touch Machine**: 4-axis GRBL frame (`0.05mm` precision), spring-cushioned capacitive stylus protecting glass screens, Python API control — [Mobile Call Bot](https://fossagentic.men/videos/products/2.3.cnc.touch.mobi.call.mp4), [High-Speed Multi-Touch](https://fossagentic.men/videos/products/3.2.cnc.touch.mp4), [1M+ Click Durability](https://fossagentic.men/videos/products/4.cnc.toch.mp4), [QA/QC Touch Bot](https://fossagentic.men/videos/products/4.1.cnctouch.mp4).
  - **CNC Wooden Machine & Plotter**: Heavy-duty woodworking CNC driven by industrial **TB6600** drivers (4.0A, 1/32 microstepping) and 32-bit **GRBL-HAL** controller; vector-to-single-line mechanical plotter — [Single-Line Plotter](https://fossagentic.men/videos/products/4.3.cnc.drawing.mp4) & [Vector Art](https://fossagentic.men/videos/products/4.4.cnc.drawing.mp4).
  - **AI Computer Vision Anti-Spoofing**: Real-time `60FPS` (`99.8%`) facial recognition and liveness detection defeating photos and deepfakes — [Video Demo](https://fossagentic.men/videos/products/2.fake.face.mp4).
- **Links & Demo**: [10 Real-World Product Videos at `fossagentic.men/#products`](https://fossagentic.men/#products)

---

## 💎 Core Capabilities & Strategic Collaboration

{{< lead >}}
Beyond writing code, I deliver end-to-end architectural solutions: Rock-solid Foundation – Deep Performance Optimization – Cost Efficiency – Exponential Speed via AI.
{{< /lead >}}

### 🏗️ 1. Foundation Infrastructure & High-Performance Architecture
*For enterprises needing scalable architecture or solving critical performance bottlenecks.*
- **Enterprise Architecture Patterns**: Deep expertise in **CQRS (Command Query Responsibility Segregation), Domain-Driven Design (DDD), Event Sourcing, Asynchronous Message Brokers (Redis, Message Queues)**, and **Microservices**.
- **Deep Low-Level Optimization**: Eliminating communication overhead by compiling **Native C/C++ shared libraries (`.so`/`.dll`)** and invoking them directly via **Dart FFI** or **CLR Interop** for high-throughput computing, graphics, and real-time streaming.
- **Ultra-Lean Runtime Infrastructure**: Building ultra-lightweight backend runtimes (Dart Server, .NET Core Serverless, Micro-frameworks) delivering single-digit millisecond latency while slashing cloud server bills by up to 70%.

### 🚀 2. Zero-to-One Product Engineering (Technical Co-founding & Partnership)
*For founders and teams seeking to turn visionary ideas into production-ready platforms at record speed.*
- **Full-Spectrum Technical Leadership**: Covering the entire product lifecycle from foundation infra, database design, API Gateways, and real-time communications (SSE, WebSockets, WebRTC) to modern cross-platform apps (Flutter Mobile & Desktop).
- **AI-Accelerated Delivery**: Leveraging specialized AI Agentic workflows and custom IDE harnesses to dramatically compress MVP build times, shipping to production in weeks rather than months.
- **Architected for Scale**: Building clean, maintainable foundations from day one so you never have to throw away code when user traffic surges.

### 🤖 3. Pragmatic AI Agentic Workforce & Local LLM Solutions
*For organizations seeking genuine AI automation with zero cloud overhead and 100% data privacy.*
- **PC AI Agentic Workforce (Local-first, No Cloud Server Required)**: Deploying autonomous 24/7 AI agents that run directly on your workstation or PC, controlled seamlessly via Telegram Bot or private webhooks without recurring cloud fees.
- **Skill-Based Harness & Token Optimization**: Crafting project-specific rules and skill frameworks that activate the full multi-disciplinary power of AI IDEs while strictly minimizing token consumption.
- **On-Device & CPU-Optimized LLMs**: Deploying and optimizing local large language models (`llama.cpp`, `Vistral`, `Ollama`) on CPU hardware for Named Entity Recognition (NER), local document parsing, and absolute privacy.

### 🌐 4. Technical Advisory & Global Engineering Network
*For investors, startups seeking technical due diligence, or engineers wishing to connect.*
- Architecture auditing, technology stack evaluation, and tackling hard engineering challenges.
- Technical exchange on computing evolution: *Punched Cards → Machine Code → Assembly → High-Level Code (C#, C++, Dart) → AI Agentic Workforce*.

---

## ⚡ Battle-Tested Proof of Work (170+ Repositories)

Highlights from open-source repositories on [GitHub @badpaybad](https://github.com/badpaybad):

### 🤖 AI Agentic, Local LLMs & Computer Vision
- [**a.i-foundation-boilerplate**](https://github.com/badpaybad/a.i-foundation-boilerplate): Enterprise Foundation Boilerplate (.NET 10, Angular Standalone, Flutter `tot-hub`), AI Sales Agent, Warehouse UHF RFID, ESP32-OS & CNC Automation ([fossagentic.men](https://fossagentic.men/)).
- [**a.i-assistant-chatbot-telegram-serverles**](https://github.com/badpaybad/a.i-assistant-chatbot-telegram-serverles): PC AI Agentic Workforce – Personal AI assistant running locally on PC, controlled via Telegram, zero cloud server needed.
- [**Ner_Llm_Gpt**](https://github.com/badpaybad/Ner_Llm_Gpt): CPU-optimized execution of Vistral LLM via `llama.cpp` for Named Entity Recognition (NER).
- [**InsightFace_TF**](https://github.com/badpaybad/InsightFace_TF) & [**insightface**](https://github.com/badpaybad/insightface): 2D/3D deep facial analysis and recognition pipelines on TensorFlow.
- [**pixel_link**](https://github.com/badpaybad/pixel_link) & [**OcrTesseract**](https://github.com/badpaybad/OcrTesseract): Instance segmentation for text detection in natural scenes and advanced OCR.
- [**darknet**](https://github.com/badpaybad/darknet): YOLOv4 real-time object detection neural network implementations.

### ⚡ Low-Level Native Interop & High-Performance Media
- [**flutter-dart-ffi-dlib-opencv**](https://github.com/badpaybad/flutter-dart-ffi-dlib-opencv): Building native C/C++ (`dlib`, `OpenCV`) shared libraries (`.so`) invoked directly via Dart FFI on Android/Flutter with zero bridge latency.
- [**rplayer**](https://github.com/badpaybad/rplayer): Ultra-low-latency RTSP video streaming player for Flutter using direct Dart FFI instead of slow MethodChannels.
- [**cameraip2youtubelive**](https://github.com/badpaybad/cameraip2youtubelive): Ingesting IP camera RTSP streams via OpenCV and live-transcoding directly to YouTube via FFmpeg.
- [**dlib-android**](https://github.com/badpaybad/dlib-android) & [**libuvc**](https://github.com/badpaybad/libuvc): Cross-platform USB video device control and embedded computer vision.

### 🏗️ Enterprise Foundation Architecture & Distributed Backend
- [**cqrs-dot-net-core**](https://github.com/badpaybad/cqrs-dot-net-core): Enterprise reference boilerplate implementing CQRS on .NET Core with Redis as a distributed message bus.
- [**opendotnet-ecommerce-platform**](https://github.com/badpaybad/opendotnet-ecommerce-platform): Distributed eCommerce platform built on CQRS, DDD, Event Sourcing, and Microservices.
- [**dart-run-as-httpserver-api-sse-ws**](https://github.com/badpaybad/dart-run-as-httpserver-api-sse-ws): High-throughput Dart HTTP server supporting REST APIs, Server-Sent Events (SSE), and WebSockets.
- [**mini-mvc**](https://github.com/badpaybad/mini-mvc): Lightweight C# WebHost runtime supporting HTTP & WebSockets without heavy framework overhead.
- [**dotnetcore-serverless**](https://github.com/badpaybad/dotnetcore-serverless): Serverless boilerplate architected for AWS, Azure, and Google Cloud.

### 🛰️ Robotics, Real-time Streaming & Edge Computing
- [**ros_navigation_command_app**](https://github.com/badpaybad/ros_navigation_command_app): ROS autonomous robot navigation with voice commands, map goal-setting, and virtual joystick.
- [**rplidaropencv**](https://github.com/badpaybad/rplidaropencv) & [**ros_nodes**](https://github.com/badpaybad/ros_nodes): Real-time RPLIDAR A1 integration and ROS communication interfaces.
- [**webrtc-api-connect**](https://github.com/badpaybad/webrtc-api-connect) & [**webrtc-firebase-demo**](https://github.com/badpaybad/webrtc-firebase-demo): Low-latency real-time video/audio chat via WebRTC.
- [**jetson-nano-image**](https://github.com/badpaybad/jetson-nano-image): Minimalist custom Ubuntu distribution built for Nvidia Jetson Nano embedded edge AI.

---

## 🎯 Why Partners & Clients Trust Me

1. **Hardware-to-Application Mastery**: I don't stop at framework wrappers; I operate comfortably across kernel levels, memory management, ESP32-S3 microcontrollers, UHF RFID, native C/C++ bindings, and distributed cloud layers.
2. **Long-Term Architectural Discipline**: Every system is designed with clean boundaries, high observability, robust error handling, and complete documentation.
3. **Proven Real-World Execution**: Not just theory — all architectural patterns are validated by 170+ open-source repositories, live production systems at [fossagentic.men](https://fossagentic.men/), and enterprise deployments.
4. **Pragmatic Cost-Efficiency**: Always recommending the most economical and performant path (PC-based AI agents, token reduction strategies, lean server footprints).

---

## 📬 Get in Touch & Start a Project

Let's discuss your next system architecture, product launch, or AI & hardware automation workflow:

- 🌐 **ToT Tech Ecosystem**: [https://fossagentic.men/](https://fossagentic.men/) *(Flagship Products, Video Demos & Consultation)*
- 🚀 **Live AI Sales Workspace**: [app.fossagentic.men/workspaces/sale-agent/cockpit](https://app.fossagentic.men/workspaces/sale-agent/cockpit)
- 📞 **Hotline / Zalo**: [0778.384.849](tel:0778384849)
- ✉️ **Email**: [badpaybad@gmail.com](mailto:badpaybad@gmail.com)
- 🐙 **GitHub**: [@badpaybad](https://github.com/badpaybad) *(170+ Repositories | Arctic Vault Contributor)*
- 🐦 **X (Twitter)**: [@badpaybad](https://twitter.com/badpaybad)
- 💬 **Telegram**: [@badpaybad](https://t.me/badpaybad)
- 📱 **Skype**: `badpaybad`
- 🌐 **Facebook**: [facebook.com/badpaybad](https://facebook.com/badpaybad)
- 📍 **Location**: Hanoi, Vietnam (Available for Global Remote Engagements)
- ☕ **Sponsor**: [PayPal.me/dunp211284](https://www.paypal.com/paypalme/dunp211284)

---
