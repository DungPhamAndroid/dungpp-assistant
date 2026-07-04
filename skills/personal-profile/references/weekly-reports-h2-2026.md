# Weekly Reports Summary — H2 2026

> Tổng hợp các báo cáo tuần của Dũng từ iGoal.
> Bắt đầu từ W27 (30/06/2026).

---

## W27 / 2026 (30/06 – 04/07) — AI Learn: Hoàn thiện & đóng gói phase phát triển

**Sản phẩm/Phase**: AI Learn — Phase hoàn thiện & đóng gói

**IKAME WHAT (KẾT QUẢ)**:

**1. Hoàn thiện tính năng chính → E1 KS1**
- Đóng gói Free Talk & Lesson Talk: optimize trải nghiệm, bổ sung các logic phát sinh ngoài scope ban đầu.
- Đóng gói Practice Tab: optimize code + UI/UX; hỗ trợ check kết quả khi team fill CMS.
- Đóng gói Progress Tab: nhận bàn giao code từ anh Thọ, hoàn thiện nốt các phần còn dở.
- Fix bug AI Talk feature.

**2. Điều phối nhóm Android**
- Nắm bắt tiến độ toàn phase, đưa request timeline merge dựa trên tình hình thực tế.
- Review code + review output trả ra, bổ sung các case bị thiếu cho anh em.

**3. Cross-team**
- Hỗ trợ team AI + BE trace bug phát sinh.
- Hỗ trợ Thành (BE mới join) nắm business logic → bổ sung được các API và logic còn thiếu.
- Hướng dẫn tester sử dụng tool + doc BE để triển khai test API, đẩy nhanh việc đóng gói.

**IKAME HOW (CÁCH LÀM)**:
- Dành thêm thời gian ngoài giờ để giữ tiến độ phase trong bối cảnh nhiều dependency phát sinh.
- Nhận thấy team đang bị tắc ở đầu BE → chủ động raise vấn đề, yêu cầu QA triển khai test API song song — phân tách rõ phần QA cần verify (content output) và phần dev đã có thể đóng gói.
- Theo sát timeline tester: chủ động hỏi han, xác nhận blocker, cung cấp thêm build khi cần.
- Theo sát BE: đồng hành khi BE bị vướng logic, đề xuất hướng xử lý để không bị dừng chờ.
- Hỗ trợ Thành BE hiểu business context của sản phẩm → giảm round back-and-forth giữa các bên.

**Các TRY trong tuần**:
- Try 1 (Worked): Giao tiếp mềm mỏng hơn khi đưa yêu cầu cho cross-team — đúc kết từ checkpoint, áp dụng ngay vào các cuộc trao đổi với BE/AI/QA tuần này.
- Try 2 (Worked): Workflow Claude Code + Asana MCP hỗ trợ fix bug — đã xây xong, áp dụng thực tế và cho kết quả tốt.

**IKAME LEVEL UP**:
- Xây và áp dụng thực tế workflow Claude Code + Asana MCP cho bug fixing.
- Phong cách giao tiếp với cross-team — chủ ý mềm mỏng hơn và frame yêu cầu theo hướng cùng giải quyết.
- Tình trạng team bị block nhiều đầu (BE sync data, outsource model chậm) → tối đa hóa phần client-side có thể làm, đồng thời unblock QA bằng cách hướng dẫn test API độc lập.

**Tồn đọng & rủi ro**: Không thể release app do BE gặp khó trong quá trình sync data từ đầu Content (bên AI) vào hệ thống + các source/model outsource chưa trả đúng timeline. Hướng xử lý: Team đã họp và có phương án — dự kiến release tuần sau.

**Cần hỗ trợ**: TL: Không. Manager: Không.

**⭐ IDP tags**: #1 Innovation 4.6 (Claude Code + Asana MCP workflow) | #5 Continuous Dev 4.3 (hỗ trợ Thành BE; hướng dẫn tester) | #9 Ownership 4.2 (quản lý đồng thời nhiều đầu việc) | #12 Ownership 4.6 (điều chỉnh cách giao tiếp sau checkpoint)

**Self-rating**: Làm tốt
**Lý do**: Hoàn thiện 100% phần client-side đúng cam kết. Phase chưa thể release do block từ BE + Content ngoài tầm kiểm soát của dev — đã chủ động raise và tìm cách unblock tối đa trong phạm vi có thể (E1 KS1).
