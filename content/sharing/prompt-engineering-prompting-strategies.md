---
title: "Prompt Engineering - Prompting Strategies"
date: 2026-04-19T12:00:00+07:00
description: "Back to basic - Prompt Engineering - Prompting Strategies, hiểu cách hoạt động và làm prompt tốt hơn"
featured_image: "img/featured.png"
categories: ["PC AI Agentic", "Sharing"]
tags: ["llm", "ai", "prompt"]
---

A.I LLM phát triển rất nhanh về việc ứng dụng và sử dụng vào công việc và cuộc sống. Bạn hàng ngày sẽ nhận được rất nhiều cách làm, rất nhiều MVP ( minimum value product) để demo. Bạn thấy rất FOMO (nỗi sợ bị đứng ngoài), các từ khóa liên tục xuất hiện vd  harness engineering ... và muốn học thật nhanh, thật nhiều. Và cũng nhiều mô hình A.I LLM liên tục cập nhật ...

Nhưng bạn có bao giờ dừng lại và tự hỏi chạy theo mãi thì đến bao giờ mới dừng? 

Back to basic, hãy quay về với những gì là căn bản nhất để tự tin hơn khi sử dụng A.I LLM. A.I LLM sẽ thành nền tảng của xã hội mới hãy nắm bắt một cách có trách nhiệm và hiệu quả.

# Các đặc thù của A.I LLM 

Nó giống như bộ não thứ 2 của con người, sẽ khuếch đại năng lực của con người lên rất nhiều lần, nhưng cũng sẽ khuếch đại những sai lầm. 

Bộ máy thông minh tạo ra chữ từ chữ được đưa cho, bạn gần như chỉ cần hiểu nó là 1 blackbox, một hàm thông minh bạn không rõ bên trong có gì. Nhận đầu vào là string và return là string. Nhận Input string và trả Output string

Cần một năng lực tính toán và bộ nhớ khổng lồ để ra kết quả tốt. 

Sâu thẳm là khái niệm self attention, giống như việc bạn đọc một câu chuyện, bạn sẽ chú ý đến các từ khóa, các từ quan trọng để hiểu câu chuyện. 

# Làm sao để khai thác nó tốt?

Bạn cần hiểu cách tạo ra string input tốt để A.I LLM có thể hiểu và trả ra string output kết quả tốt. 

## Các tài liệu tham khảo sẽ giúp bạn

[Prompt Engineering](https://drive.google.com/file/d/1wHqX_qkG4eF__SQKxFZVNoZ7KhzATdGE/view?usp=sharing)

[Prompting Strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies)

[Agentic Design Patterns](https://drive.google.com/file/d/1MNO1N14au4LcC7CH1lsWq9w1LokfhZZa/view?usp=sharing)

# Kinh nghiệm bản thân

## Các khái niệm 

- Self attention: Giống như việc bạn đọc một câu chuyện, bạn sẽ chú ý đến các từ khóa, các từ quan trọng để hiểu câu chuyện. 

- Context: Là việc cộng dồn string rồi tạo thành input string cho A.I LLM

- System instruction: Trong input string bạn đưa cho LLM thì đoạn đầu tiên thường là system instruction, nó sẽ định hướng cho LLM hiểu nó là ai, nó cần làm gì, nó cần trả ra kết quả như thế nào.

- Prompt: Là các string bạn cộng chuỗi thêm vào sau system instruction. Nếu cấu trúc tốt thì LLM sẽ hiểu và trả ra kết quả tốt. 

- Data feed: Là các string bạn cộng chuỗi thêm vào sau prompt để phục vụ việc khai thác dữ liệu nhờ LLM đọc hiểu prompt để khai thác dữ liệu. 

- Markdown: Cấu trúc để bố trí text, đơn giản và dễ đọc, dễ hiểu cho LLM. 

- Tools (tool calls, functions call): Là một dạng prompt đặc biệt để **lập trình viên** có thể định nghĩa tên hàm , mô tả hàm, tham số hàm, và LLM sẽ trả ra kết quả là một string chứa tên hàm và tham số hàm để **lập trình viên** có thể gọi hàm đó và trả lại kết quả cho LLM. (Tức là ở output string nhận được lập trình viên sẽ regex if else ... tên hàm rồi gọi code chạy thật)

- A.I Workflow: Là một chuỗi các prompt, tool call được sắp xếp theo một trình tự nhất định để xử lý một tác vụ cụ thể. Có thể do lập trình viên sắp xếp code, kéo thả như n8n, make.com ...

- A.I Agent: Là một đoạn code, với vòng lặp vô tận ( while true) dùng các prompt, tool call để lấy data feed tạo context cho LLM xử lý cho tới khi trả được kết quả cuối cho người dùng. Tức là có thinking có suy luận rồi thực thi (tools) cho tới khi có kết quả như prompt mong muốn.

- A.I MCP (Model context protocol): Là giao thức kết nối giữa AI và Nguồn dữ liệu/Công cụ. Là đề cập tới việc các đoạn code viết ra Agent hoặc wrap LLM, đưa ra cấu trúc định nghĩa tools vào LLM và LLM có thể gọi tools để lấy dữ liệu hoặc thực hiện hành động. 

- A.I Agentic: Là một hệ thống gồm nhiều A.I Agent làm việc cùng nhau để giải quyết một vấn đề phức tạp. Tiến tới việc AI có thể tự động hóa các tác vụ phức tạp, thay thế con người trong nhiều công việc.

- Hallucination (ảo giác): Do context có thể lớn, data feed và prompt để xử lý bị chiếm thiểu số, LLM có đặc tính self attention nên bị nhầm lẫn thông tin, dẫn tới trả ra kết quả sai lệch so với thực tế. 

## Các kỹ thuật

- Memmory: Là việc lưu trữ các thông tin cần thiết để A.I LLM có thể sử dụng trong các lần tương tác sau. 

- Short memory (trí nhớ ngắn hạn): Chính là context bạn đưa cho LLM trong một lần tương tác. 

- Long memory (trí nhớ dài hạn): Là việc lưu trữ các thông tin cần thiết để A.I LLM có thể sử dụng trong các lần tương tác sau. Thường là các file text, markdown, json, database, vector database... Bạn sẽ cần tools để lấy thông tin trong quá trình suy luận của A.I Agent.

- Orchestration, Router (điều phối, điều hướng): Là một Agent làm việc sắp xếp để cộng dồn các prompt, data feed một cách thông minh để A.I LLM có thể hiểu và trả ra kết quả tốt. Bạn có thể định nghĩa nhiều prompt + tools ở nhiều folder (Skills), nhưng khi chạy thật dựa trên context LLM sẽ quyết định cộng chuỗi prompt nào, data feed nào vào context để xử lý và tools để thực hiện hành động thật. 

- Spec driven: Viết yêu cầu vào một file .md (specification.md todo.md yeucau.md) và để A.I Agent ghi lại suy nghĩ cách làm ra file .md (plan.md implementation.md timhieu.md) khác 

- Divide and Conquer, break down (Chia ra để trị): Để tránh Hallucination (ảo giác) thì bạn nên chia nhỏ vấn đề ra để xử lý, mỗi lần chỉ xử lý một vấn đề nhỏ, sau đó tổng hợp kết quả lại. Chia nhỏ bài toàn ở các bước nhỏ, mỗi bước chỉ xử lý một vấn đề nhỏ, sau đó tổng hợp kết quả lại.

## Các ví dụ thực tế 

IDE Google Antigravity là A.I Agentic chuyên nghành software develope.

System promt + tools + các kỹ năng ... đã được google làm rất tốt rồi

Bạn cần chủ yếu làm:
Prompt user là các file .md 
Data feed là các file code.

Giả sử bạn có figma: [iBank - Banking & E-Money Management App ](https://www.figma.com/design/IRvkp6XOexOUnlnel3TMtU/iBank---Banking---E-Money-Management-App-%7C-FinPay-%7C-Digital-%7C-Finance-Mobile-Banking-App-Ui-Kit--Community-?t=kXXbbFC2XhRsqeEG-0)

Bạn có thể vào figma export ra ảnh vào folder: design, và dùng ide google Antigravity để code app. Việc bạn code theo spec driven sẽ tiện. Luôn chỉ có 2 file yeucau.md và phattrien.md để xuyên suốt quá trình làm việc, figma export ra 1 folder ảnh rồi bạn promt ntn https://github.com/badpaybad/a.i-assistant-chatbot-telegram-serverles/blob/main/assistantapp/my_pc_assistant/yeucau.md . Nhưng bạn vẫn phải tuân thủ việc bản thân bạn phải review code kiến trúc code của bạn, điều chỉnh yeucau.md cập nhật liên tục, chia ra để trị từng lần cập nhật hoặc theo folder là sẽ ko bị ngợp.
Tuyệt đối ko để A.I sinh 1 đống rồi mới review tới lúc đó là tech debt quá lớn rồi.

Chia ra để trị và breakdown task (ko để AI làm, người làm, AI nó viết tham khảo lại thôi ): 

Vd về ứng dụng ban đầu dựng app hay web thì quan trọng nhất vẫn là : 

- Phase 1: layout + navigation -> dựng xong cơ bản vd lên đc login vào đc màn home ok done phase 1 (lúc này có thể còn thiếu nhiều vấn đề, đừng tham quá ). 

- Phase 2: tạo 1 dòng cập nhật mới ở yeucau.md vd thêm việc nhận notification UI và cơ chế. để ko phụ thuộc BE luôn cần yêu cầu viết mock của A.I -> để A.I auto test report = video . rồi tự mình test lại vd push noti =google console xem nó hiện thị ... . Xong rồi lại vào yeucau.md tạo cập nhật mới ... 

Làm cuốn chiếu xong gì dứt điểm đó và bản thân phải kiểm soát từng lần làm của A.I

Cách để bảo IDE google antigravity cập nhật, cần chắc chắn nó cập nhật suy nghĩ và cách làm vào phattrien.md 

                gõ vào ô chát A.I của IDE vd: @yeucau.md **cập nhật 2026-04-22 09:09:09**

![ai-guide-prompt](/img/ai-guide-prompt.png)


## Nguyên tắc làm việc với AI lifecycle

Chia ra để trị, làm cuốn chiếu, đảm bảo chất lượng từng phần 1. Ko ôm đồm. Ko để AI làm 1 núi xong mới test, review lúc đó tech debt quá lớn ko gỡ đc 

![AI-software-lifecycle](/img/AI-software-lifecycle.png)
