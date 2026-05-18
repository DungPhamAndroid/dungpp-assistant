# Learning Plan Template — KMP / CMP / SwiftUI

## Khung kế hoạch học hàng tuần

```
# Learning Plan — Tuần W## ([khoảng ngày])

## Topic chính tuần này
- [Chủ đề] — VD: KMP — Shared ViewModel pattern

## Thời lượng đầu tư
- Cam kết: [X giờ / tuần]
- Khung giờ cố định: [VD: 21h-22h thứ 3, 5, 7]

## Resources
1. [Official docs] — link — phần cụ thể nào
2. [Medium article] — link — tại sao chọn bài này (xem `medium-curation.md`)
3. [Video / Talk] — link — speaker là ai, vì sao trust

## Deliverable cuối tuần
- [1 output cụ thể: code sample, blog note, demo, summary]

## Câu hỏi cần trả lời
- [Câu hỏi 1] — VD: "Khác biệt giữa expect/actual và interface trong KMP là gì?"
- [Câu hỏi 2] — ...

## Reflection cuối tuần
- Đã hiểu: ...
- Còn vướng: ...
- Tuần sau: ...
```

## Nguyên tắc khi lập learning plan

### Topic
- **Chỉ 1 topic chính / tuần**. Tham học nhiều thứ song song → không vững thứ nào.
- Topic gắn với IDP, không học theo trend ngẫu nhiên

### Resources
- **Ưu tiên thứ tự**: Official docs (JetBrains / Apple / Google) → bài viết của engineer team product (JetBrains team, Google DevRel) → Medium từ author có track record → Stack Overflow / Reddit
- Tránh: tutorial blog không rõ tác giả, video clickbait, "Top 10 things..."

### Deliverable
- Mỗi tuần phải có **1 thứ kiểm chứng được**: commit code, gist, blog note, screen recording demo
- Không học chỉ để "biết"; học để áp dụng

### Câu hỏi
- Liệt kê 2-3 câu hỏi cụ thể trước khi học → đọc với mục đích trả lời
- Cuối tuần tự trả lời và ghi lại

## Lộ trình macro 2026 (gợi ý dựa trên IDP)

### Q2-Q3 2026 — KMP Foundation → Production
- Tháng 1: KMP basics — expect/actual, shared module setup
- Tháng 2: Shared ViewModel, networking (Ktor), database (SQLDelight)
- Tháng 3: Ship 1 module thật vào app production

### Q3-Q4 2026 — CMP UI
- Tháng 1: Compose Multiplatform getting started, navigation
- Tháng 2: Resources, theming cross-platform
- Tháng 3: Sample app Android + iOS chia sẻ UI

### Song song (mỗi tuần 2-3h) — SwiftUI Basic
- Mục tiêu: đọc hiểu được SwiftUI code, không cần build sản phẩm
- Output: 1 PR review code iOS / tháng

## Lưu ý quan trọng

- **Không nhồi**: 1 topic / tuần là đủ. Nhồi nhiều → quên hết.
- **Học trong context iKame**: chọn topic có thể áp dụng vào product hiện tại trong 3-6 tháng
- **Share-back**: cứ 4 tuần học 1 chủ đề, share lại 1 lần cho team (tinh thần Level-up + Respect)
