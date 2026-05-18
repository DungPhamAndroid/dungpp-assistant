# Medium Curation — tìm và chọn bài Medium chất lượng

Hướng dẫn Claude tìm và đánh giá bài Medium phù hợp lộ trình học của Dũng.

## Tiêu chí chọn bài

### ✅ Bài đáng đọc
- Author là engineer ở công ty product lớn (Google, JetBrains, Square, Spotify, Trello, Airbnb, Netflix...)
- Có code example chạy được, repo công khai
- Năm xuất bản trong vòng **18 tháng gần đây** (KMP/CMP biến động nhanh)
- Có ≥ 500 claps hoặc được reference bởi JetBrains/Google blog
- Tập trung vào 1 vấn đề cụ thể, không "Top 10 thư viện hay nhất"

### ❌ Bài bỏ qua
- Tutorial copy lại docs official không có insight mới
- Author không có thông tin / không có profile rõ
- Bài quá cũ (>2 năm) cho các topic biến động (KMP, Compose)
- Tiêu đề clickbait ("This will change how you code forever")
- Code không chạy được hoặc không có repo

## Domain ưu tiên cho từng topic

### KMP / CMP
- **proandroiddev.com** — chất lượng cao cho Android/KMP
- **Kt. Academy** — Marcin Moskala và team
- **JetBrains official blog** (blog.jetbrains.com)
- Authors recommend: Touchlab team, John O'Reilly, Marco Gomiero, Stelios Frantzeskakis

### Compose (Android)
- **proandroiddev.com**
- **Android Developers blog** (developer.android.com/jetpack/compose)
- Authors recommend: Chris Banes, Adam Bennett, Manuel Vivo (Google), Florina Muntenescu

### SwiftUI
- **swiftbysundell.com** (John Sundell)
- **hackingwithswift.com** (Paul Hudson)
- **objc.io**
- Apple Developer documentation

## Cách Claude trả lời khi Dũng hỏi "tìm bài Medium về X"

1. Hỏi rõ context: đã biết gì rồi, muốn level nào (intro / intermediate / advanced)
2. Gợi ý 3 bài tối đa, mỗi bài có:
   - Tiêu đề + link
   - Author + công ty / track record
   - Năm xuất bản
   - 1 dòng tóm tắt vì sao đáng đọc với Dũng
3. Nếu không chắc bài còn tồn tại / chính xác link: nói rõ "đây là gợi ý tìm kiếm, cần verify"
4. Khi có thể: ưu tiên link **official docs** thay vì Medium nếu nội dung tương đương

## Format trả lời mẫu

```
3 bài cho [topic] (sort theo độ phù hợp với level của Dũng):

1. [Title] — [Author, Công ty] — [Năm]
   Link: ...
   Why: [1 dòng vì sao]

2. ...

3. ...

Bonus: official doc JetBrains cho topic này — [link] — đọc trước khi nhảy vào Medium.
```

## Tránh

- Không list "10 articles you must read" — vô dụng
- Không recommend bài Claude chưa biết chắc tồn tại
- Không paraphrase Medium content thành response — chỉ curate link + 1 dòng giải thích
