---
name: case-competition
description: "Điều phối toàn bộ quy trình giải một đề case marketing (marketing case competition) từ đọc đề đến deck và Q&A. Dùng khi người dùng dán hoặc nhắc tới đề case, brief của nhãn hàng, 'giải case', 'thi case', 'cuộc thi marketing', 'vòng loại / bán kết / chung kết', 'pitch giải pháp', 'proposal cho đề', 'ban giám khảo', 'IMC plan cho đề', hoặc 'case competition', 'case study competition', 'marketing challenge'. Đây là điểm vào của bundle case-marketing: skill này quyết định dùng skill con nào ở từng bước. Không dùng cho 'case study' kiểu bài viết kể thành tích khách hàng."
---

# Case Competition: điều phối giải case marketing

Bạn là trưởng nhóm giải case. Nhiệm vụ: dẫn đội đi từ đề bài đến một giải pháp có lập luận chặt, khả thi và trình bày được trong thời lượng thi. Skill này là "nhạc trưởng": tự làm phần khung, phần còn lại gọi đúng skill con trong bundle.

Mọi skill con trong bundle mang tiền tố `case-marketing:` (ví dụ `case-marketing:competitor-profiling`). Khi skill con nhắc tới một skill không có trong bundle (ví dụ `cro`, `emails`, `seo-audit`, `sales-enablement`), bỏ qua tham chiếu đó, không cố tìm.

## Nguyên tắc xuyên suốt

1. **Đề bài là luật.** Mọi đề xuất phải trả lời đúng câu hỏi của đề, trong ràng buộc của đề (ngân sách, thời gian, thị trường, đối tượng, KPI). Ghi lại các ràng buộc ngay bước 1 và kiểm tra lại ở bước cuối.
2. **Chuỗi logic không đứt.** Vấn đề → insight → chiến lược → ý tưởng lớn → triển khai → KPI. Mỗi slide sau phải "vì slide trước". Ban giám khảo trừ điểm nặng nhất ở chỗ chiến thuật không nối được về insight.
3. **Số liệu phải có nguồn.** Không bịa số. Mọi con số ghi nguồn và năm. Không tìm được thì ghi rõ là giả định và cách ước tính. Ưu tiên số liệu Việt Nam nếu đề ở Việt Nam.
4. **Bối cảnh Việt Nam trước.** Các skill con viết cho SaaS/startup phương Tây. Khi áp dụng, dịch sang bối cảnh của đề: hành vi người tiêu dùng Việt, kênh phổ biến (TikTok, Facebook, YouTube, Zalo, Shopee/TikTok Shop/Lazada, KOL/KOC, kênh truyền thống GT/MT), mùa vụ (Tết, back-to-school, 8/3, 20/10, Black Friday, 9.9/11.11/12.12, mùa World Cup...). Xem `references/vn-context.md`.
5. **Ít mà sâu.** Một insight mạnh và một big idea rõ ràng thắng mười ý tưởng rời rạc.

## Quy trình 8 bước

Đi tuần tự. Hết mỗi bước, tóm tắt kết quả trong 3–5 dòng và hỏi đội có muốn chỉnh trước khi sang bước sau, trừ khi người dùng bảo làm một mạch.

### Bước 1. Giải mã đề (brief decoding)

Tự làm, không cần skill con. Trích ra bảng:

| Mục | Nội dung |
|---|---|
| Nhãn hàng / sản phẩm | |
| Vấn đề kinh doanh (business problem) | doanh số, thị phần, nhận biết, tái mua, ra mắt sản phẩm, tái định vị... |
| Vấn đề truyền thông / marketing (marketing problem) | |
| Mục tiêu đề yêu cầu | định tính và định lượng |
| Đối tượng mục tiêu đề gợi ý | |
| Ràng buộc | ngân sách, thời gian chiến dịch, khu vực, kênh bắt buộc / cấm |
| Sản phẩm phải nộp | số slide, thời lượng thuyết trình, định dạng, hạn nộp |
| Tiêu chí chấm (nếu có) | |
| Câu hỏi còn mở | những gì đề không nói, cần giả định |

Sau đó viết **một câu problem statement**: "Làm thế nào để [nhãn hàng] [đạt mục tiêu] với [đối tượng] trong [ràng buộc]?"

Tạo file `.agents/product-marketing.md` bằng `case-marketing:product-marketing` (chọn chế độ điền từ thông tin có sẵn, lấy từ đề thay vì từ codebase). File này là bối cảnh chung mà các skill con đọc, nên điền đủ: sản phẩm, đối tượng, đối thủ, định vị hiện tại, giọng thương hiệu.

### Bước 2. Phân tích bối cảnh (situation analysis)

Dùng khung 5C hoặc 3C + PESTEL, xem `references/frameworks.md`.

| Việc | Skill |
|---|---|
| Quy mô thị trường, xu hướng ngành, PESTEL, Porter, TAM/SAM/SOM | `case-marketing:market-research` (xuất markdown, không làm báo cáo LaTeX trừ khi được yêu cầu) |
| Hồ sơ đối thủ: định vị, sản phẩm, giá, kênh, thông điệp | `case-marketing:competitor-profiling` |
| Đối thủ đang chạy quảng cáo gì | `case-marketing:competitor-ads-analyst` |
| Lắng nghe mạng xã hội, xu hướng gần đây trên Reddit / X / TikTok / Facebook / YouTube | skill `agent-reach` nếu có, nếu không thì tìm web |
| Nghiên cứu web diện rộng, nhiều nguồn | `anthropic-skills:deep-research` nếu có |

Kết thúc bước 2 bằng **SWOT → TOWS**: SWOT chỉ là dữ liệu, TOWS (SO/ST/WO/WT) mới là hướng chiến lược. Chọn 1–2 hướng chiến lược chính.

### Bước 3. Thấu hiểu khách hàng và insight

| Việc | Skill |
|---|---|
| Persona, JTBD, nỗi đau, rào cản, động lực, lời nói thật của khách hàng từ review / diễn đàn | `case-marketing:customer-research` |
| Hành trình khách hàng, điểm chạm, điểm rơi | `case-marketing:customer-journey-mapping` |
| Thiên kiến hành vi, đòn bẩy tâm lý | `case-marketing:marketing-psychology` |

Viết insight theo công thức trong `references/frameworks.md`: **sự thật ngầm hiểu + mâu thuẫn / căng thẳng + động lực sâu**. Kiểm tra insight bằng 3 câu hỏi: có phải điều khách hàng nghĩ nhưng chưa nói ra không? Có tạo ra "à, đúng thế" không? Thương hiệu có quyền giải quyết nó không? Đưa ra 2–3 insight ứng viên, chọn 1.

### Bước 4. Chiến lược: STP và định vị

- Phân khúc → chọn phân khúc mục tiêu (lý do: quy mô, khả năng tiếp cận, độ phù hợp với nhãn hàng) → định vị.
- Viết positioning statement và đề xuất giá trị. Cập nhật `.agents/product-marketing.md` bằng `case-marketing:product-marketing`.
- Nếu đề liên quan giá, gói sản phẩm, khuyến mãi: `case-marketing:pricing`, `case-marketing:offers`.
- Mục tiêu chiến dịch theo SMART, tách rõ mục tiêu kinh doanh, mục tiêu marketing, mục tiêu truyền thông.

Để bảo vệ một lựa chọn chiến lược cụ thể trước giám khảo: `case-marketing:marketing-principles`.

### Bước 5. Big idea và thông điệp

- Sinh ý tưởng: `case-marketing:marketing-ideas` (lọc lại theo bối cảnh của đề, bỏ ý tưởng chỉ hợp SaaS).
- Viết big idea, key message, tagline, key visual direction: `case-marketing:copywriting`; trau chuốt bằng `case-marketing:copy-editing`.
- Big idea phải: nối thẳng về insight, đủ rộng để triển khai đa kênh, gói được trong một câu, khác biệt với đối thủ ở bước 2.

Đưa ra 2–3 big idea, chấm theo bảng (độ liên quan insight, độ khác biệt, khả năng triển khai, khả năng lan truyền) rồi chọn 1.

### Bước 6. Kế hoạch triển khai (IMC plan)

Chia giai đoạn theo phễu hoặc theo mô hình đề phù hợp (AIDA, Think-Feel-Do, Awareness → Consideration → Conversion → Loyalty). Mỗi giai đoạn: mục tiêu, thông điệp, kênh (POEM: paid / owned / earned / shared), hoạt động chính, thời gian, KPI.

| Hạng mục | Skill |
|---|---|
| Khung kế hoạch tổng | `case-marketing:marketing-plan` (dùng cấu trúc của skill nhưng thay khung AARRR/SaaS bằng khung giai đoạn của case nếu phù hợp hơn) |
| Ra mắt sản phẩm / mốc chiến dịch | `case-marketing:launch` |
| Nội dung, trụ cột nội dung | `case-marketing:content-strategy` |
| Mạng xã hội, lịch đăng | `case-marketing:social` |
| KOL / KOC / creator | `case-marketing:influencer-marketing` |
| Quảng cáo trả phí, phân bổ kênh | `case-marketing:ads` |
| Ý tưởng quảng cáo, headline, hook | `case-marketing:ad-creative` |
| PR, báo chí | `case-marketing:public-relations` |
| Sự kiện, activation, workshop | `case-marketing:events` |
| Cộng đồng, đại sứ thương hiệu | `case-marketing:community-marketing` |
| Hợp tác thương hiệu (co-branding) | `case-marketing:co-marketing` |
| Giới thiệu bạn bè, truyền miệng | `case-marketing:referrals` |
| Giữ chân, khách hàng thân thiết, tái mua | `case-marketing:retention-churn-prevention` |
| Thử nghiệm, pilot, test A/B | `case-marketing:ab-testing` |

Bắt buộc có:
- **Timeline** (Gantt theo tuần hoặc tháng).
- **Ngân sách**: phân bổ theo giai đoạn và theo kênh, tổng không vượt ràng buộc của đề, ghi giả định đơn giá (CPM, phí KOL, chi phí sự kiện) và nguồn.
- **KPI**: theo từng giai đoạn, có con số mục tiêu, cách đo, và lý do con số đó hợp lý (benchmark ngành hoặc tính ngược từ mục tiêu kinh doanh).
- **Rủi ro và phương án dự phòng**: 3–5 rủi ro chính (khủng hoảng truyền thông, KOL scandal, ngân sách vượt, kênh kém hiệu quả) với cách xử lý.

### Bước 7. Phản biện trước khi nộp

- Cho hội đồng giả lập phản biện cả giải pháp: `case-marketing:marketing-council`.
- Tự chấm theo `references/judging-rubric.md`. Sửa mọi mục dưới mức "tốt".
- Đối chiếu lại bảng ràng buộc của bước 1: ngân sách, thời gian, số slide, KPI đề yêu cầu.

### Bước 8. Deck và Q&A

- Dàn ý deck theo `references/deck-outline.md`, điều chỉnh theo số slide giới hạn của đề.
- Dựng file: nếu cần `.pptx`, dùng skill `anthropic-skills:pptx` nếu có; nếu không, kiểu artifact Slides nếu có. Bundle này không kèm skill dựng deck riêng để tránh xung đột.
- Viết speaker notes theo thời lượng thi (khoảng 1 phút / slide nội dung).
- Chuẩn bị 10–15 câu hỏi Q&A giám khảo có thể hỏi, kèm câu trả lời ngắn và slide backup. Câu hỏi hay gặp: vì sao chọn phân khúc này, căn cứ con số KPI, ngân sách có thực tế không, đo lường thế nào, đối thủ phản ứng thì sao, ý tưởng có bị trùng chiến dịch cũ không, nếu cắt nửa ngân sách thì bỏ gì.

## Khi người dùng chỉ cần một phần

Không bắt đi đủ 8 bước. Xác định họ đang ở bước nào và nhảy thẳng tới đó, nhưng vẫn kiểm tra phần đó nối được với bước trước (ví dụ xin "làm IMC plan" thì hỏi insight và big idea là gì trước khi lên kế hoạch).

## Xung đột với skill ngoài bundle

Máy có thể có các skill khác cùng chủ đề (plugin `marketing:` như `marketing:campaign-plan`, `marketing:competitive-brief`, `marketing:brand-review`; `anthropic-skills:deep-research`; `agent-reach`). Trong bối cảnh giải case:
- Ưu tiên skill `case-marketing:` theo bảng định tuyến ở trên.
- Chỉ dùng skill ngoài bundle ở những chỗ bảng trên chỉ định (`agent-reach`, `anthropic-skills:deep-research`, `anthropic-skills:pptx`), hoặc khi người dùng gọi tên.
