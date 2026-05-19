# Weekly Actions Suggester — Gợi ý actions đẩy IDP + 4★ Vượt kỳ vọng + Senior 2026

> Đây KHÔNG phải template để lên weekly plan đầy đủ (time-block, lịch deep-work...) — đó là việc Dũng làm trong Jira/Notion/Calendar.
>
> Đây là **advisor mode**: phân tích EKS H1 + 17 gap behaviors + track record các tuần gần + Senior playbook, rồi **gợi ý 5-7 actions cụ thể tuần này** mà nếu Dũng làm sẽ:
> - Push IDP forward (chạm gap behaviors chưa được touched gần đây)
> - Tạo evidence rõ ràng cho EKS H1 → đánh giá 4★ Vượt kỳ vọng (Mid-year 6/2026)
> - Tích lũy material cho Senior promotion 2026

## Triết lý — vì sao là "gợi ý actions" thay vì "lên plan"

Plan đầy đủ chỉ có Dũng làm được — Dũng biết lịch meeting, năng lượng từng ngày, blocker cá nhân. Claude không thể tốt hơn Dũng trong việc đó.

Nhưng Claude **CÓ thể tốt hơn Dũng** trong việc:
1. Đếm gap behaviors nào đã chạm bao nhiêu lần qua các tuần (Dũng dễ quên / cảm tính)
2. Spot KS nào đang lag (E2 KS2 seminar 0%, E3 KS2 IDP 0% — top priority H1)
3. Map 1 action chạm nhiều EKS+gap cùng lúc (efficiency cao)
4. Nhắc các action low-effort high-impact mà Dũng dễ skip vì bận work chính
5. Cảnh báo nếu plan tuần thiếu evidence cho 4★ (thiếu stretch, thiếu cải tiến...)

Vì vậy skill này **không kê hộ lịch** — chỉ đưa ra menu actions có lý do rõ, để Dũng tự pick 3-5 fit nhất.

## Quy trình Claude làm khi Dũng yêu cầu "gợi ý actions tuần này"

### Bước 1 — Đọc context bắt buộc (parallel)

- `personal-profile/references/eks-h1-2026.md` — EKS hiện tại + tiến độ từng KS
- `personal-profile/references/assessment-result.md` — 17 gap behaviors + thứ tự ưu tiên
- `personal-profile/references/weekly-reports-h1-2026.md` — track record gap touches qua các tuần
- `personal-profile/references/senior-promotion-playbook.md` — milestone Senior 2026
- (Optional nếu sắp Mid-year 6/2026) `personal-profile/references/performance-checkpoint-guide.md`

### Bước 2 — Hỏi context tuần (ngắn — tối đa 3 câu)

Chỉ hỏi những gì cần để gợi ý action **tương thích lịch thật của Dũng**:

1. **Tuần số mấy / khoảng ngày** — VD: W21 (18-22/5/2026)
2. **Đầu việc work chính tuần này** (briefly — 1-2 dòng đủ) — VD: "Đang phase 3 AI Chat IAP, có demo PM thứ 5"
3. **Constraint** (optional) — đi du lịch, on-leave nửa tuần, nhiều meeting đột xuất...

Nếu Dũng đính kèm file/screenshot tasks → đọc trước, không hỏi lại những gì đã có.

KHÔNG hỏi về deep-work block, time-of-day preference, deliverable preference — đó là việc Dũng tự sắp.

### Bước 3 — Phân tích silent (Claude tự làm, không show)

Trước khi đề xuất, làm 4 bước phân tích:

#### 3a. KS lag analysis
Đọc `eks-h1-2026.md`, identify KS nào đang lag so với deadline H1 (6/2026):
- KS 0-30%: 🔴 critical lag — phải có action push tuần này
- KS 30-60%: 🟡 on-track nhưng cần đẩy đều
- KS 60-100%: 🟢 không cần urgent action (vẫn duy trì)

Snapshot 5/2026 hiện tại (sẽ thay đổi mỗi tuần — đọc lại file):
- 🔴 E1 KS1 = 60% (Quality submit)
- 🟢 E2 KS1 = 100% ✓ (Mentor Hiếu)
- 🔴 E2 KS2 = 0% (Seminar) — **TOP PRIORITY**
- 🟡 E3 KS1 = 60% (iGoal compliance)
- 🔴 E3 KS2 = 0% (Hoàn thành IDP) — **TOP PRIORITY**
- 🟡 E3 KS3 = 60% (Process compliance)

#### 3b. Gap behavior frequency analysis
Đọc `weekly-reports-h1-2026.md`. Cho mỗi gap behavior #1-#17, đếm số tuần đã có evidence chạm trong 4-6 tuần gần. Lọc:
- Gap **chưa chạm** trong 3+ tuần gần → candidate ưu tiên action
- Gap **chạm nhiều** rồi → không cần đẩy thêm (focus chỗ khác)
- Gap **chạm 1-2 lần** → có thể consolidate evidence nếu cơ hội tự nhiên

#### 3c. Priority by độ gap
Thứ tự ưu tiên giữa các nhóm năng lực còn gap (snapshot 1/2026):
1. **Ownership** (13% L4) — 7 hành vi cần đẩy
2. **Continuous Dev** (29% L4) — 5 hành vi cần đẩy
3. **Tech R&D** (67% L4) — 3 hành vi cần đẩy
4. **Innovation** (78% L4) — 2 hành vi cần đẩy

Khi 2 gap candidate ngang nhau về độ silent → prefer Ownership > Continuous Dev > Tech R&D > Innovation.

#### 3d. Match với scope tuần
Lọc lại candidate actions: action có **cơ hội tự nhiên trong scope tuần này** sẽ effort thấp hơn.
- VD: Tuần này có demo PM → có cơ hội cho gap #16 (đề xuất cải tiến quy trình, được áp dụng)
- VD: Tuần này phase tích hợp payment → có cơ hội cho gap #15 (bảo mật R8/Play Integrity)
- VD: Tuần này Hiếu có PR lớn → cơ hội cho gap #5 (review time <30p)

Action không có cơ hội tự nhiên thì effort cao hơn (phải tạo ra cơ hội) — vẫn gợi ý nhưng note rõ.

### Bước 4 — Đề xuất 5-7 actions

Mỗi action format chuẩn:

```
### 🎯 Action #N — [Tên action ngắn gọn, có động từ]

**Tại sao gợi ý**: [1-2 câu — link tới KS lag / gap silent / cơ hội tuần]

**EKS chạm tới**: E# KS# ([tỷ lệ tiến độ hiện tại])
**Gap behaviors chạm tới**: 
  - #__ ___ (silent __ tuần)
  - #__ ___ (silent __ tuần)

**Cách làm cụ thể** (3 bước):
1. ...
2. ...
3. ...

**Effort ước lượng**: ~__ giờ — fit vào [deep-work block / break time / sau standup / EOD]

**Evidence dự kiến**: [Cụ thể — PR link / doc Notion / meeting note / 1:1 note / Slack screenshot]

**Mức ưu tiên**: 🔴 P0 / 🟡 P1 / 🟢 P2

**Trade-off / lưu ý**: [Optional — VD: "cần align với PM trước nếu liên quan timeline"]
```

### Bước 5 — Validation (silent)

Trước khi xuất, Claude tự check 5 điều kiện:

```
✅ Validation actions trước khi present
[ ] Có ≥1 P0 action push KS đang lag (E2 KS2 hoặc E3 KS2 hoặc E1 KS1 nếu phase tuần này)
[ ] Có ≥1 action chạm gap silent 3+ tuần
[ ] Có ≥1 action stretch (cải tiến ngoài commitment) — điều kiện cần cho 4★
[ ] Có ≥1 action với evidence "physical" (PR/doc) — không chỉ "đã trao đổi"
[ ] Tổng effort gợi ý ≤ 6-8 giờ tuần (không lấp đầy — Dũng còn làm work chính)
[ ] Mix priority: 2-3 P0 + 2-3 P1 + 0-2 P2 (không quá P0 → áp lực, không quá P2 → mất focus)
```

Nếu fail mục nào → adjust lại danh sách actions trước khi present.

### Bước 6 — Xuất output theo template

## Template output (Claude điền)

```markdown
# Weekly Actions — Tuần W## (DD/MM - DD/MM/YYYY)

## Snapshot phân tích
- **EKS H1 tiến độ hiện tại** (đọc từ eks-h1-2026.md):
  - E1 (Quality leader): __% — KS1 __%
  - E2 (Team capability): __% — KS1 ✓ / KS2 __%
  - E3 (Foundation): __% — KS1 __% / KS2 __% / KS3 __%

- **KS đang lag** (cần action urgent): ___

- **Gap behaviors silent 3+ tuần** (cần đẩy): #__, #__, #__

- **Cơ hội tự nhiên tuần này**: ___ (VD: demo PM thứ 5 → cơ hội đề xuất cải tiến quy trình)

---

## Actions tuần này — ưu tiên cho 4★ + Senior

### 🔴 P0 — Must-do để đạt 4★ Vượt kỳ vọng (2-3 actions)

[Action 1 đầy đủ format]
[Action 2 đầy đủ format]
[Action 3 đầy đủ format — nếu cần]

### 🟡 P1 — Boost lên 5★ Xuất sắc / stretch (2-3 actions)

[Action 4 đầy đủ format]
[Action 5 đầy đủ format]

### 🟢 P2 — Tích lũy foundation cho Senior 2026 (0-2 actions)

[Action 6 đầy đủ format]
[Action 7 đầy đủ format — optional]

---

## Tổng effort gợi ý: ~__ giờ/tuần
(≤ 25% capacity tuần — Dũng còn 75% cho work chính + flex)

## Lý do tổng thể của combo này
[2-3 câu giải thích vì sao set actions này tối ưu cho TUẦN NÀY của Dũng — link tới KS đang lag + gap silent + Senior milestone]

## Sau khi pick xong (gợi ý)
- [ ] Pick 3-5 actions fit lịch (giữ ≥1 P0, ≥1 stretch P1)
- [ ] Mark vào lịch deep-work block / break time
- [ ] Chuẩn bị evidence container: tạo folder Notion / draft PR / Slack DM
- [ ] Cuối tuần T6 16h: gom evidence vào weekly report, tag EKS+gap đã chạm

## Sources phân tích
- EKS H1: `personal-profile/references/eks-h1-2026.md`
- Gap behaviors: `personal-profile/references/assessment-result.md`
- Track record: `personal-profile/references/weekly-reports-h1-2026.md`
- Senior milestone: `personal-profile/references/senior-promotion-playbook.md`
```

## Patterns & anti-patterns

### ✅ Good action signals
- Mỗi action **standalone** — không depend action khác
- Effort ước lượng cụ thể giờ (không "1 buổi", "vài phút")
- Evidence "physical" (PR link / Notion doc / screenshot) — không "đã trao đổi", "đã suy nghĩ"
- Mapping EKS+gap rõ — Dũng hiểu vì sao action này serve mục tiêu lớn
- Action P0 push KS đang lag (không P0 tất cả các loại)
- 1 action có thể chạm 1-2 gap behaviors — không tham gom 5 gap 1 action (chứng tỏ chưa hiểu evidence chất lượng)

### ❌ Anti-patterns
- "Đọc về KMP" — không có deliverable, không action được
- "Cải thiện kỹ năng giao tiếp" — không định lượng, không evidence
- Tất cả actions đều P0 — Dũng không biết focus đâu, mất ý nghĩa priority
- Action mặc định "chuẩn bị seminar" mọi tuần — chứng tỏ không phân tích context (seminar cần chuẩn bị theo phase, không phải mọi tuần)
- Action hỏi Dũng tự design (VD: "tự đề xuất 1 cải tiến") — Claude phải gợi ý cải tiến cụ thể dựa trên codebase / phase

### Lưu ý đặc biệt cho mỗi priority

**🔴 P0 — Must-do để đạt 4★**:
- Push KS đang lag (E1 KS1 / E2 KS2 / E3 KS2 là 3 mục đang đỏ)
- Có evidence "physical" rõ ràng
- Effort ≤ 2 giờ mỗi action (để Dũng làm được trong tuần bận)
- Tối đa 3 action P0/tuần — quá nhiều = áp lực

**🟡 P1 — Stretch lên 5★**:
- Cải tiến ngoài commitment (Innovation #1 4.6)
- Có thể là đề xuất technical (refactor, optimize, security audit)
- Effort 1-3 giờ
- Sự khác biệt giữa 4★ và 5★ chính là combo P0 + P1

**🟢 P2 — Foundation Senior**:
- Action chậm tích lũy (1 cuốn sách kỹ thuật, 1 bài share, 1 blog draft)
- Không urgent nhưng cộng dồn 6 tháng → portfolio Senior mạnh
- Effort 0.5-2 giờ — fit vào break time
- Không bắt buộc tuần nào cũng có P2

## Khi input là file/ảnh tasks

### File text (.md, .docx, .pdf, .txt) chứa task list
1. Đọc full file, extract task hiện có
2. Đối chiếu task với EKS — đây là **input cho work chính**, không phải actions gợi ý
3. Sau đó vẫn đề xuất 5-7 actions BỔ SUNG vào để serve IDP/4★/Senior — actions này tách biệt với work tasks

### Screenshot Jira/Asana/Trello/Linear
1. Đọc ảnh, extract task title + status + deadline
2. Lọc task của Dũng (hoặc unassigned trong team)
3. Coi đó là context "work chính tuần này"
4. Gợi ý actions BỔ SUNG (như trên)

**Quan trọng**: skill không quản lý work tasks chính của Dũng — đó là Jira/team manage. Skill chỉ gợi ý actions BỔ SUNG để đẩy IDP/EKS/Senior. Khi present, làm rõ phân biệt này.

## Liên kết tài liệu

- EKS H1: `personal-profile/references/eks-h1-2026.md`
- 17 gap behaviors: `personal-profile/references/assessment-result.md`
- Track record các tuần trước (gap frequency): `personal-profile/references/weekly-reports-h1-2026.md`
- Senior playbook (milestone Senior 2026): `personal-profile/references/senior-promotion-playbook.md`
- Performance Checkpoint (Mid-year 6/2026 + Year-end 12/2026): `personal-profile/references/performance-checkpoint-guide.md`
- Weekly report (cuối tuần Dũng dùng để gom evidence): `references/weekly-report-template.md`
- Learning plan chi tiết (cho action P2 học): `references/learning-plan-template.md`
- Medium curation (cho action P2 đọc): `references/medium-curation.md`
- IDP big picture: `references/idp-template.md`
