---
title: "Nguyen Phan Du (badpaybad) | Senior Software Architect & AI Agentic Specialist"
description: "Production-ready software, AI Agentic, and embedded hardware systems by Nguyen Phan Du (@badpaybad) - Founder of ToT Tech Ecosystem (fossagentic.men): AI PC Agentic Workforce, Omnichannel AI Sales Agent, Warehouse UHF RFID (tot-hub), ESP32-OS Kits, Enterprise Boilerplate (.NET 10 / Angular / Flutter) & CNC Automation."
aliases:
  - "/en/"
draft: false
---

Hello! I am **Nguyen Phan Du** ([@badpaybad](https://github.com/badpaybad)), **Senior Software Architect, Foundation Infra Engineer & AI Agentic Specialist** in Hanoi, Vietnam — and Founder of **[ToT Tech Ecosystem (`fossagentic.men`)](https://fossagentic.men/)**.

With **10+ years of end-to-end engineering** spanning embedded hardware, Native C/C++ FFI, distributed backends, and **AI Agentic Workforce** (**170+ open-source repositories**, **Arctic Code Vault Contributor**), every product below is **system-complete, field-tested, and ready for immediate practical deployment**.

{{< button href="https://fossagentic.men/" target="_blank" rel="noopener noreferrer" >}}🌐 Explore All Live Products & Video Demos at fossagentic.men →{{< /button >}}

- **Product Portal & Video Demos**: [https://fossagentic.men/](https://fossagentic.men/)
- **Live AI Sales Workspace**: [https://app.fossagentic.men/workspaces/sale-agent/cockpit](https://app.fossagentic.men/workspaces/sale-agent/cockpit)
- **Foundation Boilerplate Repo**: [github.com/badpaybad/a.i-foundation-boilerplate](https://github.com/badpaybad/a.i-foundation-boilerplate)
- **AI PC Agentic Workforce Guide**: [AI PC Agentic Workforce Overview](/pc-ai-agentic/)

---

## 🚀 Production-Ready Systems & Practical Solutions ([fossagentic.men](https://fossagentic.men/))

{{< lead >}}
Each system below is engineered as a complete, ready-to-use solution—combining hardware, firmware, backend, apps, and AI workflows to solve real operational bottlenecks reliably.
{{< /lead >}}

| # | Solution | Practical Business Problem Solved | System Readiness | Access |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **A.I PC Agentic Workforce** | Replace 60%–90% SaaS gaps with a **99%–100%** tailored workflow via Forward Developer + AI, controlled via Telegram / FB Messenger | **Ready to Deploy** (Local PC + Skills + Tunnel) | [Read Overview →](/pc-ai-agentic/) |
| **2** | **A.I Agent Omnichannel Sales** | Eliminate slow Facebook replies, pricing errors & missed orders; grow Fanpage **Level 1 → Level 10** | **Live Production** (`app.fossagentic.men`) | [Live Cockpit →](https://app.fossagentic.men/workspaces/sale-agent/cockpit) |
| **3** | **Warehouse UHF RFID Finder** | Find mixed SKUs inside sealed cartons instantly without fixed bin locations, synced to Sapo POS | **Production Ready** (`SR160` + `tot-hub`) | [4K Video Demo →](https://fossagentic.men/videos/products/5.1.warehouse-rfid.webm) |
| **4** | **`ESP32-OS` & 6 Embedded Kits** | Ready-to-integrate IoT touch UI, dual-mic wake-word, audio DAC, chip ID card (`CCCD NFC`) & Voice AI hardware | **6 Standalone Kits Ready** (`ESP32-S3`) | [Embedded Kits →](https://fossagentic.men/#embedded-kits) |
| **5** | **Enterprise Foundation Boilerplate** | Cut 3–6 months of core architecture setup (`.NET 10`, Angular, Flutter, SSO, Decree 13) by **80%** | **Complete Source Ownership** | [Boilerplate →](https://fossagentic.men/#services) |
| **6** | **CNC Automation & AI Vision** | Automate 1M+ physical touch QA tests, wood routing/vector plotting, and 60FPS anti-spoofing liveness | **10 Product Videos Live** | [Product Videos →](https://fossagentic.men/#products) |

### 1. [A.I PC Agentic Workforce & Forward-Developer Custom Systems](/pc-ai-agentic/)

- **System Readiness**: Complete local-first worker framework ready to deploy on any office PC or Mini-PC without monthly cloud VM costs ([`a.i-assistant-chatbot-telegram-serverles`](https://github.com/badpaybad/a.i-assistant-chatbot-telegram-serverles)).
- **Business Problem Solved**: Packaged SaaS only covers **60%–90%** of real daily operations. A **Forward Developer** paired with AI sits beside your team to build a **99%–100% tailored fit in under 1 week**, then guides your team to keep refining rules into a durable **Harness Worker**.
- **Practical Application**: Staff and managers assign tasks, send files/photos, review outputs, and receive end-of-day reports directly through **Telegram** or **Facebook Messenger**—while keeping sensitive company data on-premise via local LLMs (`Ollama`, `llama.cpp`, `Gemma 4`) or Cloud APIs.
- **Core Stack & Resources**: Cloudflare Tunnel (zero-server HTTPS webhooks), modular `Skills/` (`Playwright`, `PyAutoGUI`/OCR, `Jira`, Google Drive/Nextcloud, Zalo), Markdown/`.md` memory & RAG — [Full Overview](/pc-ai-agentic/) · [GitHub Source](https://github.com/badpaybad/a.i-assistant-chatbot-telegram-serverles).

### 2. [A.I Agent Omnichannel Sales — 3-Column Sales Cockpit & Fanpage Level 10](https://fossagentic.men/#ai-sale-agent)

- **System Readiness**: Live multi-tenant platform actively deployed at [`app.fossagentic.men`](https://app.fossagentic.men/workspaces/sale-agent/cockpit) with real-time Facebook Webhooks and multi-branch POS integration.
- **Business Problem Solved**: Stops missed customer Messenger/comment leads at peak hours, prevents incorrect SKU or promo pricing, and replaces inconsistent manual posting with structured **Level 1 → Level 10 Fanpage** growth.
- **Practical Application**:
  - Operators manage all customer conversations inside a real-time **3-column Sales Cockpit** (6 session queues: `All`, `Pending`, `Needs Order`, `Messenger`, `Comment`, `Missed Messages`) with **Dual-Mode**: `AI_AUTO` (`< 5s` 24/7 response) and `CO_PILOT` (`Approve & Send` / `Edit` / `Regenerate`).
  - Built-in safety (`Obsolete Guarding` blocks 0-VND or discontinued SKUs; `Session Focus Product` keeps pricing accurate) syncs confirmed orders directly to **Sapo Multi-Store (`#DUNP`)** with pre/post-merger Vietnam address normalization.
  - Automated **Fanpage Growth Engine** (~80% AI / ~20% human) schedules `08:00 AM` Daily Triads (Google Trends + copywriting + Photo + 9:16 Story + 9:16 FFmpeg Vietnamese TTS Reel), Lookalike 1%–2% Sapo audiences (30%–60% lower CPA), and `02:00 AM` self-learning cycles.
- **Core Stack & Resources**: Event-Driven CQRS (`Redis CQRS` + `.NET 10` + `Angular 19` + PostgreSQL `pgvector` GraphRAG) — [Solution Overview](https://fossagentic.men/#ai-sale-agent) · [Open Live Cockpit](https://app.fossagentic.men/workspaces/sale-agent/cockpit).

### 3. [Location-Agnostic Warehouse UHF RFID Item Finder (`Chainway SR160` + `tot-hub`)](https://fossagentic.men/#warehouse-rfid)

- **System Readiness**: End-to-end production hardware + mobile + POS backend system, field-proven in high-turnover SKU warehouses.
- **Business Problem Solved**: Eliminates slow line-of-sight barcode scanning, fixed-bin rigidity, and time wasted opening sealed cartons to locate items across thousands of SKUs.
- **Practical Application**:
  - Scans UHF radio waves (`865–928 MHz`) straight through cartons to match single or multiple SKUs simultaneously, tagging metal/non-metal goods cleanly with **Anti-Metal Hard Tags** and EPC labels.
  - Built-in **free offline Vietnamese Voice TTS (`flutter_tts` `vi-VN`)** announces exact picks hands-free (*1 match speaks product name, ≥ 2 speaks match count, 0 speaks "Không thấy"*), while automatically repairing Telex keyboard Hex corruption (`DD→Đ`, `AA→Â`, `EE→Ê`).
  - Supports 1-tap tag binding, global duplicate prevention, and cross-warehouse Atomic RFID Transfer synced directly with **Sapo POS** `barcode` fields.
- **Core Stack & Resources**: **Chainway SR160** (Impinj Gen2X, EPCglobal C1G2 / ISO 18000-6C, Dual RFID + Barcode, BLE 5.0 GATT / HID / USB-C OTG) + Flutter `tot-hub` (`shadcn_flutter`, radial 1-hand menu, OIDC SSO) + `.NET Core.Infra.WarehouseRfid` — [Solution Details](https://fossagentic.men/#warehouse-rfid) · [4K Demo Video (`02:25`)](https://fossagentic.men/videos/products/5.1.warehouse-rfid.webm).

### 4. [`ESP32-OS` Embedded Operating System & 6 Standalone Hardware Kits](https://fossagentic.men/#embedded-kits)

- **System Readiness**: Six independently packaged, production-ready hardware + firmware modules engineered on `ESP32-S3 N16R8` (16MB Flash / 8MB OPI PSRAM) so product teams can plug and deploy immediately without debugging RTOS/bus conflicts.
- **Business Problem Solved**: Removes months of low-level firmware engineering for industrial IoT gateways, hotel/hospital/bank eKYC kiosks reading chip citizen IDs, Vietnamese HMI touch panels, and standalone Voice AI devices.
- **6 Ready-to-Use Modules**:
  1. **`ESP32-OS` Core Kernel & FreeRTOS EventBus**: Mutex-safe Core 0 / Core 1 split, `esp32os_dunp` Captive Portal (5 WiFi profiles), ECDSA P-256 auth & Firestore sync.
  2. **TFT Touch 2.8" Vietnamese UTF-8 Kit**: `ILI9341` 320×240 (`40MHz` SPI) + `XPT2046` rendering native Unicode Vietnamese diacritics directly without heavy bitmap tables.
  3. **Dual-Mic Digital Audio `INMP441` Kit**: `16kHz` I2S PCM, DC-offset DSP, on-chip TFLite Micro Wake-Word (*"Du ơi"*) + 60s VAD auto-standby.
  4. **24kHz Digital DAC `MAX98357A` Kit**: Broadcast-clean PCM matched to Gemini Live with 256KB OPI PSRAM ring buffer and boot self-test.
  5. **RFID & Chip Citizen ID Reader (`CCCD NFC PN532`)**: `13.56MHz` ISO/IEC 14443-4 & ICAO Doc 9303 (APDU BAC/3DES reading DG1, DG2 portrait photo, DG13; 262-byte FIFO patch & `921600` baud UART) for instant eKYC check-in.
  6. **Voice AI Hardware Chatbot (`ESP32 Mic Phone`)**: Real-time full-duplex WebSocket voice agent powered by **Gemini 3.1 Flash Live** (`Aoede` `vi-VN`), Smart Barge-In, and 8 Function Calling tools.
- **Access & Video Proofs**: [Embedded Kits Portal](https://fossagentic.men/#embedded-kits) · [IoT Gateway Video](https://fossagentic.men/videos/products/3.iot.mp4) · [Industrial IoT PCB Video](https://fossagentic.men/videos/products/3.1.iotthbb.mp4).

### 5. [Enterprise Foundation & Boilerplate Platform (`.NET 10` + `Angular Standalone` + `Flutter Monorepo`)](https://fossagentic.men/#services)

- **System Readiness**: Complete, cleanly layered **Clean Architecture / Modular Monolith / Microservices** foundation actively powering multiple commercial systems—delivered with 100% source ownership and zero vendor lock-in.
- **Business Problem Solved**: Saves engineering teams **3–6 months** of boilerplate plumbing (auth, CQRS messaging, real-time events, multi-language UI, legal compliance) before delivering their first business feature.
- **Practical Impact**: Cuts project bootstrap time by **80%**, maintains `< 100ms` API response times, and ships with built-in Vietnam Personal Data Protection **Decree 13/2023/NĐ-CP** safeguards.
- **Core Stack & Resources**: **C# .NET 10** (`Core.Infra` NuGet libraries, `BaseDbContext`, MediatR CQRS, Redis Cache/PubSub, Firebase Auth/Firestore), **Angular Standalone + Signals** (Vite + AnalogJS, TailwindCSS v4, 3-tier i18n), **Flutter Monorepo (`tot-hub`)** — [Services Overview](https://fossagentic.men/#services) · [4-Layer Architecture](https://fossagentic.men/#architecture) · [Cost Estimator](https://fossagentic.men/#estimator) · [GitHub Source](https://github.com/badpaybad/a.i-foundation-boilerplate).

### 6. [CNC Industrial Automation & 60FPS AI Computer Vision Anti-Spoofing](https://fossagentic.men/#products)

- **System Readiness**: Operational electro-mechanical CNC hardware rigs and real-time computer vision pipelines verified across **10 live demo videos**.
- **Business Problem Solved**: Replaces repetitive manual touchscreen durability/QA testing on phones, automates precision woodworking and single-line plotting, and blocks photo/deepfake spoofing in attendance & access systems.
- **Ready-to-Use Systems**:
  - **CNC Touch Machine**: 4-axis GRBL frame (`0.05mm` precision), spring-cushioned capacitive stylus protecting glass, scripted via Python API — [Auto Call](https://fossagentic.men/videos/products/2.3.cnc.touch.mobi.call.mp4) · [Multi-Touch](https://fossagentic.men/videos/products/3.2.cnc.touch.mp4) · [1M+ Click Test](https://fossagentic.men/videos/products/4.cnc.toch.mp4) · [QA/QC Touch Bot](https://fossagentic.men/videos/products/4.1.cnctouch.mp4).
  - **CNC Wooden & Mechanical Plotter**: Industrial **TB6600** (`4.0A`, 1/32 microstepping) + 32-bit **GRBL-HAL** controller and vector-to-single-line plotting — [Plotter Video](https://fossagentic.men/videos/products/4.3.cnc.drawing.mp4) · [Vector Art Video](https://fossagentic.men/videos/products/4.4.cnc.drawing.mp4).
  - **AI Vision Anti-Spoofing**: Real-time `60FPS` (`99.8%` liveness) face verification — [Live Anti-Spoofing Video](https://fossagentic.men/videos/products/2.fake.face.mp4).
- **Video Library**: [All 10 Product Videos (`fossagentic.men/#products`)](https://fossagentic.men/#products).

---

## 💎 Core Engineering Capabilities & How We Collaborate

| Track | Best For | Deliverable & Value |
| :--- | :--- | :--- |
| **1. Foundation Infra & High-Load Architecture** | Enterprises scaling systems or cutting cloud spend | CQRS, DDD, Event Sourcing, Redis/Kafka brokers, Native C/C++ FFI, ultra-lean runtimes (up to 70% lower server cost) |
| **2. Zero-to-One Product Partnership** | Founders turning a product concept into production | Full-stack ownership (infra, APIs, WebSockets/SSE/WebRTC, Flutter apps) shipped rapidly without sacrificing scalability |
| **3. AI Agentic Workforce & Local LLM** | Teams automating real ops with full data privacy | Local-first PC AI agents (Telegram/Messenger), token-saving `Skills` harnesses, CPU-optimized `llama.cpp`/`Vistral`/`Ollama` |
| **4. Technical Advisory & Due Diligence** | CTOs, investors, or teams unblocking hard bugs | Architecture review, low-level performance audits, and practical AI adoption mentoring |

---

## ⚡ Open-Source Proof of Work (170+ Repositories)

Selected production-oriented repositories from [GitHub @badpaybad](https://github.com/badpaybad):

### 🤖 AI Agentic, Local LLMs & Computer Vision
- [**a.i-foundation-boilerplate**](https://github.com/badpaybad/a.i-foundation-boilerplate): Enterprise Foundation (.NET 10, Angular Standalone, Flutter `tot-hub`), AI Sales Agent, Warehouse RFID, ESP32-OS & CNC Automation ([fossagentic.men](https://fossagentic.men/)).
- [**a.i-assistant-chatbot-telegram-serverles**](https://github.com/badpaybad/a.i-assistant-chatbot-telegram-serverles): PC AI Agentic Workforce running locally 24/7 via Telegram with zero cloud server cost.
- [**Ner_Llm_Gpt**](https://github.com/badpaybad/Ner_Llm_Gpt): CPU-optimized Vistral LLM (`llama.cpp`) for local Named Entity Recognition.
- [**InsightFace_TF**](https://github.com/badpaybad/InsightFace_TF), [**pixel_link**](https://github.com/badpaybad/pixel_link), [**OcrTesseract**](https://github.com/badpaybad/OcrTesseract) & [**darknet**](https://github.com/badpaybad/darknet): 2D/3D face recognition, scene text segmentation, OCR & YOLOv4 detection.

### ⚡ Native FFI, Distributed Backend & Robotics Edge
- **Native Interop & Media**: [**flutter-dart-ffi-dlib-opencv**](https://github.com/badpaybad/flutter-dart-ffi-dlib-opencv) · [**rplayer**](https://github.com/badpaybad/rplayer) (low-latency RTSP via Dart FFI) · [**cameraip2youtubelive**](https://github.com/badpaybad/cameraip2youtubelive) · [**dlib-android**](https://github.com/badpaybad/dlib-android) · [**libuvc**](https://github.com/badpaybad/libuvc)
- **Distributed Backend**: [**cqrs-dot-net-core**](https://github.com/badpaybad/cqrs-dot-net-core) · [**opendotnet-ecommerce-platform**](https://github.com/badpaybad/opendotnet-ecommerce-platform) · [**dart-run-as-httpserver-api-sse-ws**](https://github.com/badpaybad/dart-run-as-httpserver-api-sse-ws) · [**mini-mvc**](https://github.com/badpaybad/mini-mvc) · [**dotnetcore-serverless**](https://github.com/badpaybad/dotnetcore-serverless)
- **Robotics & Edge**: [**ros_navigation_command_app**](https://github.com/badpaybad/ros_navigation_command_app) · [**rplidaropencv**](https://github.com/badpaybad/rplidaropencv) · [**ros_nodes**](https://github.com/badpaybad/ros_nodes) · [**webrtc-api-connect**](https://github.com/badpaybad/webrtc-api-connect) · [**jetson-nano-image**](https://github.com/badpaybad/jetson-nano-image)

---

## 🎯 Why Partners Work With Me

1. **Full-Stack Ownership From Hardware to Cloud**: Seamless execution across ESP32-S3 firmware, UHF RFID, Native C/C++, .NET 10 backends, Flutter/Angular apps, and PC AI Agents.
2. **Systems Ready for Real Use**: Focused on finished, maintainable products with clear documentation—not fragile hackathon demos.
3. **Tailored Workflow Fit Over Rigid Software**: Forward-developer delivery paired with AI gives **99%–100% alignment** in days rather than forcing teams into 70%-fit tools.
4. **Pragmatic Cost Control**: Local-first AI execution, token efficiency, and lean server architectures built to protect your operating margins.

---

## 📬 Direct Contact & Start a Deployment

- 🌐 **Product Ecosystem & Demos**: [https://fossagentic.men/](https://fossagentic.men/)
- 🚀 **Live AI Sales Cockpit**: [app.fossagentic.men/workspaces/sale-agent/cockpit](https://app.fossagentic.men/workspaces/sale-agent/cockpit)
- 📞 **Hotline / Technical Zalo**: [0778.384.849](tel:0778384849)
- ✉️ **Email**: [badpaybad@gmail.com](mailto:badpaybad@gmail.com)
- 💬 **Telegram**: [@badpaybad](https://t.me/badpaybad) · **Facebook**: [facebook.com/badpaybad](https://facebook.com/badpaybad)
- 🐙 **GitHub**: [@badpaybad](https://github.com/badpaybad) · **X**: [@badpaybad](https://twitter.com/badpaybad) · **Skype**: `badpaybad`
- 📍 **Location**: Hanoi, Vietnam *(Global Remote Ready)* · ☕ **Sponsor**: [PayPal.me/dunp211284](https://www.paypal.com/paypalme/dunp211284)
