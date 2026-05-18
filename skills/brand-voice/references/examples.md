# Ví dụ viết tốt / viết kém theo iKame voice

## Ví dụ 1 — Báo cáo gặp blocker

**❌ Viết kém (thiếu Autonomy + On Fire Together)**
> Em đang bị stuck với task X, không làm được vì API bên backend chưa sẵn sàng. Mong leader hỗ trợ.

**✅ Viết tốt**
> Task X đang chờ API từ backend (dự kiến sẵn sàng ngày 20/5). Trong thời gian chờ, em chủ động: (1) viết mock layer để UI test trước, (2) hỗ trợ team review PR khác. Nếu cần đẩy nhanh, leader có thể giúp align lịch với backend không?

## Ví dụ 2 — Đề xuất giải pháp kỹ thuật

**❌ Viết kém (thiếu Think Big + Innovation)**
> Em đề xuất dùng Retrofit như mọi khi để gọi API. Đơn giản, dễ làm.

**✅ Viết tốt**
> Có 2 hướng cho phần network layer của module này:
> 1. Retrofit truyền thống — quen team, ship nhanh, nhưng khó share giữa Android & iOS sau này
> 2. Ktor Client (KMP-ready) — đầu tư thêm ~3 ngày setup, nhưng sẵn sàng cho lộ trình KMP của team trong Q3
>
> Em đề xuất hướng 2: vừa giải quyết bài toán hiện tại, vừa chuẩn bị cho mục tiêu lớn hơn. Anh thấy thế nào?

## Ví dụ 3 — Feedback cho đồng nghiệp

**❌ Viết kém (thiếu Respect + cụ thể)**
> PR của em cần làm lại, code chưa ổn lắm.

**✅ Viết tốt**
> Cảm ơn em đã hoàn thành PR nhanh — phần ViewModel logic xử lý gọn. Anh có 2 góp ý:
> 1. Hàm `fetchData()` (line 45) đang xử lý cả network + parsing — tách parsing ra giúp test dễ hơn
> 2. Tên biến `tmp1`, `tmp2` ở line 60-65: đổi thành tên có nghĩa giúp người đọc sau đỡ phải đoán
>
> Em thử refactor lại, nếu cần thảo luận hướng cụ thể thì ping anh nhé.

## Ví dụ 4 — Email đề xuất learning

**❌ Viết kém (thiếu Level-up)**
> Em xin phép dành 1 tiếng / tuần học Kotlin Multiplatform.

**✅ Viết tốt**
> Em đề xuất đầu tư 4h/tuần cho lộ trình KMP trong 3 tháng tới, với cam kết cụ thể:
> - Tháng 1: hoàn thành KMP official tutorial + viết 1 demo nội bộ
> - Tháng 2: chuyển 1 module nhỏ của app sang KMP để team review
> - Tháng 3: chia sẻ kinh nghiệm trong session nội bộ
>
> ROI cho team: chuẩn bị foundation cho mục tiêu KMP của Q3, giảm risk khi migrate quy mô lớn. Anh approve được không ạ?

## Ví dụ 5 — Thông báo daily đơn giản

**❌ Viết kém (thiếu năng lượng)**
> Hôm qua em làm task X, hôm nay làm task Y. Không có blocker.

**✅ Viết tốt**
> Done: PR #123 (login flow), merged. Hôm nay: bắt đầu task Y (refactor session manager), dự kiến PR sẵn trước cuối ngày mai. No blocker — nếu ai đang touch SessionManager.kt thì ping em để tránh conflict nhé.
