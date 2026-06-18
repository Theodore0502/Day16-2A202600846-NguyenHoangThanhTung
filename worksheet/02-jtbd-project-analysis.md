---
artifact: 02 — JTBD Project Analysis
bai-tap: Lab 2 — Dùng JTBD để soi lại dự án nhóm
format: Theo nhóm dự án → share trong bàn → chốt hypothesis cuối
time: 25 phút trên lớp
nop-cuoi: Có — đây là file nộp cuối của Lab 2
companion-reference: Strategyn_JTBD_Playbook.pdf (giảng viên gửi kèm)
student: Nguyễn Hoàng Thanh Tùng
msv: 2A202600846
date: 18/06/2026
---

# Lab 2 — JTBD Project Analysis / Dùng JTBD để soi lại dự án nhóm

**Học viên:** **Nguyễn Hoàng Thanh Tùng**  
**MSV:** **2A202600846**  
**Ngày:** **18/06/2026**

**Tên dự án / sản phẩm:** Design System MCP Copilot cho nhóm sản phẩm SaaS

> Lưu ý: repo chưa có mô tả dự án nhóm riêng, nên bài này chọn một lát cắt dự án phù hợp trực tiếp với case Figma/AI trong tài liệu đính kèm.

---

## Bước 0 — Khoanh đúng 1 lát cắt của dự án

- **Dự án của nhóm tôi là:** Một trợ lý AI giúp nhóm sản phẩm SaaS biến yêu cầu giao diện thành prototype/code nhất quán với design system nội bộ.
- **Lát cắt tôi chọn để phân tích hôm nay là:** Giúp product designer và frontend developer tạo bản nháp màn hình mới từ yêu cầu PM mà vẫn bám component, token và guideline đang có.
- **Vì sao tôi chọn lát cắt này:**  
  > Đây là điểm đau rõ trong bối cảnh AI-native tools tạo giao diện rất nhanh nhưng dễ sai brand, sai component, sai accessibility và khó tinh chỉnh ở quy mô lớn.

---

## Bước 1 — Viết `Project Snapshot`

1. **Nhóm tôi đang nghĩ mình đang giải quyết vấn đề gì?**  
   > Các nhóm SaaS muốn dùng AI để tăng tốc thiết kế/giao diện, nhưng output thường không tuân thủ design system và phải sửa tay nhiều trước khi đưa vào production.

2. **Người dùng chính hiện nhóm đang nhắm tới là ai?**  
   > Product designer hoặc design system owner trong team SaaS có nhiều màn hình, nhiều component và nhiều developer cùng triển khai.

3. **Hiện tại người dùng đó đang giải quyết vấn đề này bằng cách nào?**  
   > Họ dùng Figma library, checklist design review, handoff thủ công, screenshot đưa vào Claude/Cursor, hoặc tự prompt v0/Lovable rồi sửa lại component cho đúng hệ thống.

---

## Bước 2 — Viết `Market Context`

1. **Ai đang gặp vấn đề này?**  
   > Nhóm sản phẩm SaaS đã có design system nhưng đang chịu áp lực ship nhanh hơn nhờ AI.

2. **Vấn đề xuất hiện trong hoàn cảnh nào?**  
   > Khi cần tạo màn hình mới, biến yêu cầu PM thành prototype, hoặc chuyển prototype thành UI code trong sprint ngắn.

3. **Hiện tại họ đang dùng giải pháp thay thế nào?**  
   > Figma + Dev Mode, design review thủ công, v0/Bolt/Lovable, Claude Code/Cursor, hoặc copy component từ codebase cũ.

4. **Vì sao đây là thời điểm đáng giải?**  
   > AI đã làm generation rẻ hơn, nhưng refinement và chuẩn hóa theo design system vẫn là điểm nghẽn tốn thời gian. Nếu giải được điểm này, AI không chỉ tạo demo đẹp mà còn giúp sản phẩm tiến gần production hơn.

### Tóm tắt market context trong 3-4 dòng

> Thị trường đang chuyển từ thiết kế tĩnh sang prototype/code được sinh bởi AI.
> Tuy nhiên, doanh nghiệp SaaS không chỉ cần tốc độ; họ cần output bám brand, component, accessibility và quy chuẩn kỹ thuật.
> Vì vậy cơ hội nằm ở lớp kết nối giữa AI generation và design system/codebase thật của doanh nghiệp.

---

## Bước 3 — Xác định `Job Executor`

- **Job executor của dự án này là:** Product designer phụ trách thiết kế màn hình trong một team SaaS có design system.
- **Vì sao tôi tin đây là người trực tiếp "thuê" giải pháp để làm job:**  
  > Người này trực tiếp nhận yêu cầu từ PM, chọn component, tạo layout, kiểm tra tính nhất quán, phối hợp với developer và chịu trách nhiệm chất lượng trải nghiệm trước khi bàn giao.

---

## Bước 4 — Viết `Core JTBD`

**Core JTBD bản nháp:**  
> Tạo màn hình bằng AI đúng design system để developer code nhanh hơn.

### Gạch bỏ từ solution nếu có

- Các từ solution tôi đang lỡ nhét vào câu: AI, design system, developer code

### Bản chốt

**Core JTBD cuối cùng:**  
> Chuyển một yêu cầu sản phẩm mới thành phương án giao diện nhất quán, có thể kiểm tra và sẵn sàng triển khai trong thời gian ngắn.

---

## Bước 5 — Viết 3 `Job Stories`

| # | Trigger / When | Motivation / I want to | Outcome / so I can | Điều story này cho thấy |
|---|---|---|---|---|
| JS1 | Khi PM đưa yêu cầu màn hình mới ngay trước sprint planning | Tôi muốn nhanh chóng tạo vài phương án giao diện bám pattern hiện có | Chốt hướng đủ sớm để team estimate và không trễ sprint | Pain nằm ở bước biến yêu cầu mơ hồ thành artifact cụ thể. |
| JS2 | Khi developer hỏi component nào, state nào và token nào cần dùng | Tôi muốn có spec rõ, nhất quán với thư viện hiện tại | Giảm vòng hỏi đáp và tránh code lệch design system | Pain nằm ở handoff và confirm tính đúng của component. |
| JS3 | Khi stakeholder yêu cầu sửa một chi tiết trên nhiều màn hình | Tôi muốn cập nhật thay đổi đồng bộ và kiểm tra tác động nhanh | Không phải rà từng frame hoặc từng file code thủ công | Pain nằm ở modify/refinement trên hệ thống nhiều màn hình. |

---

## Bước 6 — Liệt kê `Current Alternatives`

| Alternative hiện tại | User đang thuê nó để làm gì? | Nó làm tốt gì? | Nó fail ở đâu? | Switching cost hiện tại cao hay thấp? |
|---|---|---|---|---|
| Figma + component library + Dev Mode | Thiết kế, review, inspect và bàn giao UI | Cộng tác tốt, direct manipulation tốt, design system mạnh | Tạo bản nháp ban đầu chậm hơn AI; Dev Mode/seat tạo friction chi phí | Cao với team đã có thư viện lớn |
| v0 / Lovable / Bolt.new | Tạo prototype hoặc UI code nhanh từ prompt | Rất nhanh ở bản nháp đầu, có code chạy được | Dễ sai component nội bộ, khó đảm bảo brand/accessibility/governance | Thấp cho thử nghiệm, cao cho production |
| Claude Code / Cursor + screenshot Figma | Sinh code từ hình hoặc mô tả | Tiện cho developer, không cần nhiều handoff | Thiếu context design system có cấu trúc, dễ đoán sai spacing/state | Trung bình |

### Kết luận nhanh

**Nếu project của tôi biến mất hôm nay, user nhiều khả năng sẽ quay về:**  
> Figma để quản trị design system, cộng thêm v0/Claude/Cursor để tạo bản nháp nhanh rồi sửa tay cho đúng.

---

## Bước 7 — Điền `JTBD Lite Map`

| Step | Trong workflow này user đang cố làm gì? | Hôm nay họ đang dùng gì? | Friction / pain hiện tại | Mức đau |
|---|---|---|---|---|
| Define | Hiểu yêu cầu màn hình, constraint nghiệp vụ, user flow | Ticket PM, meeting, doc | Yêu cầu mơ hồ, thiếu state/edge case | High |
| Locate | Tìm pattern, component, token, màn hình tương tự | Figma library, file cũ, Storybook | Tìm lâu, dễ dùng nhầm version component | Med |
| Prepare | Lắp layout, chọn component, chuẩn bị content/state | Figma, copy frame cũ, AI prompt | Bản nháp nhanh thì sai chuẩn; bản đúng chuẩn thì làm chậm | High |
| Confirm | Kiểm tra đúng brand, accessibility, component và logic flow | Design review, checklist, comment | Review thủ công, bỏ sót edge case | High |
| Execute | Tạo prototype hoặc spec cho developer | Figma prototype, Dev Mode, ticket | Handoff thiếu ngữ cảnh hoặc phải mua seat | Med |
| Monitor | Theo dõi developer implement có lệch design không | PR review, QA, Slack | Designer vào muộn, lỗi phát hiện sau | Med |
| Modify | Sửa thay đổi trên nhiều màn hình/component | Variables, component updates, sửa tay | Thay đổi lan rộng khó kiểm soát, tốn nhiều lượt review | High |
| Conclude | Chốt phiên bản, lưu lesson/pattern mới vào system | Figma branch, design system doc | Tri thức không được cập nhật lại thành rule tái sử dụng | Med |

### Chốt 2 bước đau nhất

**Bước đau nhất #1:** Prepare
**Bước đau nhất #2:** Confirm

**Vì sao đây là nơi đáng chú ý nhất:**  
> Prepare là nơi AI có thể tăng tốc rõ nhất, nhưng cũng là nơi dễ sinh UI sai chuẩn nếu thiếu context.
> Confirm là nơi quyết định output có đủ tin để đi tiếp vào production hay chỉ là demo đẹp.

---

## Bước 8 — Chỉ ra `AI Leverage Point`

| Step | AI nên giúp bằng cách nào? | Vì sao AI hợp ở đây? | Rủi ro chính nếu dùng AI |
|---|---|---|---|
| Prepare | Sinh layout/prototype từ yêu cầu, nhưng chỉ dùng component/token/pattern đã được cho phép | AI giỏi tạo phương án nhanh và kết hợp nhiều ngữ cảnh nếu được cấp design system có cấu trúc | Hallucinate component, tạo pattern ngoài chuẩn, bỏ sót state |
| Confirm | Tự kiểm tra output so với rule: component hợp lệ, token đúng, accessibility cơ bản, state đầy đủ | AI có thể làm reviewer lặp lại trên checklist dài và phát hiện sai lệch | False confidence; bỏ sót lỗi trải nghiệm tinh tế hoặc nghiệp vụ |

### Kết luận nhanh

**AI leverage point quan trọng nhất của dự án tôi là:**  
> Dùng AI như một design-system-aware drafter và reviewer: tạo bản nháp nhanh nhưng bị ràng buộc bởi component, token, rule và ví dụ chuẩn của doanh nghiệp.

**Vì sao không phải ở bước khác:**  
> Define vẫn cần nhiều judgment từ PM/designer; Execute/Monitor liên quan sâu đến codebase và quy trình engineering. Prepare + Confirm là nơi vừa đau, vừa lặp lại, vừa có thể đo được chất lượng cải thiện.

---

## Bước 9 — Viết `Product Hypothesis`

### Bản hypothesis của tôi

> Nếu chúng ta giúp product designer chuyển yêu cầu màn hình mới thành bản nháp giao diện đúng component và tự kiểm rule ở bước Prepare/Confirm,
> bằng cách cho AI truy vấn design system qua MCP hoặc API có cấu trúc,
> thì họ sẽ chuyển từ việc dùng Figma thủ công + prompt rời rạc trong v0/Claude sang một workflow AI có kiểm soát,
> vì họ nhận được tốc độ của AI mà vẫn giữ được độ tin cậy cần cho production.

### Tín hiệu sớm nếu hypothesis này đúng

1. Designer tạo được bản nháp đầu tiên nhanh hơn ít nhất 50% nhưng số lỗi component/token trong review không tăng.
2. Developer giảm số vòng hỏi lại designer về spacing, state, component và handoff spec.

---

## Bước 10 — Liệt kê `Assumptions to Validate`

| Assumption | Vì sao assumption này rủi ro? | Tôi đang có bằng chứng gì? | Cần validate bằng cách nào tiếp theo? |
|---|---|---|---|
| A1: Product designer là job executor đúng | Có thể developer hoặc PM mới là người sẵn sàng dùng và trả tiền hơn | Tài liệu case cho thấy Figma có nhiều non-designer users | Phỏng vấn 5 designer, 5 frontend dev, 3 PM về ai bắt đầu workflow |
| A2: Pain Prepare/Confirm đủ đau và đủ thường xuyên | Nếu team ít màn hình hoặc design system đơn giản, pain không đáng tiền | Case nêu refinement chiếm phần lớn effort sau generation | Quan sát 2 sprint thực tế, đo thời gian từ yêu cầu đến design ready |
| A3: AI có thể truy vấn design system đủ chính xác | Nếu dữ liệu Figma/codebase lộn xộn, AI không có nguồn sự thật tốt | Figma đang định vị MCP/API cho AI agent trong tài liệu case | Prototype với 1 thư viện component thật, đo tỷ lệ dùng đúng component |
| A4: User tin output AI để đưa vào workflow thật | Designer có thể xem AI chỉ là demo generator, không đủ tin để ship | Sự cố Make Design cho thấy trust/QA là rủi ro lớn | Test blind review: AI draft vs human draft, đo lỗi và mức tin cậy |
| A5: Switching khỏi alternative hiện tại đủ hấp dẫn | Figma/v0/Cursor đã quen dùng; thêm tool mới có thể tăng friction | Seat/pricing và prompt rời rạc đang tạo bất mãn | Landing test hoặc concierge pilot với 3 team SaaS |

### Assumption nguy hiểm nhất nếu tôi đang sai

> Assumption nguy hiểm nhất là design system của doanh nghiệp đủ sạch và có cấu trúc để AI truy vấn. Nếu nguồn sự thật không rõ, sản phẩm sẽ chỉ tạo thêm một lớp AI không đáng tin.

---

## Bước 11 — Share trong bàn

### Ghi nhanh sau khi nghe bàn phản biện

| Ý phản biện tôi nghe được | Nó chạm vào phần nào? | Tôi sẽ giữ / sửa gì? |
|---|---|---|
| Có thể frontend developer mới là người cảm nhận pain rõ nhất vì phải sửa code lệch design. | Job executor | Giữ designer là executor chính cho lát cắt thiết kế, nhưng thêm developer là key collaborator cần validate. |
| AI reviewer dễ tạo cảm giác đúng giả nếu rule design system không đủ rõ. | AI leverage point / assumption | Bổ sung assumption về chất lượng nguồn dữ liệu và cần đo false confidence. |
| Nếu chỉ tạo draft trong Figma thì chưa khác nhiều v0; khác biệt phải là governance và rule binding. | Product hypothesis | Nhấn mạnh MCP/API design system và kiểm rule, không chỉ generation. |

---

## Bước 12 — Chốt version cuối sau thảo luận

### Sau khi nghe phản biện, tôi thay đổi gì?

- [x] Giữ nguyên `job executor`
- [ ] Sửa `job executor`
- [x] Giữ nguyên `core JTBD`
- [ ] Sửa `core JTBD`
- [ ] Giữ nguyên `AI leverage point`
- [x] Sửa `AI leverage point`
- [ ] Giữ nguyên `product hypothesis`
- [x] Sửa `product hypothesis`

### Vì sao tôi giữ / sửa?

> Tôi giữ job executor là product designer vì người này trực tiếp chịu trách nhiệm tạo và chuẩn hóa giao diện. Tuy nhiên, tôi sửa leverage point để nhấn mạnh AI không chỉ tạo draft mà phải bị ràng buộc bởi design system có cấu trúc và có bước review rule rõ ràng.

### Version cuối cùng tôi nộp

**Job executor:**  
> Product designer phụ trách thiết kế màn hình trong một team SaaS có design system.

**Core JTBD:**  
> Chuyển một yêu cầu sản phẩm mới thành phương án giao diện nhất quán, có thể kiểm tra và sẵn sàng triển khai trong thời gian ngắn.

**2 bước đau nhất trong workflow:**  
> Prepare và Confirm.

**AI leverage point chính:**  
> AI tạo bản nháp và kiểm tra chất lượng dựa trên component, token, rule, ví dụ chuẩn và design system được truy vấn qua MCP/API.

**Product hypothesis:**  
> Nếu chúng ta giúp product designer tạo và kiểm bản nháp giao diện ở bước Prepare/Confirm bằng AI có ràng buộc design system, họ sẽ chuyển từ prompt rời rạc trong v0/Claude/Cursor sang workflow của nhóm vì nhận được tốc độ của AI mà vẫn giữ được độ tin cậy để đưa vào production.

**Assumption cần validate đầu tiên:**  
> Design system của team mục tiêu có đủ sạch, đủ cấu trúc và đủ quyền truy cập để AI dùng làm nguồn sự thật đáng tin.

---

## Checklist trước khi nộp

- [x] Tôi đã khoanh đúng 1 lát cắt cụ thể của dự án.
- [x] Tôi đã phân biệt được `job executor` với buyer / influencer.
- [x] `Core JTBD` của tôi không nhét solution vào câu.
- [x] Tôi đã viết đủ 3 `job stories`.
- [x] Tôi đã điền `JTBD lite map` và khoanh ra 2 bước đau nhất.
- [x] Tôi đã chỉ ra `AI leverage point` thay vì nhảy thẳng vào feature list.
- [x] Tôi đã ghi rõ `assumptions to validate`.
- [x] Tôi đã sửa version cuối sau khi share trong bàn.
