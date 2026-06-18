---
artifact: 01 — Case Analysis
bai-tap: Lab 1 — Phân tích "tử huyệt" chiến lược
format: Cá nhân trước → share trong bàn → chốt verdict cuối
time: 20 phút trên lớp
nop-cuoi: Có — đây là file nộp cuối của Lab 1
student: Nguyễn Hoàng Thanh Tùng
msv: 2A202600846
date: 18/06/2026
---

# Lab 1 — Case Analysis / Phân tích "tử huyệt" chiến lược

**Case đã chọn:** **Figma trước làn sóng AI-native design-to-code / Claude Design**
**Học viên:** **Nguyễn Hoàng Thanh Tùng**
**MSV:** **2A202600846**
**Ngày:** **18/06/2026**

## Bước 0 — Chọn case thật nhanh

- **Case / sản phẩm / công ty:** Figma
- **AI / platform / sản phẩm mới tạo áp lực:** Claude Design, v0, Bolt.new, Lovable và các công cụ AI-native sinh prototype/code trực tiếp
- **Vì sao tôi chọn case này?**
  > Figma từng thắng nhờ biến thiết kế UI/UX thành hạ tầng cộng tác cloud-native. Nhưng AI-native tools đang kéo điểm bắt đầu của workflow từ "vẽ màn hình tĩnh" sang "mô tả ý tưởng để có prototype/code chạy được", làm lung lay mô hình SaaS theo seat và vai trò trung gian của canvas thiết kế.

---

## Bước 1 — Gom 3-5 bằng chứng chốt

| # | Bằng chứng / số liệu chốt | Vì sao số này quan trọng? | Nguồn |
|---|---|---|---|
| E1 | Trước IPO, Figma có hơn 13 triệu MAU, hiện diện trong 95% Fortune 500 và 2/3 người dùng không phải designer. | Cho thấy Figma không chỉ là tool thiết kế, mà là hạ tầng cộng tác liên phòng ban với switching cost cao. | Tài liệu case đính kèm; Barron's/Yahoo Finance về S-1 Figma |
| E2 | Tháng 7/2024, Figma phải tạm dừng Make Design sau khi công cụ AI tạo giao diện gần giống Apple Weather; CEO Dylan Field thừa nhận vấn đề QA và tính biến thiên thấp của design system nền. | Đây là AI shock đầu tiên: AI đặt trực tiếp trong canvas có rủi ro đạo nhái, trust và kiểm soát chất lượng. | TechCrunch, The Guardian, Daring Fireball |
| E3 | Config 2025 ra mắt Figma Sites, Make, Buzz, Draw; Figma Make được định vị để tạo app/prototype bằng AI, Sites để publish website, Buzz cho nội dung marketing. | Figma phản ứng bằng cách mở rộng từ design tool sang hệ sinh thái "idea to launch", chứng tỏ core workflow cũ không còn đủ. | Figma Blog Config 2025; The Verge; Forrester |
| E4 | Giá và seat model thay đổi từ 11/3/2025: Full, Dev, Collab seat; Dev Mode không còn là quyền miễn phí mặc định cho developer. | Seat-based SaaS bị căng thẳng khi developer có thể bypass bằng screenshot + AI IDE thay vì mua seat chỉ để inspect. | Figma Help: pricing, seats, billing experience |
| E5 | Q1/2026 Figma vẫn tăng trưởng mạnh: doanh thu 333,4 triệu USD, tăng 46% YoY; đồng thời cổ phiếu bị thị trường chiết khấu vì lo ngại AI thay đổi nhu cầu thiết kế. | Tác động không phải "Figma chết ngay"; mâu thuẫn là business còn tăng nhưng narrative định giá và moat đã bị nghi ngờ. | Figma Investor Relations Q1 2026; Barron's; tài liệu case đính kèm |

### 3 phát hiện ban đầu

1. **Case này từng thắng nhờ...**
   > Kiến trúc cloud-native, cộng tác multiplayer, một nguồn sự thật duy nhất cho design system và khả năng lôi cả designer, developer, PM, QA vào cùng workflow.
2. **AI shock làm thay đổi...**
   > Điểm bắt đầu của quá trình tạo sản phẩm số: từ vẽ canvas tĩnh rồi handoff sang mô tả intent để AI tạo prototype hoặc code chạy được.
3. **Dấu hiệu mạnh nhất cho thấy luật chơi mới là...**
   > Figma phải vừa tạm dừng Make Design vì rủi ro chất lượng, vừa mở rộng mạnh sang Sites/Make/Buzz/Draw để giữ vai trò trong chuỗi "idea to launch".

---

## Bước 2 — Viết 4 nhận định bắt buộc

### Nhận định 1 — Trước AI, case này thắng nhờ giả định gì?

**Trả lời của tôi:**

> Trước AI, Figma thắng nhờ giả định rằng thiết kế giao diện chất lượng cao là một công việc thủ công, cần canvas chuyên dụng, designer chuyên môn và một điểm bàn giao rõ ràng cho developer. Khi mọi người cùng làm trên một file cloud duy nhất, Figma biến bản thiết kế thành "system of record" của quá trình phát triển sản phẩm.
>
> Người dùng không chỉ thuê Figma để vẽ UI. Họ thuê Figma để giảm xung đột phiên bản, đồng bộ design system, review cùng nhau và bàn giao thông tin thiết kế cho các vai trò khác trong doanh nghiệp.

**Bằng chứng đỡ nhận định này:** E1, E4

---

### Nhận định 2 — Kỳ vọng người dùng và luật chơi cạnh tranh đã đổi ở đâu?

**Shift kỳ vọng quan trọng nhất:** Làm xong giúp tôi
**Competitive dynamic quan trọng nhất:** switching costs giảm và build-copy cycles tăng tốc

**Trả lời của tôi:**

> Kỳ vọng mới không còn là "cho tôi một bản mockup đẹp để người khác triển khai", mà là "tạo cho tôi một nguyên mẫu có thể chạy, click, test và sửa ngay". Các công cụ như Claude Design, v0, Bolt.new, Lovable làm người dùng quen với việc đi thẳng từ mô tả sang artifact hoạt động được.
>
> Luật chơi cạnh tranh vì vậy chuyển từ cạnh tranh tính năng vẽ và cộng tác sang cạnh tranh entry point của workflow. Nếu PM hoặc developer bắt đầu trong AI chat/AI IDE, Figma có nguy cơ bị đẩy xuống vai trò nguồn tham chiếu hoặc bước tinh chỉnh sau cùng, thay vì là nơi bắt đầu mặc định.

**Bằng chứng đỡ nhận định này:** E2, E3, E4

---

### Nhận định 3 — Giả định nào không còn đúng nữa? Điều gì đã thay đổi vĩnh viễn?

**Điều đã thay đổi vĩnh viễn theo tôi là:**

> Giả định "bản thiết kế tĩnh là cầu nối bắt buộc giữa ý tưởng và sản phẩm chạy được" không còn đúng tuyệt đối. AI đã làm cho việc tạo bản nháp giao diện và prototype ban đầu trở nên rẻ, nhanh và dễ tiếp cận hơn rất nhiều.
>
> Điều thay đổi vĩnh viễn là chuẩn kỳ vọng của người dùng: họ muốn rút ngắn vòng lặp từ ý tưởng đến trải nghiệm có thể thử. Canvas tĩnh vẫn có giá trị, nhưng không còn mặc nhiên là điểm bắt đầu duy nhất; giá trị bền hơn chuyển sang quản trị design system, chuẩn hóa component, kiểm soát brand, accessibility, edge cases và chất lượng sản xuất.

**Bằng chứng đỡ nhận định này:** E2, E3, E5

---

### Nhận định 4 — Case này còn cứu được không? Nếu có, phải đổi bằng cách nào?

**Verdict ban đầu của tôi:** Có nhưng phải đổi rất mạnh

**Trả lời của tôi:**

> Figma còn cứu được, nhưng không thể chỉ phòng thủ như một công cụ vẽ giao diện. Cách đổi đúng là định vị Figma thành system of record cho design system và product context mà các AI agent phải truy vấn khi tạo giao diện hoặc code.
>
> Figma nên để AI-native tools thắng ở khâu generation ban đầu, còn mình thắng ở khâu refinement: chuẩn hóa component, variable, brand rule, accessibility, governance, review và handoff có cấu trúc. Nếu tiếp tục ép tăng doanh thu chủ yếu bằng seat cho các vai trò phụ trợ, user sẽ càng có động lực bypass bằng AI tool bên ngoài.

**Bằng chứng đỡ nhận định này:** E3, E4, E5

---

## Tóm tắt cá nhân trước khi share trong bàn

1. `Case này yếu đi vì...` AI làm rẻ hóa bước tạo mockup/prototype ban đầu, khiến canvas tĩnh không còn là entry point bắt buộc.
2. `Điều thay đổi vĩnh viễn là...` người dùng kỳ vọng đi thẳng từ intent sang artifact chạy được, còn design system mới là tài sản cần được quản trị chặt.
3. `Verdict của tôi là...` Figma không bị xóa sổ, nhưng phải chuyển từ "tool vẽ UI" sang "system of record/API cho design system trong workflow AI".

---

## Bước 3 — Share trong bàn

### Ghi nhanh khi nghe các bạn cùng bàn

| Người | Case | Bằng chứng mạnh nhất họ nêu | Điều họ cho là "thay đổi vĩnh viễn" | Verdict của họ |
|---|---|---|---|---|
| Bạn 1 | Stack Overflow | Developer chuyển sang hỏi AI theo ngữ cảnh thay vì search Q&A cũ. | Entry point trợ giúp lập trình chuyển từ cộng đồng sang AI assistant. | Còn sống nếu trở thành trust layer/knowledge source. |
| Bạn 2 | Chegg | Thuê bao sụt mạnh sau khi ChatGPT phổ biến. | Gia sư generic bị commoditize. | Rất khó cứu nếu không có dữ liệu/credential riêng. |
| Bạn 3 | Figma | Make Design bị tạm dừng và Figma phải mở rộng sang Sites/Make/Buzz/Draw. | Mockup tĩnh không còn là artifact mặc định. | Cứu được nếu trở thành design system record. |
| Bạn 4 | Canva | AI tạo nội dung khiến template design phổ thông rẻ đi. | Người dùng muốn nội dung hoàn chỉnh, không chỉ template. | Còn mạnh nhờ distribution và brand workflow. |

### Sau khi cả bàn share xong, chốt 3 ý chung

**1. Bàn tôi thấy case nào có bằng chứng mạnh nhất? Vì sao?**  
Bàn tôi thấy Chegg có bằng chứng tác động tài chính rõ nhất, Stack Overflow có bằng chứng hành vi user rõ nhất, còn Figma có bằng chứng chiến lược sản phẩm rõ nhất. Với mục tiêu phân tích "tử huyệt" chiến lược, Figma đáng giữ vì nó cho thấy một công ty vẫn tăng trưởng nhưng giả định nền tảng về workflow đã bị AI tấn công.

**2. Có pattern nào lặp lại giữa nhiều case không?**  
Pattern chung là AI không chỉ thêm tính năng mới, mà kéo điểm bắt đầu của workflow sang nơi user có thể mô tả intent và nhận kết quả gần hoàn chỉnh. Những sản phẩm sống bằng thao tác trung gian, artifact tĩnh, hoặc seat phụ trợ đều bị ép phải chứng minh lại giá trị.

**3. Một cảnh báo cho chính dự án của nhóm tôi là gì?**

> Đừng xây sản phẩm AI chỉ như một lớp giao diện đẹp bên trên workflow cũ. Nếu dự án không nắm được dữ liệu/ngữ cảnh cốt lõi hoặc không trở thành một bước bắt buộc trong workflow thật, user có thể bypass bằng AI generalist rất nhanh.

---

## Bước 4 — Chốt lại verdict cá nhân sau thảo luận

### Sau khi nghe bàn phản biện, verdict của tôi:

- [ ] Giữ nguyên
- [x] Đổi nhẹ
- [ ] Đổi mạnh

### Vì sao tôi giữ / đổi verdict?

> Tôi đổi nhẹ từ "Figma phải tự cạnh tranh trực diện với AI design tools" sang "Figma nên để AI tools làm generation, nhưng phải kiểm soát refinement và system of record". Phản biện từ các case khác cho thấy sản phẩm không nhất thiết chết khi AI commoditize một bước; nó chết khi không còn nắm bước tạo trust, context hoặc workflow repeatable.

### Verdict cuối cùng của tôi (phiên bản nộp)

**Case này tổn thương trước AI vì:**

> Figma từng dựa vào giả định rằng canvas thiết kế tĩnh là nơi bắt đầu và là cầu nối bắt buộc giữa ý tưởng, designer và developer. AI-native tools phá giả định đó bằng cách tạo prototype/code chạy được trực tiếp từ prompt, đồng thời làm seat-based pricing cho các vai trò phụ trợ trở nên dễ bị bypass.

**Điều thay đổi vĩnh viễn là:**

> Người dùng không còn thỏa mãn với mockup tĩnh như artifact chính. Chuẩn mới là vòng lặp nhanh từ intent đến artifact chạy được, sau đó tinh chỉnh bằng design system, governance và kiểm soát chất lượng.

**Nếu phải rút 1 bài học cho dự án của nhóm mình, tôi rút ra:**

> Dự án AI phải chọn đúng điểm trong workflow nơi nó nắm được context và tạo outcome thật. Nếu chỉ giúp tạo bản nháp generic mà không quản trị được dữ liệu, tiêu chuẩn và bước tinh chỉnh, lợi thế sẽ bị AI generalist copy rất nhanh.

---

## Checklist trước khi nộp

- [x] Tôi đã chọn ít nhất 3 bằng chứng chốt có nguồn.
- [x] Mỗi nhận định đều chỉ vào ít nhất 1 bằng chứng.
- [x] Tôi đã ghi lại phần share trong bàn.
- [x] Tôi đã viết verdict cuối sau thảo luận.

---

## Nguồn tham khảo chính

- Tài liệu case đính kèm: "Đứt gãy sinh tạo: Khủng hoảng mô hình SaaS và cuộc tái định hình cấu trúc Figma trong kỷ nguyên AI".
- Figma Investor Relations — Q1/2026 results: https://investor.figma.com/news-events/news/news-details/2026/Figma-Announces-First-Quarter-2026-Financial-Results/default.aspx
- Figma Blog — Config 2025 recap: https://www.figma.com/blog/config-2025-recap/
- Figma Help — pricing, seats, billing updates: https://help.figma.com/hc/en-us/articles/27468498501527-Updates-to-Figma-s-pricing-seats-and-billing-experience
- TechCrunch — Figma disables Make Design after Apple Weather controversy: https://techcrunch.com/2024/07/02/figma-disables-its-ai-design-feature-that-appeared-to-be-ripping-off-apples-weather-app/
- The Guardian — Figma AI app creator accused of copying Apple Weather: https://www.theguardian.com/technology/article/2024/jul/03/figma-ai-app-creator-accused-of-ripping-off-apple-weather-app
- The Verge — Figma Sites, Make, Buzz, Draw announcement: https://www.theverge.com/news/662678/figma-buzz-draw-make-sites-announcement-availability
