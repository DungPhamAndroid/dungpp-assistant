# Weekly Reports Summary — H1 2026

> Tổng hợp các báo cáo tuần của Dũng từ iGoal. Nguồn: <https://igoal.ikameglobal.com/eks/personal?reportId=f45da75b-b234-4e8f-a349-61234f2231dc>
> Cập nhật: 5/2026. 8/16 báo cáo fetch được, 8 báo cáo cũ (giữa Feb - đầu Mar) iGoal SPA chưa cho re-fetch.

## Timeline & key achievements

### Tháng 1 — Báo cáo W4 (02/02/2026)
**Sản phẩm**: AI Home
- Tối ưu tốc độ load ảnh thumbnail: **1.6s → 0.15s** (cải tiến đáng chú ý)
- Clear hết bug Asana trước đó
- Nghiên cứu, demo ML Kit Image Labeling cho AI Home (loại phòng, suggest đồ dùng)
- Hỗ trợ PM mới hiểu app & CMS
- Cảm hứng từ chia sẻ anh Quyết trong YEP

### Tháng 2 W2-W3, Tháng 3 W2, Check-in 11/3
*(Báo cáo còn lại chưa fetch được. Đề xuất Dũng tự bổ sung khi có thời gian)*

### Tháng 2 — Báo cáo W4 (02/03/2026)
**Sản phẩm**: AI Home — tag EKS1-KS1, EKS2-KS1

**Kết quả (IKAME WHAT)**:
- Rà lại UI flow Remove object, Replace object — fix bugs QA
- Optimize database
- Optimize Remove object (sau khi rà soát thấy data input chưa đúng → chủ động fix)
- Fix bug Styles trong Regenerate (duplicate do CMS) + Surprise Color hiển thị cuối
- Check remote config cho A/B testing khóa tính năng
- Tìm hiểu cơ chế retry của **OTHTTP** support mạng yếu
- Nghiên cứu kịch bản notification → define remote code, logic để support Hiếu

**Cách làm (IKAME HOW) — heavy ownership**:
- Chủ động rà soát + optimize ngoài kế hoạch team (Database, Remove Object, Styles, Surprise Color)
- Recheck remote config giúp PM trước A/B test
- Xem dashboard Server thấy lỗi Connection Error (1003, 1005) → tự research → apply OTHTTP retry
- Hỗ trợ Hiếu kịch bản Notification: verify kịch bản, lên remote config, bàn giao cho Hiếu thực thi
- Chủ động cùng PM, BE check lỗi API

**Level up (IKAME LEVEL UP)**:
- OTHTTP Connection Error + cách giải quyết
- Mindset mới: quan tâm **SUB Retention Rate** hơn RR đơn thuần
- **IDP tag (theo template iKame)**: "Nghiên cứu và phát triển công nghệ mục 4.3" — Tech R&D L4 #4.3 (Phân tích, nghiên cứu, thiết kế, tích hợp nhiều công nghệ)

**Tồn đọng & rủi ro**:
- Process generate lâu → đề xuất chuyển sang service để chạy ngầm, giảm lỗi 499 Client Closed Request

**Cần hỗ trợ**:
- Manager: "Đầu việc client đang mỏng" — RAISE: nguồn lực Android có thể underutilized vs iOS team

**Self-rating**: Làm tốt (bám OUTPUT & EKS1 & EKS2)

### Tháng 3 — Báo cáo W1 (07/03/2026)
**Sản phẩm**: AI Home — tag EKS1, EKS2

**Kết quả (IKAME WHAT)**:
- Optimize: giảm lượng user cancel khi phải đợi lâu
  - Chuyển Generate Process sang service
  - Chuyển Regenerate Process sang service
  - Triển khai Minimize
  - Rà soát Sankey

**Cách làm (IKAME HOW) — đột phá về Problem Solving + Influence**:
- **Tự chủ**: Rà soát Sankey phát hiện luồng Onboarding → IAP có vấn đề khiến user không vào được Home ở session 1 → chủ động push team fix
- **Phối hợp + thuyết phục**: PM và dev phụ trách Onboarding/IAP ban đầu đánh giá là lỗi nhỏ → Dũng phân tích đưa giải pháp → thuyết phục được mọi người triển khai sửa ⭐ Đây là evidence rất mạnh cho **Innovation L4 + Ownership L4 (tư vấn đồng nghiệp)**
- **Hỗ trợ Hiếu**: notification + IAP v3, góp ý khi fix reject, góp ý remote config cho IAP v3

**Level up (IKAME LEVEL UP)**:
- Short Polling vs Long Polling (foundation cho tuần sau chuyển AI Home sang short polling)

**Cần hỗ trợ**:
- ⭐ **Manager: "Đưa ra các UT trong IDP"** — Đạt yêu cầu Dũng clarify deliverables / use cases cụ thể cho IDP. RAISE: cần follow up với DM để chốt format IDP

**Self-rating**: Làm tốt

### Tháng 3 — Báo cáo W3 (21/03/2026) — ⭐ Big leap: Tech Lead transition
**Sản phẩm**: AI Home — tag EKS1, EKS2

**Kết quả (IKAME WHAT)**:
- **Fix crash firebase**: 99.6% → **99.89%** (version 1.0.7) — metric đáng chú ý
- Đóng gói version Minimize với Job
- Triển khai optimize UI/UX mới: Interior, Exterior, Garden, Reference, Edit (Remove, Replace, Paint Wall, Floor), Detail, Regenerate cho all features
- **Product/Tech Lead duties**:
  - Lên plan phase optimize UI: chia task, estimate, asana cho team
  - Đốc thúc tiến độ anh em dev, điều chỉnh nguồn lực khi Hiếu nghỉ phép
  - **Onboard anh em mới**: đưa yêu cầu tối ưu, lưu ý khi triển khai luồng
  - Trao đổi với BE, UI/UX cho phù hợp với sản phẩm
  - Theo dõi chỉ số bản mới + đưa timeline phase mới
  - Support team điều tra alert Slack
  - Review code

**Cách làm (IKAME HOW) — heavy team coordination**:
- **Tự chủ**:
  - Phát hiện free crash giảm nhẹ → fix update cùng minimize → 99.89%
  - Bản minimize có side effects → theo dõi tiến độ roll, trao đổi PM xử lý ngay
  - Tracking API thay đổi → trao đổi BI để kéo số ra dashboard
  - **Điều phối khi có thêm dev**: đảm bảo không dẫm chân
  - Thứ 6 có 2 cuộc họp + 1 sharing phát sinh → OT tối thứ 6 vẫn ship đúng plan
- **Phối hợp**:
  - UI/UX: đảm bảo không sót màn hình, đưa priority để dev start sớm không phải chờ
  - Góp ý UI/UX chỗ chưa phù hợp
  - Phối hợp dev Android + iOS đảm bảo luồng chung
  - PM: thay đổi CMS phù hợp UI mới

**Level up (IKAME LEVEL UP)**:
- **Kiến thức mới**:
  - Reverse engineering: tools, chức năng, cách làm (qua sharing team android)
  - Hiểu rõ hơn về production numbers (qua sharing anh ĐạtT)
- **Kỹ năng**: Phân phối công việc cho nhiều dev → cần tính thêm time cho phối hợp, họp, vấn đề phát sinh
- **Vấn đề khó giải quyết**: Khi nguồn lực dev nhiều → giải pháp:
  1. Thông tin rõ ràng khi ae bắt đầu code
  2. Làm việc với UI/UX có design sẵn
  3. Bám sát ae khi triển khai

**Self-rating**: Làm tốt (Đảm bảo tốt tiến độ bám sát EKS1)

⭐ **Insight quan trọng**: Tuần này là **bước chuyển từ IC sang Tech Lead** — Dũng bắt đầu plan & điều phối nhiều dev, onboard người mới, review code. Đây là evidence rất mạnh cho **Ownership L4 #4.2 (quản lý nhiều mục tiêu phức tạp)** và **L4 #4.3 (tư vấn/hướng dẫn đồng nghiệp)**.

### Tháng 3 — Báo cáo tức thời 25/03/2026
**Sản phẩm**: AI Home New UI
- 100% phase dev xong, 99% test
- Block: source anim chưa đủ, CMS chưa xong, API webhook lỗi
- Manager (Đạt) ack: "Okie anh nắm thông tin nhé"

### Tháng 3 — Báo cáo W4 (27/03/2026) — ⭐ 4 sao từ Manager
**Sản phẩm**: AI Home New UI (Big Update)
- Code & Optimize hoàn thiện version New UI (api design v5, feature v2)
- Bổ sung Reference Style (Wall, Floor, Replace), Add Photo Guide, Preview reference photo
- **EKS2 launched**: Buổi 1:1 đầu tiên với Hiếu
  - Chia sẻ mindset Ownership
  - Đẩy Hiếu tự tin hơn, mạnh dạn hơn với role PIC
  - Định hướng giao Hiếu PIC AI Home
  - Góp ý kỹ năng giao tiếp (chậm lại để lắng nghe)
- Cải tiến quy trình: Tạo flow QA expect ngoài scope → PM → cân rủi ro → dev triển khai

**Manager feedback (Trần Đạt, 4⭐)**:
> Phối hợp tốt cho 4 Dev Android, chủ động push các bộ phận khác, dẫn dắt kế cận (chia sẻ mindset cho Hiếu). "Mong tương lai có nhiều bạn kế cận có tinh thần như em"

### Tháng 3 — Check-in 27/03 (08/04/2026)
- Mục tiêu EKS2: giúp Hiếu làm PIC AI Home, thực hành các trách nhiệm
- Next: trao quyền, giao task khó, thúc đẩy Hiếu thay đổi tư duy

### Tháng 4 — Báo cáo W1 (05/04/2026) — ⭐ 5 sao XUẤT SẮC từ Manager
**Sản phẩm**: AI Home (release new UI), bắt đầu phase Cost Estimate
- Tối ưu hóa home (anim, mockdata), Inspiration, Input UX, business logic generate, Tracking
- Migrate CMS sang Production an toàn
- Trace bug AI response chậm + 2 edge case BE/Client
- OT đến 2h30 sáng fix bug release
- **EKS2**: Hướng dẫn Hiếu PIC — tạo task Asana, giao tiếp PM, break task, estimate
- Tiếp cận lần đầu KMP & CMP qua sharing của ChungHA

**Manager feedback (Trần Đạt, 5⭐ — Xuất sắc)**:
> Càng thể hiện rõ tinh thần owner của sản phẩm, không chỉ Android mà còn support BE, QA, PM, iOS. "Luôn giữ tinh thần để ae cùng xây dựng BU, cty lớn mạnh"

### Tháng 4 — Báo cáo W2 (10/04/2026)
**Sản phẩm**: AI Home phase Cost Estimate
- Upload File, Room Type/Location/Size Input, Proposed Budget, Change Structure Level, Labour Costs
- Tích hợp API: GET question, Upload File, Generation Review Scope
- **Cải tiến quy trình**: Thiết kế Mock Data → gửi đồng loạt iOS & BE → unblock client từ ngày đầu
- Hỗ trợ Hiếu release thành công bản IAP v4
- **TRY thành công**: Trao quyền hoàn toàn cho Hiếu (tự họp BI, tự estimate) → Worked
- **AI tools đầu tiên**: Claude Code + MCP plugin → tăng tốc độ code logic và UI

**Insight quan trọng**: "Chuyển từ ôm đồm sang delegation — lùi 1 bước, helicopter view, dọn đường"

### Tháng 4 W3 (18/04/2026)
*(Chưa fetch được — đề xuất bổ sung)*

### Tháng 4 — Báo cáo W4 (26/04/2026) — ⭐ 4 sao "Vượt kỳ vọng"
**Sản phẩm**: AI Chat IAP DeepSearch Phase 2 + IAP Remote Config
- Splash/Onboard animation update
- **Đóng gói module IAP Remote Config thành chuẩn chung** (tái sử dụng cho các app khác)
- DeepSearch Phase 2: refactor navigation, Client Database, History flow, 5 APIs mới
- **Cross-project**: Phát hiện tỷ lệ retry trên 1 ID rất lớn ở AI Home → raise issue
- **Bối cảnh khó khăn**: Android effort 100% 1 mình + Hiếu 20%, trong khi iOS 3 dev
- OT để đảm bảo timeline, fix crash sáng thứ 7 sau release
- **AI workflow đột phá**: Claude Code + VS Code lập plan trước → giảm 50% thời gian prompt, DeepSearch Phase 2 dev chỉ 1.5 ngày

**Manager feedback (Trần Đạt, 4⭐)**:
> Đóng góp hệ thống (reusable module, AI workflow), tạo cải tiến rõ ràng. Manager note: sẽ ngồi với PM tháng 5 để tìm phương án workload không bị miss require.

### Tháng 5 — Báo cáo W2 (09/05/2026) — ⭐ 4 sao
**Sản phẩm**: AI Chat IAP — Đóng gói Phase DeepSearch + Phase Đồng bộ màu
- Refactor toàn bộ DeepSearch (code logic, follow question, history)
- Đồng bộ màu cho Common Views, Tabs Main, các features (AI Avatar, Sticker, Logo, Document, Link)
- **Vượt timeline 2 ngày**
- **Custom AI Skill** đầu tiên: tự động hóa việc map màu — "lập trình quy tắc cho AI xử lý task đặc thù"
- Manage technical debt: refactor cấu trúc cũ cồng kềnh thay vì code đè

**Manager feedback (Trần Đạt, 4⭐)**:
> Vượt tiến độ, ownership, cải tiến (Custom AI Skill nên share lên cho nhóm Dev). "Tăng mức độ contribute"

### Tháng 5 — Báo cáo W3 (17/05/2026) — ⭐ Security incident response + Multi-role coverage
**Sản phẩm**: AI Chat IAP — Phase Update App Color — tag EKS1 KS1

**Kết quả (IKAME WHAT)**:
- Hoàn thiện Phase Update App Color đúng cam kết với PM (update API, animation, fix toàn bộ QA bug Asana)
- **Đóng góp hệ thống — Cover roles**:
  - Chủ động đảm nhận triển khai **CMS** thay PM (PM bận đi học)
  - Chủ động **test API** mới vì QA không nhận được info từ PM
  - → Đảm bảo luồng không block/đứt gãy

**Cách làm (IKAME HOW) — peak Ownership + Security mindset**:

Bridge roles (lấp khoảng trống nhân sự):
- (1) Triển khai CMS thay PM
- (2) Test API mới thay QA, confirm/trade bug với BE/AI

**🛡️ Security incident handling — Star moment**:
- API IAP bị hack → phối hợp BE tìm root-cause
- Tự xây dựng matrix các abuse cases
- **Không dừng ở phương án fix của BE** — chủ động viết code mô phỏng spam request để stress-test
- Phát hiện phương án "chặn theo path" vẫn có lỗ hổng → **đề xuất phương án thay thế chặt chẽ hơn**, vá kịp thời trước release
- **Impact: tránh mất thêm $1k vào ngày hôm sau**

Mentor Hiếu sâu hơn:
- Rà soát code Hiếu, đưa feedback và hướng xử lý cho cả những lỗi QA chưa kịp log
- → Hiếu đóng defect nhanh, tránh re-open

TRY:
- Try 1 (Worked): Hỗ trợ chéo vai trò (PIC CMS + Tester) → Phase không bị block
- Try 2 (Worked): Cùng BE rà soát lỗ hổng API → Chốt phương án fix + cover abuse cases

**🤖 Cải tiến lớn — Asana automation**:
- Dùng AI (Claude) thiết lập bot tự động hóa luồng xử lý ticket Asana sau commit code: comment "Fix on #xxxxx" → đổi trạng thái → assign cho Tester
- → Chấm dứt tình trạng quên update ticket, hand-off QA dứt khoát

**Level up (IKAME LEVEL UP)**:
- **Kiến thức**: Security Mindset cho API — enumerate abuse cases + viết test cover exploit cases
- **Điều làm tốt hơn**: Tư duy bao quát (trám PM/Tester); Chất lượng Mentor (review chặt hơn, bắt lỗi trước QA)
- **Vấn đề khó giải**: Cùng BE tìm root cause lỗ hổng bảo mật API, chặn rủi ro thất thoát doanh thu IAP

**⭐ IDP tag (Dũng tự tag theo template iKame — đúng practice!)**:
- **#1 Innovation 4.6** — Setup tự động hóa Asana
- **#5 Continuous Dev 4.3** — Review thực chiến và hướng dẫn Hiếu
- **#9 Ownership 4.2** — Quản lý đa mục tiêu (Dev + CMS + test API)
- **#10 Ownership 4.3** — Tư vấn đồng nghiệp (bug của Hiếu)
- **#15 Tech R&D 4.6** — Quản lý rủi ro & bảo mật (sự cố API)

**Tồn đọng & rủi ro**:
- Luồng verify IAP chưa xử lý triệt để từ BE
- Bảo mật hoàn toàn Client → dễ bypass bằng tools hack
- **Đề xuất**: BE setup cơ chế check/verify IAP trực tiếp trên server thay vì phụ thuộc Client

**Self-rating**: Làm tốt
**Lý do**: 100% commitment phase + chủ động cross-support + security incident response bảo vệ doanh thu IAP + đề xuất giải pháp verify dài hạn cho BE

**Manager feedback (Trần Đạt, ⭐4 sao — Làm xuất sắc)**:
> "Tuần này em làm đỉnh luôn, tư duy vượt scope của một Dev. Tiếp tục phát huy mạnh mẽ em nhé!"
>
> - **Vượt kỳ vọng & Gánh vác**: Đạt 100% tiến độ cá nhân, đồng thời chủ động lấp vào khoảng trống nhân sự, vận hành mượt mà cả CMS thay PM và tự test API thay QA để đảm bảo timeline phase.
> - **Tác động lớn & Ownership**: Tinh thần trách nhiệm tối đa khi xử lý sự cố bảo mật. Tự viết code mô phỏng hành vi spam để stress-test, phát hiện ra lỗ hổng của BE và đề xuất phương án vá kịp thời, chặn đứng rủi ro thất thoát doanh thu ngay lập tức (cứu nguy 1k$/day có thể mất).
> - **Cải tiến & Tự động hóa**: Ứng dụng AI để tự động hóa toàn bộ luồng xử lý ticket Asana sau commit, tối ưu hóa quy trình hand-off cho QA. **Phần này em chia sẻ lại quy trình/cách setup cho các anh em Dev khác trong tổ chức cùng áp dụng nhé** (tăng mức độ đóng góp hệ thống).
> - **Mentor hiệu quả**: Review code sâu cho Hiếu, bắt lỗi chuẩn xác trước cả QA giúp nâng cao chất lượng code chung của team.

⭐ **Insight**: Đây là tuần Dũng đạt level Senior **rõ nét nhất** — vượt scope Android Dev thuần (Security/API/CMS/QA), self-tag IDP đúng practice trong weekly-report-template, tìm root cause + đề xuất systemic fix (Server-side IAP verify). Manager dùng cụm "tư duy vượt scope của một Dev" = signal rõ ràng cho Senior promotion track.

🎯 **Action request từ Manager (chuyển ngay thành deliverable)**: Chia sẻ quy trình/cách setup Asana automation cho các anh em Dev khác trong tổ chức. Đây là **mũi tên 1 đích 3 ăn**:
1. Đáp ứng yêu cầu Manager trực tiếp
2. Hoàn thành **Continuous Dev #4** (2 buổi tech sharing/quý — đang 0% trong EKS E2 KS2)
3. Hoàn thành **Continuous Dev #6** (đúc kết hệ thống) — gap behavior đang trống

→ Đề xuất: 1 buổi 30 phút trong tuần này hoặc đầu tuần sau, có slide + demo + repo. Format có thể: live demo + sharing chữa các edge case.

## Patterns observed across H1

### Productivity & technical
1. **AI tooling adoption**: Tháng 4 bắt đầu Claude Code → giảm 50% prompt time → tự tạo Custom AI Skill tháng 5. Đang đi nhanh trên đường mastery AI workflow.
2. **Refactor & technical debt**: Có thói quen review tổng thể và refactor khi cần, không chỉ code đè.
3. **Mock-first approach**: Thiết kế mock data → unblock client trước khi BE ready.
4. **Reusable modules**: Đóng gói IAP Remote Config thành module chung — chuẩn Senior thinking.

### People & collaboration
1. **Mentor Hiếu** liên tục từ tháng 3 — chuyển dần từ "đồng hành" → "trao quyền" → "Hiếu PIC độc lập, mình review chiến lược". Tiến triển rất tốt.
2. **Cross-team push**: Luôn chủ động làm việc với BE, AI, PM, QA, UI/UX. Không chỉ làm code của mình.
3. **Quy trình**: Đề xuất nhiều quy trình mới (QA scope, Asana, mock data flow) — chuẩn Senior contribution.
4. **OT có chiến lược**: OT khi nguồn lực thiếu, không thường xuyên. Dấu hiệu Ownership chứ không phải burnout.

### Self-assessment vs Manager
- Self: thường "Làm tốt", thỉnh thoảng "Vượt kỳ vọng"
- Manager: thường cao hơn — 4⭐ là chuẩn, có 1 lần 5⭐ Xuất sắc (W1 tháng 4), W3 tháng 5 nhận 4⭐ "Xuất sắc" + "tư duy vượt scope của một Dev"
- → Dũng đang tự đánh giá khiêm tốn so với evidence thực tế. Có thể tự tin hơn ở promotion review.

### Manager direct action items (đang OPEN, cần follow up)
1. **W1/3 — "Đưa ra các UT trong IDP"**: Đến giờ chưa thấy follow up trong các báo cáo sau. Cần clarify với Manager format UT.
2. **W2/5 — "Chia sẻ Custom AI Skill cho nhóm Dev"**: Đến giờ chưa thấy buổi sharing diễn ra.
3. **W3/5 — "Chia sẻ Asana automation cho anh em Dev trong tổ chức"**: Mới nhất, cần action trong 1-2 tuần tới.

→ 3 items này đều liên quan đến **Continuous Dev sharing** — đang là gap lớn (29% L4). Một buổi tech sharing có thể cover 2-3 items cùng lúc (AI Skill + Asana automation + share IDP UT framework).

## Mapping vào EKS H1 + 17 gap behaviors

### EKS H1 (xem `eks-h1-2026.md`)
- **E1 KS1 (Quality submit phase)** — 60% — Evidence rất mạnh từ AI Home + AI Chat IAP các tuần
- **E2 KS1 (Mentor Hiếu PIC)** — 100% ✓ — Evidence rất rõ từ W4/3 đến W2/4
- **E2 KS2 (Seminar quality)** — 0% — Đề xuất: chia sẻ về Custom AI Skill (W2/5 manager đã gợi ý)
- **E3 KS1 (iGoal compliance)** — 60% — Đang on-track
- **E3 KS2 (IDP 100%)** — 0% trên dashboard, nhưng evidence thực tế đã chạm nhiều gap behaviors (xem dưới)
- **E3 KS3 (Quy trình team)** — 60% — Đã hỗ trợ Manager rà soát Asana toàn team

### Evidence cho 17 gap behaviors (đã captured)

| # | Gap behavior | Evidence từ báo cáo tuần |
|---|---|---|
| 1 | Innovation 4.6 (Dẫn dắt cải tiến) | Sankey bug detection + thuyết phục team fix dù ban đầu đánh giá nhỏ (W1/3); Cải tiến quy trình QA scope (W4/3); Module IAP Remote Config reusable (W4/4); AI workflow + Custom AI Skill (W4/4, W2/5); **Asana automation bot** (W3/5) |
| 2 | Innovation 4.9 (Phán đoán phản ứng team) | Thuyết phục PM + dev fix bug ban đầu họ thấy nhỏ (W1/3); Trao quyền Hiếu PIC (W1/4, W2/4); Điều phối nguồn lực khi Hiếu nghỉ phép (W3/3) |
| 3 | Continuous Dev 4.1 (IDP dài hạn) | (Cần evidence: chốt IDP với DM) |
| 4 | Continuous Dev 4.2 (Chia sẻ cơ hội học) | (Cần evidence: 2 buổi tech sharing/quý) |
| 5 | Continuous Dev 4.3 (Mentor Hiếu, review < 30p) | ⭐ Evidence rất mạnh: 1:1 đều đặn, Hiếu lên PIC độc lập (W4/3 → W2/4); **Review code Hiếu sâu, bắt lỗi trước QA, tránh re-open** (W3/5) |
| 6 | Continuous Dev 4.6 (Đúc kết hệ thống) | Module IAP Remote Config + AI Skill có thể đóng gói thành tài liệu |
| 7 | Continuous Dev 4.7 (Coach/Mentor) | Mentor Hiếu chi tiết về break task, estimate, giao tiếp PM (W1/4) |
| 8 | Ownership 4.1 (Mục tiêu dài hạn OKRs) | iGoal 60% on-track |
| 9 | Ownership 4.2 (Quản lý nhiều mục tiêu) | Plan + chia task + estimate cho nhiều dev (W3/3); Điều phối khi Hiếu nghỉ phép (W3/3); AI Home + AI Chat IAP song song, push 4 dev (W4/3); **Multi-role coverage Dev+CMS+API test** (W3/5) |
| 10 | Ownership 4.3 (Tư vấn đồng nghiệp) | Onboard ae mới vào dự án (W3/3); Review code anh em (W3/3, W4/3); Hỗ trợ Manager rà soát Asana toàn team (W4/4); **Review code Hiếu sâu, bắt lỗi trước QA** (W3/5) |
| 11 | Ownership 4.5 (Strength/weakness team) | Note observations về Hiếu trong 1:1 (W4/3); Hiểu cách phân phối công việc theo strength khi có nhiều dev (W3/3) — chưa thấy specific cho Lan Anh, Thành |
| 12 | Ownership 4.6 (Kiểm soát cảm xúc thay đổi) | "Bình tĩnh khi tester xếp ưu tiên sau cùng" (W2/3); "Lùi 1 bước helicopter view" (W2/4) |
| 13 | Ownership 4.7 (Nắm động lực thành viên) | Chia sẻ mindset với Hiếu (W4/3) |
| 14 | Ownership 4.8 (Tự thúc đẩy động lực) | Cảm hứng từ YEP anh Quyết (W4/1); OT có chiến lược |
| 15 | Tech R&D 4.6 (Rủi ro & bảo mật) | ⭐ **Security incident API IAP hack (W3/5)**: tìm root-cause với BE, xây matrix abuse cases, viết simulation code stress-test, phát hiện lỗ hổng "chặn theo path", đề xuất phương án thay thế → tránh mất $1k. Đề xuất systemic server-side IAP verify. (Cần thêm: R8 / Play Integrity nếu muốn evidence kỹ thuật cụ thể hơn) |
| 16 | Tech R&D 4.7 (Cải tiến quy trình) | Quy trình QA scope, mock-first, AI workflow (W4/3, W2/4, W4/4) |
| 17 | Tech R&D 4.9 (Hướng dẫn đánh giá tích hợp) | (Cần evidence rõ ràng hơn) |
| + | **Tech R&D 4.3** (Tích hợp nhiều công nghệ — Dũng tự tag IDP trong W4/2) | OTHTTP retry mechanism cho mạng yếu (W4/2); ML Kit Image Labeling research (W4/1); Custom AI Skill cho map màu (W2/5) — Dũng đang tích hợp nhiều công nghệ khác nhau vào sản phẩm |

**Note**: Trong báo cáo W4 tháng 2, Dũng tag IDP "Tech R&D 4.3". Behavior này không nằm trong 17 gap behaviors mình ghi nhận ban đầu từ IDP Google Sheets fetch (chỉ có 4.6, 4.7, 4.9 cho Tech R&D). Có 3 khả năng: (a) IDP Sheets đã cập nhật thêm items mà mình chưa re-fetch, (b) Dũng tag IDP rộng hơn — bất kỳ L4 behavior chưa nắm hết, (c) ban đầu mình đọc IDP thiếu. Cần Dũng xác nhận để align tracking.

## Đề xuất next steps

### Đẩy mạnh trong nửa cuối H1 (5-6/2026)
1. **E2 KS2 (Seminar)** — TOP PRIORITY: Tổ chức 1 buổi share về Custom AI Skill / Claude Code workflow. Manager đã gợi ý.
2. **E3 KS2 (IDP)** — Document evidence đã có cho từng gap behavior để cuối H1 update IDP % lên dashboard
3. **Tech R&D gap #15** — Triển khai R8 + Play Integrity cho 1 sản phẩm
4. **Continuous Dev #6** — Đóng gói AI workflow + IAP module thành tài liệu chính thức cho team

### Bổ sung evidence còn thiếu
- Observations về **Lan Anh, Thành** (không chỉ Hiếu) — Ownership gap #11
- Chính thức chốt IDP với DM — Continuous Dev gap #3
- 2 buổi tech sharing/quý — Continuous Dev gap #4 (seminar là 1, cần thêm 1 cho Q2)

### Câu hỏi cho Dũng để hoàn thiện tài liệu
1. Báo cáo W2-W3 tháng 2 + W2 tháng 3 + W3 tháng 4: có thể share content để bổ sung không?
2. Có sản phẩm nào đã apply R8 / Play Integrity chưa?
3. **Manager Đạt yêu cầu "Đưa ra các UT trong IDP" ở W1/3** — đã follow up chưa? UT = User Test / Use Cases cụ thể cho mỗi gap behavior trong IDP?
4. Tech R&D 4.3 — đây có phải item IDP chính thức không? (Dũng tag trong W4/2 nhưng không có trong danh sách 17 gap behaviors ban đầu)
