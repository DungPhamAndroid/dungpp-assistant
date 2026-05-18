# Weekly Report Template — iKame BU3 Android Dev (official)

> Đây là template báo cáo tuần CHÍNH THỨC của team Dev iKame. Bám sát 6 sections để Tech Lead / Manager dễ review.
> Khi điền: nhớ link mọi achievement với **EKS H1** (xem `personal-profile/references/eks-h1-2026.md`) và **17 gap behaviors** (xem `personal-profile/references/assessment-result.md`).

## Template gốc (copy-paste)

```markdown
**1) IKAME WHAT (KẾT QUẢ – bám EKS1/OKR)**
- Sản phẩm/Phase phụ trách tuần này:
- Tiến độ so với kế hoạch:
  + SP1: ...
  + SP2: ...

**2) IKAME HOW (CÁCH LÀM – TỰ CHỦ, XOAY XỞ, PHỐI HỢP)**
- Tôi đã chủ động xoay xở gì để bám mục tiêu:
- Cách tôi phối hợp với team/PM/QA:
- Các TRY trong tuần (đã thử gì → kết quả worked/partial/failed):
- 1 cải tiến nhỏ tôi áp dụng (nếu có):

**3) IKAME LEVEL UP (HỌC ĐƯỢC & NÂNG NĂNG LỰC)**
- Kiến thức/kỹ năng tôi học được tuần này:
- Điều tôi làm tốt hơn so với tuần trước:
- Vấn đề khó tôi đã xử lý được (impact ngắn gọn):
- IDP: [tag gap behavior nào đã chạm tuần này]

**4) TỒN ĐỌNG & RỦI RO**
- Tồn đọng chính:
- Ảnh hưởng tới tiến độ/chất lượng:
- Hướng xử lý dự kiến:

**5) Cần hỗ trợ của manager, techleader không**
- TL hỗ trợ: [công nghệ / chốt hướng xử lý / tìm hiểu công nghệ khó]
- Manager hỗ trợ: [nguồn lực / timeline / phối hợp]

**6) TỰ ĐÁNH GIÁ (theo 5 mức)**
- Tuần này khối lượng công việc: [Ít việc / Bình thường / Nhiều việc / Rất nhiều việc]
- Mức: [Không đạt kỳ vọng / Chưa đạt kỳ vọng / Làm tốt / Vượt kỳ vọng / Xuất sắc]
- Lý do (1–2 câu, bám OUTPUT & EKS1):
```

## Guidance khi điền — chuẩn iKame voice

### Section 1 — IKAME WHAT (Kết quả)

Mục đích: chứng minh **OUTPUT** đã ship được, không liệt kê activity.

Format cho mỗi sản phẩm:
```
+ [Tên SP] — [Phase đang phụ trách]: [tiến độ cụ thể] vs [kế hoạch]
```

Ví dụ tốt:
```
+ SP1 (AI Home): Phase 2 — Hoàn thành 4/5 feature theo cam kết, 1 feature lùi sang tuần sau do API backend chưa ready
+ SP2 (AI Learn): Phase 1 — Đã ship onboarding flow ra staging, đang chờ QA verify
```

Ví dụ kém: "Tuần này làm AI Home và AI Learn"

**Tag EKS**: Tự động link với E1 KS1 (100% phase submit đúng kế hoạch) — luôn nói rõ tỷ lệ phase hoàn thành.

### Section 2 — IKAME HOW (Cách làm)

Mục đích: chứng minh tinh thần **On Fire Together + Autonomy + Innovation** của iKame.

#### Tôi đã chủ động xoay xở gì để bám mục tiêu
Phải có evidence cụ thể, không chung chung. Ví dụ tốt:
- "API backend chưa ready → viết mock layer để UI test trước, không bị block"
- "Phase deadline tight → reorganize thứ tự task theo dependency, ship feature core trước"

#### Cách phối hợp với team/PM/QA
Nêu cụ thể tương tác có giá trị:
- "1:1 với Hiếu thứ 3 — review PR session manager, time review giảm còn 25 phút"
- "Sync với QA Lan Anh trước khi merge — giảm 2 round bug fix"
- "Đề xuất với PM hoãn 1 feature low-priority sang phase sau để đảm bảo quality phase này"

#### Các TRY trong tuần (đã thử gì → kết quả)
Format `[Action] → [Result: worked/partial/failed] — [Lesson]`. Ví dụ:
- "Thử dùng Compose Navigation 2 → worked — giảm 30% boilerplate code"
- "Thử Hilt cho module mới → partial — hoạt động OK nhưng build time tăng 15s, cần investigate"
- "Thử dùng Coroutine Flow cho realtime sync → failed — performance không tốt, fallback dùng StateFlow"

#### 1 cải tiến nhỏ tôi áp dụng
Quan trọng — đây là evidence cho **Innovation gap behavior #1 (4.6)**. Mỗi tuần cố gắng có 1.
Ví dụ:
- "Refactor utility class Date thành extension functions → giảm 40 lines code repeat trong 5 file"
- "Setup Git hook auto check format trước commit → team không còn quên format"

**Tag EKS**: E2 KS1 (mentor Hiếu) + E3 KS3 (quy trình team). 
**Tag gap behaviors**: Innovation #1, Continuous Dev #5 (mentor Hiếu).

### Section 3 — IKAME LEVEL UP (Học được)

Mục đích: evidence cho **Level-up + Continuous Development** — đây là 1 trong 2 năng lực gap lớn của Dũng.

#### Kiến thức/kỹ năng tôi học được
Phải cụ thể, không "học được nhiều thứ". Format:
```
- [Topic] — [Source: docs/blog/PR review/meeting] — [Áp dụng được vào đâu]
```

Ví dụ:
- "Kotlin sealed class hierarchy — JetBrains docs — refactor được UI state class trong AI Home"
- "R8 obfuscation rules — Android Dev blog — chuẩn bị áp dụng cho release Q3"

#### Điều tôi làm tốt hơn so với tuần trước
Có metric. Ví dụ:
- "PR review time: tuần trước 45p → tuần này 25p (giúp Hiếu close issues nhanh hơn)"
- "Bug count phase này: 5 → 2 sau khi áp dụng checklist tự review"

#### Vấn đề khó tôi đã xử lý được
Quan trọng — evidence cho **Problem Solving** (đã ở L4 100%, cần duy trì) và stretch lên L5.
Format `[Bug/Problem] → [Root cause] → [Fix] → [Impact]`.

#### IDP — tag gap behavior nào đã chạm
**MỚI THÊM SECTION NÀY** — quan trọng cho promotion tracking.

Format:
```
- [#Gap_number] [Tên hành vi]: [Action cụ thể đã làm tuần này] — [Evidence: link/note]
```

Ví dụ:
```
- #5 (Continuous Dev — Mentor Hiếu): 2 buổi 1:1 + review 3 PR — review time avg 28 phút
- #11 (Ownership — Strength/weakness team): Note observation về Hiếu (mạnh debug, cần grow design pattern) trong Notion
- #1 (Innovation — Cải tiến kỹ thuật): Refactor utility Date → đề xuất với Techlead, đang chờ review
```

### Section 4 — Tồn đọng & Rủi ro

Mục đích: **On Fire Together + Autonomy** — show effort + ask cụ thể, không "stuck".

Format mỗi tồn đọng:
```
- [Task] — [Ảnh hưởng cụ thể đến phase/team] — [Hướng xử lý đã thử + đề xuất tiếp theo]
```

Ví dụ tốt:
- "API endpoint /sync chưa stable — block phase 2 hoàn thành cuối tuần — đã ping backend, đề xuất họp 30p thứ 2 để align timeline"

Ví dụ kém: "API chậm, đang chờ backend"

### Section 5 — Cần hỗ trợ

Nói rõ ai hỗ trợ phần gì. Không gộp "cần hỗ trợ" chung chung.

- **TL hỗ trợ**: chọn từ [công nghệ / chốt hướng xử lý / tìm hiểu công nghệ khó]
- **Manager hỗ trợ**: chọn từ [nguồn lực / timeline / phối hợp cross-team]

Nếu không cần hỗ trợ tuần này: "TL: không. Manager: không."

### Section 6 — Tự đánh giá

#### Khối lượng công việc
Chọn 1 trong 4: Ít việc / Bình thường / Nhiều việc / Rất nhiều việc.

Lưu ý cho Dũng: là Senior aspiring, nên hạn chế tự đánh "Ít việc". Nếu "Ít việc" → chủ động pick thêm để chứng minh **Ownership #2 (gap 4.2 — quản lý nhiều mục tiêu phức tạp cùng lúc)**.

#### Mức tự đánh giá
5 mức: Không đạt / Chưa đạt / Làm tốt / Vượt kỳ vọng / Xuất sắc.

**Tinh thần iKame**: tự đánh giá khách quan, không khiêm tốn quá cũng không "tự sướng". Bám OUTPUT thực sự:
- **Làm tốt**: hoàn thành 100% commitment, không nổi bật
- **Vượt kỳ vọng**: hoàn thành 100% + có thêm cải tiến/đóng góp ngoài scope
- **Xuất sắc**: tạo impact ngoài team mình, được nhận bởi cross-team

Lý do (1-2 câu): luôn link với OUTPUT cụ thể + EKS:
- ❌ "Em cố gắng hết sức tuần này"
- ✅ "Đạt 100% commitment phase 2 (E1 KS1), thêm cải tiến refactor Date utility được Techlead merge → vượt kỳ vọng"

## Quy tắc khi Claude giúp Dũng viết báo cáo tuần

1. **Hỏi đủ thông tin** trước khi viết: tuần nào, SP nào đang phụ trách, đã ship gì, có blocker không
2. **Tự động tag** mỗi achievement với EKS KS tương ứng (xem `eks-h1-2026.md` để map)
3. **Tự động gợi ý** gap behaviors nào đã chạm trong section 3 — IDP
4. Bám đúng **6 sections + thứ tự**, không tự ý merge/split
5. **Câu ngắn, có metric**. Tránh "tôi đã cố gắng", "tôi đã học được nhiều"
6. Khi Dũng nói "không có gì làm tuần này" → KHÔNG tự bịa. Hỏi lại + suggest action cho tuần sau
7. Section 6 (tự đánh giá) — không tự khiêm hay tự sướng cho Dũng. Show evidence khách quan rồi để Dũng tự chọn

## Cấu trúc thư mục báo cáo (gợi ý)

```
weekly-reports/
├── 2026-W18.md
├── 2026-W19.md
├── 2026-W20.md
└── ...
```

Cuối Half (6/2026), gom tất cả báo cáo để:
1. Tổng kết evidence cho EKS H1 evaluation
2. Tag tổng số lần chạm vào từng gap behavior → đánh giá tiến độ IDP
3. Chuẩn bị self-assessment H2

## Liên kết tài liệu

- EKS H1: `personal-profile/references/eks-h1-2026.md`
- 17 gap behaviors: `personal-profile/references/assessment-result.md`
- Brand voice iKame: `brand-voice/SKILL.md` + `core-values.md`
