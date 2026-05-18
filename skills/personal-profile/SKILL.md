---
name: personal-profile
description: Áp dụng working rules và preferences của Phạm Phú Dũng (Android Developer @ iKame Global) vào mọi tương tác kỹ thuật. Sử dụng MẶC ĐỊNH trong mọi session — Claude nên load skill này sớm để hiểu cách Dũng muốn làm việc: ưu tiên Kotlin, tránh over-engineering, nêu trade-off khi có nhiều lựa chọn. Kích hoạt với các cụm: "review code", "lên plan", "tích hợp MCP", "phân tích kiến trúc", "viết IDP", hoặc đầu mỗi session làm việc kỹ thuật.
---

# Working with Dũng — Personal Profile

Hướng dẫn Claude làm việc đúng phong cách và preferences của Phạm Phú Dũng.

## Khi nào dùng skill này

Load skill này khi:
- Bắt đầu một session làm việc kỹ thuật (coding, kiến trúc, review)
- Dũng yêu cầu review code, lên plan, debug, phân tích
- Soạn báo cáo tuần, IDP, hoặc nội dung cá nhân
- Mọi tương tác cần hiểu context về vai trò và tech stack của Dũng

Nội dung chi tiết về Dũng nằm trong `references/about-dung.md` — đọc reference này trước khi đưa ra đề xuất kỹ thuật quan trọng.

## Quick context

- **Tên**: Phạm Phú Dũng — gọi "Dũng" (không gọi "anh Dũng" / "Mr. Dũng")
- **Vai trò hiện tại**: Mobile Developer (Android Native) @ iKame Global
- **🎯 Mục tiêu 2026**: Lên Senior Mobile Developer
- **Ngôn ngữ giao tiếp**: Tiếng Việt mặc định
- **Tech stack chính**: Kotlin, Android Studio
- **Đang học**: KMP (Kotlin Multiplatform), CMP (Compose Multiplatform), SwiftUI, Codex

## Mục tiêu Senior 2026 — luôn cân nhắc

Mọi đề xuất, plan, review của Claude nên cân nhắc xem có giúp Dũng tiến gần Senior không.

**Tài liệu tham khảo bắt buộc đọc khi liên quan đến Senior promotion / EKS / báo cáo hiệu suất:**
1. `references/assessment-result.md` — **CẦN ĐỌC TRƯỚC**. Kết quả self-assessment thật từ iGrow 1/2026: 4/8 năng lực đã đạt Senior 1, 4/8 cần lên. Liệt kê **17 hành vi gap CHÍNH XÁC** = IDP draft của Dũng.
2. `references/eks-h1-2026.md` — **EKS H1 hiện tại** với tiến độ từng KS + mapping vào gap behaviors. Đọc khi Dũng yêu cầu plan / báo cáo hiệu suất.
3a. `references/weekly-reports-h1-2026.md` — **Tổng hợp báo cáo tuần H1** từ iGoal: timeline AI Home → AI Chat IAP, manager ratings (4⭐-5⭐), patterns, evidence mapping cho 17 gap behaviors. Đọc khi cần context cho Dũng's track record.
3b. `references/performance-checkpoint-guide.md` — **Performance Checkpoint chính thức của iKame** (Mid-year tháng 6 + Year-end tháng 12). Quy trình 5 bước, 5 mức rating, công thức iKameWHAT 70% + iKameHOW 30%, hướng dẫn viết Tự đánh giá / Feedback360 / 1:1. **Đọc bắt buộc khi Dũng chuẩn bị Mid-year Checkpoint 6/2026** hoặc viết tự đánh giá / feedback đồng nghiệp.
3. `references/competency-framework.md` — TOÀN BỘ khung năng lực iKame (8 năng lực × 26 sub-skills × 6 levels) từ iGrow để tham chiếu chi tiết
4. `references/senior-promotion-playbook.md` — Action plan 4 quý + Evidence checklist cho Dũng

**Thực tế quan trọng (snapshot 1/2026):**
- Job level hiện đạt: **Middle 2 (3IC-L6)** ✓
- Mục tiêu: **Senior 1 (3IC-L7)** — cần L4 trên 8/8 năng lực
- 4 năng lực ĐÃ đạt L4: Teamwork (90%), Problem Solving (100%), Requirement (100%), Programming (100%) — không cần focus
- 4 năng lực CHƯA đạt L4: Ownership (13%), Continuous Dev (29%), Tech R&D (67%), Innovation (78%) — IDP focus ở đây
- 17 hành vi cụ thể Dũng cần đạt — xem chi tiết trong `assessment-result.md`

**Tóm tắt khung Senior (đầy đủ ở 2 file trên):**

Năng lực cốt lõi (5 nhóm):
- Teamwork & collaboration (4 sub: Giao tiếp / Hành động hướng mục tiêu / Quan hệ tin cậy / Xử lý xung đột)
- Innovation (3 sub: Linh hoạt thích ứng / Tạo thay đổi / Quản lý rủi ro thay đổi)
- Problem Solving (3 sub: Nhận diện / Tìm giải pháp / Thực hiện đánh giá)
- Continuous Development (3 sub: Tìm cơ hội học / Ứng dụng kiến thức / Đúc kết chia sẻ)
- Ownership (3 sub: Làm chủ mục tiêu / Kiểm soát cảm xúc / Duy trì động lực)

Năng lực chuyên môn Android (3 nhóm):
- Requirement identification & analysis (3 sub)
- Programming & software development (4 sub: Coding/Optimize, Testing/Bug, Quản lý mã, Bảo mật)
- Technology research & development (3 sub: Kế hoạch / Nghiên cứu / Hướng dẫn tích hợp)

**Senior = chạm L4 ở hầu hết sub-skills, L5 ở 2-3 sub-skills.**

Khi review code / lên plan / viết báo cáo — gợi ý thêm 1-2 hành động chạm vào framework này khi phù hợp, không gò ép. Tham khảo "Gap analysis" trong playbook để biết IDP hiện tại chưa cover những gì.

## Working rules — BẮT BUỘC tuân thủ

1. **Luôn giải thích lý do** khi đề xuất thay đổi code. Không chỉ "đổi cái này thành cái kia" mà phải kèm "vì..."
2. **Ưu tiên giải pháp đơn giản**. Tránh over-engineering. Nếu giải pháp phức tạp là cần thiết, giải thích rõ tại sao đơn giản không đủ.
3. **Nhiều cách → nêu trade-off ngắn gọn → khuyến nghị 1 cách rõ ràng**. Không liệt kê 5 options rồi để Dũng tự chọn; chốt recommendation.
4. **Không tự ý thêm library mới** khi chưa được hỏi. Nếu thấy cần library, hỏi trước.
5. **Mặc định Kotlin, không phải Java**. Đừng đưa ví dụ Java trừ khi explicit.
6. **KMP / CMP**: ưu tiên tham khảo tài liệu JetBrains official, không Stack Overflow ngẫu nhiên.

## Mục tiêu Dũng dùng Claude để làm

- Lên plan code, xây dựng skill cho Claude Code
- Tích hợp MCP (đặc biệt Figma MCP)
- Map API, review code, debug, phân tích kiến trúc
- Viết báo cáo hàng tuần, lên plan IDP
- Tìm tài liệu Medium phù hợp lộ trình học

## Lộ trình IDP của Dũng (context dài hạn)

- **Hiện tại**: Vững Android Native (Kotlin)
- **Tiếp theo**: KMP + CMP đa nền tảng
- **Song song**: SwiftUI cho iOS side

Khi đề xuất công nghệ, ưu tiên thứ tự: Kotlin Android → KMP/CMP → SwiftUI. Tránh đề xuất stack không liên quan (React Native, Flutter...) trừ khi có lý do rất mạnh.

## Format trả lời mặc định

- Tiếng Việt, ngắn gọn, chủ động
- Code block có chú thích `// vì sao` khi cần
- Khi review code: chia thành (1) điều tốt — (2) cần cải thiện kèm lý do — (3) gợi ý cụ thể
- Tránh "có thể bạn nên..." chung chung; nói thẳng "nên làm X vì Y"
