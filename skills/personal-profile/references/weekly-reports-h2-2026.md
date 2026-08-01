# Weekly Reports Summary — H2 2026

> Tổng hợp các báo cáo tuần của Dũng từ iGoal.
> Bắt đầu từ W27 (30/06/2026).

---

## W27 / 2026 (30/06 – 04/07) — AI Learn: Hoàn thiện & đóng gói phase phát triển

**Sản phẩm/Phase**: AI Learn — Phase hoàn thiện & đóng gói

**IKAME WHAT (KẾT QUẢ)**:

**1. Hoàn thiện tính năng chính**
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
**Lý do**: Hoàn thiện 100% phần client-side đúng cam kết. Phase chưa thể release do block từ BE + Content ngoài tầm kiểm soát của dev — đã chủ động raise và tìm cách unblock tối đa trong phạm vi có thể.

**Manager feedback (Trần Đạt, ⭐4 sao — Làm xuất sắc)**:
> "Tuần vừa rồi Dũng đã giành rất nhiều tâm trí và nỗ lực, quyết liệt để giải quyết điểm nghẽn → đưa sản phẩm về đúng quỹ đạo timeline thậm trí có thể vượt. Anh đồng ý mức đánh giá 4 sao (Làm xuất sắc) nhé. Tiếp tục giữ nhịp tạo Hit nhé :))"

---

## W28 / 2026 (07/07 – 11/07) — AI Learn: Optimize & đóng gói phase 1

**Sản phẩm/Phase**: AI Learn — Optimize & đóng gói phase 1

**IKAME WHAT (KẾT QUẢ)**:
- **Fix bug phase 1**: Đóng hết list bug Asana cho AI Talk, Login, Progress đúng kế hoạch.
- **Optimize AI Talk**: Đồng bộ lại luồng Typing × Viseme × Audio × Speed; tối ưu luồng Summary theo dữ liệu thực tế trả về; tối ưu luồng Limit Time và Create Conversation Error.
- **Đóng gói Practice Tab**: Tối ưu logic map data + UI/UX.
- **Đóng gói Progress Tab**: Tối ưu leaderboard + history; xử lý error case.
- **Tracking & Auth**: Implement Tracking Screen Active; xử lý lại luồng Login khi refresh token hết hạn.
- **Review code** cho Hiếu.

→ Tất cả các bản build được đóng gói và gửi đúng kế hoạch. Chưa thể release do chưa có API Production từ BE.

---

**IKAME HOW (CÁCH LÀM)**:
- **Chủ động xoay xở để bám mục tiêu**: Sau khi BE trả bản final API, chủ động rà soát toàn bộ data và lên plan đóng gói lại tính năng — chủ yếu thực hiện vào buổi tối và cuối tuần để giữ đúng timeline. Chủ động rà soát các vấn đề phát sinh, lên plan chỉnh sửa cụ thể trước khi bắt tay vào xử lý.
- **Không để dependency ngoài ảnh hưởng mục tiêu bộ phận**: Dù bị block bởi BE ở đầu Production API, vẫn đảm bảo toàn bộ tính năng được đóng gói hoàn chỉnh.
- **Phối hợp với team**:
  - Nhận thấy QA có xu hướng chậm lại do BE chưa trả API Production → chủ động push QA tiếp tục đóng bug theo đúng kế hoạch.
  - Phối hợp chặt với BE để trace và xử lý các vấn đề API phát sinh.
  - Làm việc với Design/UI để bổ sung các luồng còn thiếu trong spec.
- **Mentor**: Chủ động rà soát các tính năng Hiếu phụ trách, đưa góp ý cụ thể để hoàn thiện.

---

**IKAME LEVEL UP**:
- Rà soát kỹ data thực tế trước khi optimize thay vì giả định theo spec — phát hiện nhiều edge case trong luồng Summary và Limit Time mà spec chưa cover.
- Luồng refresh token hết hạn — trace được root cause và xử lý đúng lifecycle, tránh user bị văng ra màn hình login bất ngờ.

**⭐ IDP tags**: #1 Innovation 4.6 (Optimize luồng Typing × Viseme × Audio × Speed) | #5 Continuous Dev 4.3 (rà soát + góp ý tính năng Hiếu) | #9 Ownership 4.2 (quản lý song song nhiều tính năng + điều phối QA/BE/Design) | #14 Ownership 4.8 (OT buổi tối và cuối tuần để giữ đúng timeline)

---

**Tồn đọng & rủi ro**: Chưa thể release app do BE chưa có API Production. Toàn bộ phần Android đã sẵn sàng. Hướng xử lý: Tiếp tục theo sát tiến độ BE; sẵn sàng release ngay khi có API Production.

**Cần hỗ trợ**: TL: Không. Manager: Không.

**Self-rating**: Làm tốt
**Lý do**: Đóng gói hoàn chỉnh toàn bộ tính năng phase 1 + fix hết bug Asana đúng kế hoạch dù phải OT buổi tối và cuối tuần. Chủ động push QA và phối hợp đa chiều (BE/Design/QA) để không để dependency ngoài ảnh hưởng tiến độ bộ phận.

---

## W29 / 2026 (14/07 – 18/07) — AI Learn: Đóng gói & Phát hành (E1 KS1)

**Sản phẩm/Phase**: AI Learn — Đóng gói & phát hành bản đầu tiên lên store

**IKAME WHAT (KẾT QUẢ)**:
- AI Talk: Optimize replay audio + hint message cho case websocket đã đóng.
- BottomSheet: Fix triệt để lỗi dai dẳng đã tồn tại ở nhiều sản phẩm — không đi theo "cách cũ" vá tạm, dành hẳn thời gian đào đến root cause.
- Billing (Hiếu): Rà soát phát hiện crash, fix trước khi ảnh hưởng release.
- Login UX: Optimize lại toàn bộ màn.
- Practice + Progress video stream: Fix bug progress, rà soát và optimize lại cả màn Practice do trước đó design đổi nhưng không được thông tin.
- Progress Error Case: Làm việc với Design để bổ sung các case còn thiếu, triển khai code xong — đóng hoàn toàn case tồn đọng từ đầu tuần.
- Bug Asana phase 2: Fix hết.
- API Production: Ghép xong.
- Bug login (case khó): Sau khi ghép API prod lên internal, gặp case không login được — làm cùng anh Cường đến 10h đêm chưa ra. Về nhà tự đọc lại toàn bộ step setup + quy tắc, rà soát và tìm đúng nguyên nhân để fix. Đồng thời chủ động làm việc với BE check log, cùng nhau trace nguyên nhân → giúp team iOS fix login nhanh hơn nhiều so với Android.
- Optimize Home (phần trước đó không phải mình code): Rà soát phát hiện thiếu logic trạng thái lesson (Complete/Inprogress/Lock) và luồng khi chọn lesson → raise + đưa giải pháp bổ sung UI/luồng.
- Line + anim bong bóng bài hiện tại: PM chưa có kịch bản cụ thể do logic chồng chéo → nghiên cứu, gỡ rối các case (hoàn thành bài, đổi level ngôn ngữ), chốt case cụ thể gửi iOS đồng bộ xử lý.
- Detail Lesson (phần trước đó không phải mình code): Phát hiện lệch UI/info so với Design, team chưa chốt rõ luồng → chủ động làm rõ + update UI/UX.
- Lên kế hoạch optimize phase 2: Chủ động rà soát trước các vấn đề cần giải quyết cho phase tiếp theo và chuẩn bị hướng xử lý cụ thể, để team có plan rõ ràng ngay khi họp chốt vào thứ 6 — không chờ đến họp mới bắt đầu bàn.

→ Đóng gói & phát hành bản đầu tiên lên store thành công (E1 KS1).

**IKAME HOW (CÁCH LÀM)**:
- Chủ động xoay xở: đóng hết các bug nghiêm trọng chặn release (Billing, BottomSheet, Login) trước khi phát sinh thêm rủi ro cho app.
- Phối hợp: trực tiếp sang làm việc với BE để check log, cùng trace nguyên nhân bug login — không chỉ tự fix mà còn giúp team iOS fix nhanh hơn.
- Đi trước 1 bước: tự rà soát vấn đề + đề xuất phương án cho phase 2 trước khi họp, giúp cuộc họp thứ 6 có input cụ thể để chốt nhanh thay vì bàn từ đầu.
- Đầu tư thêm thời gian ngoài giờ để đảm bảo release đúng hẹn: thường xuyên làm đến 8-9h tối, có hôm đến 10h đêm để xử lý dứt điểm từng bug trước khi lên chợ.

**Các TRY trong tuần**:
- Try 1 (Worked): Case login bí đến 10h đêm cùng anh Cường không ra → về tự đọc lại step setup/quy tắc → tìm đúng root cause.
- Try 2 (Worked): Chủ động rà soát lại phần setup trên store → phát hiện đúng hướng trace lỗi login, có thể tái dùng cho case tương tự sau.

**IKAME LEVEL UP**:
- Kiến thức: cách debug case login liên quan config/setup trên store — tự tìm hiểu qua tài liệu, áp dụng trực tiếp fix bug prod.
- Vấn đề khó đã xử lý: Bug login prod → 2 người bí đến 10h đêm → root cause do sai step setup → tự rà soát + phối hợp BE trace log → fix đúng, không chặn release.
- Lesson learned: khi bí cùng người khác, đôi khi cần lùi lại tự đọc kỹ từ đầu thay vì tiếp tục thử theo hướng cũ.

**Tồn đọng & rủi ro**: Không có tồn đọng tuần này.

**Cần hỗ trợ**: TL: Không. Manager: Không.

**⭐ IDP tags**: #10 Ownership 4.3 (chủ động support BE + hướng dẫn debug cho iOS) | #1 Innovation 4.6 (fix triệt để BottomSheet) | #9 Ownership 4.2 (quản lý song song nhiều mục tiêu) | #15 Tech R&D 4.6 (rà soát rủi ro billing + login)

**Self-rating**: Vượt kỳ vọng
**Lý do**: Đóng gói + release bản đầu tiên lên chợ đúng cam kết (E1 KS1), xử lý dứt điểm bug login prod khó + BottomSheet dai dẳng, chủ động chuẩn bị plan phase 2 trước khi họp, và optimize thêm ngoài scope để đảm bảo chất lượng. Để giữ đúng tiến độ, đã đầu tư thêm nhiều thời gian ngoài giờ (thường đến 8-9h tối, có hôm 10h đêm) trong suốt tuần.

---

## W30 / 2026 (21/07 – 25/07) — AI Learn: AI Talk (Limit Usage + Tracking + Speech-to-Text)

**Sản phẩm/Phase**: AI Learn — AI Talk (Limit Usage + Tracking + Speech-to-Text)

**IKAME WHAT (KẾT QUẢ)**:
- Limit time usage cho free user: đổi từ limit thời gian ở local sang dùng event quota + API daily của BE — đồng bộ được giữa các thiết bị dùng chung 1 account.
- Triển khai flow limit usage cho Topic: chuyển từ đếm lượt sang limit theo thời gian cho user free, kèm kịch bản IAP cho user Pro.
- Kịch bản IAP cho Video Stream.
- Full tracking (ai_feature, vid_play, ai_tutor, API track, billing, feedback).
- Overview Message cho các conversation đang học.
- Optimize Speech-to-Text Local.
- Triển khai stream Audio qua WebSocket.
- Ghép phần tách message trong AI Talk.
- Review code cho Hiếu.

**IKAME HOW (CÁCH LÀM)**:
- Chủ động nhận phần việc của Hiếu khi Hiếu gặp khó trong ghép IAP SDK — hỗ trợ phân tích, gợi ý hướng xử lý logic phù hợp.
- Nhận thấy chỉ gắn tracking một phần theo kế hoạch ban đầu sẽ không đủ dữ liệu khi có user mới → chủ động gắn full tracking, đồng thời tận dụng AI để rút ngắn thời gian triển khai từ 1.5 ngày xuống 6 tiếng, có self-test đầy đủ.
- Trong lúc làm tracking phát hiện nhiều điểm sai/không phù hợp → chủ động làm việc với team BI để sửa và bổ sung.
- Chủ động đề xuất các kịch bản Learning Map để tối ưu thêm.
- Nhận thấy QA không test đúng timeline → chủ động hỏi tiến độ, xin thêm nguồn lực từ My và Lan Anh. Dù phát sinh chút vấn đề từ chỗ Hòa, vẫn giữ được timeline — Stream Audio ra đúng kế hoạch.
- Nhận thấy BE và AI có vài bug có nguy cơ bị trôi → chủ động liên hệ trước nửa buổi so với thời điểm ghép, đảm bảo timeline không bị ảnh hưởng.
- Chủ động gửi PM các video content dạy tiếng Anh hay, có thể áp dụng cho app ở các phase sau.
- Chủ động test thêm content AI trả ra trong lúc triển khai, đưa góp ý cho team AI để fix/optimize ở phase sau.
- Chủ động test và hotfix mà không cần chờ tester raise (Speech-to-Text local, bug phát sinh trên production).
- Trong cuộc họp plan tuần, chủ động đề nghị team xử lý Time Limit và kịch bản IAP cho Topic.

**IKAME LEVEL UP**:
- Kiến thức: dùng AI hỗ trợ triển khai tracking — rút thời gian từ 1.5 ngày xuống 6 tiếng mà vẫn đảm bảo self-test đầy đủ.
- Làm tốt hơn tuần trước: chủ động phát hiện rủi ro (bug BE/AI có thể trôi, QA lệch timeline) và xử lý trước khi ảnh hưởng đến tiến độ chung.
- Vấn đề khó đã xử lý: Hiếu bí ở phần ghép IAP SDK → phân tích cùng, gợi ý hướng logic phù hợp → Hiếu tự triển khai tiếp được.

**Tồn đọng & rủi ro**: Đã hoàn thành các đầu việc trong tuần, tuy nhiên do ưu tiên đẩy phần IAP của Hiếu lên trước — kéo dài đến cuối ngày thứ 6 — nên phần thay đổi lớn như Stream Audio vẫn chưa được merge và testing. Có thể phát sinh vấn đề khi đưa vào test ở tuần tới.

**Cần hỗ trợ**: TL: Không. Manager: Không.

**⭐ IDP tags**: #5 Continuous Dev 4.3 (mentor Hiếu xử lý IAP SDK + review code) | #1 Innovation 4.6 (dùng AI tăng tốc triển khai tracking) | #9 Ownership 4.2 (quản lý song song tracking + QA resource + risk BE/AI + hotfix) | #15 Tech R&D 4.6 (chủ động quản lý rủi ro bug BE/AI trước thời điểm ghép) | #14 Ownership 4.8 (tự thúc đẩy hotfix chủ động, không chờ tester raise)

**Self-rating**: Vượt kỳ vọng / Xuất sắc (tự chọn)
**Lý do**: Hoàn thành đủ tính năng AI Talk theo cam kết (E1 KS1), dùng AI tối ưu tốc độ triển khai tracking, chủ động quản lý rủi ro nhiều đầu mối (BI/BE/AI/QA) để giữ timeline, đồng thời mentor và review code cho Hiếu xử lý IAP SDK.

---

## W31 / 2026 (28/07 – 01/08) — AI Learn: Bug Fix + Refactor + Tích hợp SDK

**Sản phẩm/Phase**: AI Learn — Bug Fix + Refactor + Tích hợp SDK

**IKAME WHAT (KẾT QUẢ)**:
- Fixbug Avatar.
- Fix bug localize của Hiếu.
- Fix Socket Error Event.
- Fix bug Tracking.
- Release Split Message.
- Tích hợp SDK TikTok và Meta.
- Refactor luồng Login + Logout + Onboarding + IAP.
- Stream Audio Flow – Error case: xử lý dứt điểm case lỗi phát sinh — đóng luôn rủi ro tồn đọng từ tuần trước (Stream Audio chưa merge/test).
- Fix crash Firebase (tăng free crash 99,5% → 99,91%).
- Implement Rating Flow.

**IKAME HOW (CÁCH LÀM)**:
- Chủ động rà soát kết quả trả về từ AI, tổng hợp feedback gửi team AI để cải thiện chất lượng output.
- Chủ động rà soát lại những phần Hiếu đã làm trước đó, clear hết bug tồn đọng thay vì để dồn sang tuần sau.

**IKAME LEVEL UP**:
- Vấn đề khó đã xử lý: Refactor đồng thời 4 luồng liên kết chặt (Login/Logout/Onboarding/IAP) — dọn sạch technical debt trước khi UA đẩy thêm user vào.

**Tồn đọng & rủi ro**: Không có tồn đọng tuần này.

**Cần hỗ trợ**: TL: Không. Manager: Không.

**⭐ IDP tags**: #1 Innovation 4.6 (refactor luồng Login/Logout/Onboarding/IAP, dọn technical debt thay vì code đè) | #5 Continuous Dev 4.3 (rà soát + clear bug tồn đọng phần Hiếu làm trước) | #16 Tech R&D 4.7 (feedback quy trình cho team AI để cải thiện kết quả trả về) | #9 Ownership 4.2 (quản lý song song nhiều đầu việc: bug fix + refactor + tích hợp SDK + support Hiếu)

**Self-rating**: Làm tốt
**Lý do**: Dù nhiều task phát sinh làm đảo lộn timeline đặt ra đầu tuần nhưng mọi việc vẫn được xử lý triệt để.
