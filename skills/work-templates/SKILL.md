---
name: work-templates
description: Sinh nội dung từ các template lặp lại Dũng dùng hằng tuần — gợi ý 5-7 actions tuần này (đẩy IDP + đạt đánh giá 4★ Vượt kỳ vọng + tiến tới Senior 2026), báo cáo tuần (OFFICIAL iKame 6 sections), IDP plan, học theo lộ trình KMP/CMP/SwiftUI, tìm tài liệu Medium. Phân tích EKS H1, 17 gap behaviors silent, KS đang lag để chỉ ra actions cụ thể, có effort estimate, evidence dự kiến, priority P0/P1/P2. Sử dụng MẶC ĐỊNH khi Dũng yêu cầu "gợi ý action tuần này", "tuần này nên làm gì", "action plan EKS", "đẩy IDP tuần", "làm gì để 4 sao", "làm gì để lên senior", "viết báo cáo tuần", "weekly report", "làm IDP", "kế hoạch học", "lộ trình KMP", "tìm tài liệu Medium". Kích hoạt CẢ KHI Dũng chỉ thả vào 1 list đầu việc work chính hoặc 1 file/screenshot Jira/Asana — đó là tín hiệu cần gợi ý actions bổ sung.
---

# Work Templates — gợi ý actions tuần, báo cáo tuần, IDP, learning plan

Skill này gói các template lặp lại của Dũng để tạo nội dung nhanh và nhất quán, đồng thời **phân tích EKS H1-2026 + 17 gap behaviors** để gợi ý actions cụ thể đẩy Dũng đến đánh giá 4★ Vượt kỳ vọng và Senior promotion 2026.

## Khi nào dùng skill này

Kích hoạt khi Dũng yêu cầu một trong các tác vụ lặp lại sau:
- **Gợi ý actions tuần này** — đây là use case chính, mục tiêu đẩy IDP/EKS/Senior
- Soạn báo cáo tuần (weekly report)
- Lập / cập nhật IDP (Individual Development Plan)
- Lên kế hoạch học tuần / tháng (KMP, CMP, SwiftUI...)
- Tìm tài liệu Medium phù hợp lộ trình học

## Quy trình chung

1. **Xác định template phù hợp** (weekly actions / weekly report / IDP / learning plan / Medium curation)
2. **Đọc context bắt buộc** trước khi điền:
   - `personal-profile/references/eks-h1-2026.md` — EKS hiện tại + tiến độ KS
   - `personal-profile/references/assessment-result.md` — 17 gap behaviors
   - `personal-profile/references/weekly-reports-h1-2026.md` — track record gap frequency
   - (Cho weekly actions) `personal-profile/references/senior-promotion-playbook.md`
3. **Đọc file template tương ứng** trong `references/`
4. **Hỏi Dũng các thông tin còn thiếu** (tuần nào, work chính, constraint). Nếu Dũng có file/ảnh đính kèm — đọc trước, dùng làm input chính, chỉ hỏi khi thiếu critical info. **Tối đa 1 lượt hỏi, ≤4 câu**.
5. **Điền template**, kết hợp brand-voice của iKame nếu nội dung sẽ gửi đi nội bộ

## Các template có sẵn

- `references/weekly-plan-template.md` — **MỚI**. Weekly Actions Suggester (advisor mode): phân tích KS lag + gap silent + cơ hội tuần, gợi ý 5-7 actions có effort/evidence/priority P0/P1/P2 để đẩy 4★ Vượt kỳ vọng + Senior. **KHÔNG** kê hộ lịch — Dũng tự pick 3-5 actions fit lịch thật. Đọc khi Dũng yêu cầu "gợi ý action tuần này", "tuần này nên làm gì để 4 sao".
- `references/weekly-report-template.md` — Template báo cáo tuần CHÍNH THỨC iKame với 6 sections: IKAME WHAT / IKAME HOW / IKAME LEVEL UP / Tồn đọng & Rủi ro / Cần hỗ trợ / Tự đánh giá. Tự động tag EKS + 17 gap behaviors.
- `references/idp-template.md` — Khung IDP quarterly với cột Mục tiêu / Kết quả / Lộ trình / Đo lường
- `references/learning-plan-template.md` — Plan học weekly cho KMP/CMP/SwiftUI
- `references/medium-curation.md` — Hướng dẫn cách tìm và đánh giá bài Medium theo lộ trình

## Nguyên tắc khi điền template

- Mỗi mục có **mục tiêu định lượng** (xong cái gì, ship cái gì), không "tìm hiểu về X"
- Mỗi tuần có **1 lesson learned cụ thể** — không "học được nhiều thứ"
- Mỗi quý có **stretch goal** song song với commitment goal (tinh thần Level-up)
- Khi báo cáo blocker: kèm hướng đã thử + đề xuất next step (tinh thần Autonomy)

## Nguyên tắc đặc biệt khi gợi ý weekly actions

Khác với việc lên plan tuần đầy đủ (Dũng tự làm trong Jira/Notion/Calendar), weekly actions suggester chỉ làm 1 việc: **phân tích bức tranh lớn (EKS + IDP + Senior) và gợi ý 5-7 actions BỔ SUNG tuần này** để Dũng tiến tới mục tiêu.

Skill phải đảm bảo:
1. **Phân biệt rõ "work chính" và "actions bổ sung"** — work chính là phase/feature đã có trong Jira, actions bổ sung là evidence cho gap behaviors + KS lag
2. **Có ≥1 action P0 push KS đang lag** (snapshot 5/2026: E1 KS1, E2 KS2, E3 KS2 đang lag)
3. **Có ≥1 action chạm gap silent 3+ tuần** (đọc weekly-reports-h1 để xác định)
4. **Có ≥1 action stretch P1** — điều kiện cần cho rating 4★ Vượt kỳ vọng (không có stretch = chỉ Làm tốt)
5. **Effort tổng ≤ 25% capacity tuần** (~6-8 giờ) — Dũng còn 75% cho work chính + flex
6. **Mỗi action có evidence "physical"** (PR / Notion doc / screenshot) — không "đã trao đổi", "đã suy nghĩ"
7. **Mix priority hợp lý**: 2-3 P0 + 2-3 P1 + 0-2 P2 (không quá P0 → áp lực, không quá P2 → mất focus)
