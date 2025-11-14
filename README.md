# E. Dự án: "Ngôi nhà Chung" (HousePal) – Trợ lý Quản lý Nhà trọ/Chung cư 
Đây là dự án môn Phát triển ứng dụng cho thiết bị di động của nhóm chúng tôi.
## Thành viên:

- Phạm Đức Phú
- Nguyễn Thành Long
- Tạ Xuân Phong

### 1.Tổng quan Dự án (Project Overview) 
"HousePal" là một ứng dụng di động được thiết kế để giải quyết các xung đột và sự "nhập 
nhằng" phổ biến nhất trong cuộc sống tập thể: Ai sẽ làm việc nhà? và Ai nợ ai bao nhiêu tiền? 
Ứng dụng này là một trung tâm điều hành thu nhỏ cho "ngôi nhà chung", kết hợp ba tính năng 
chính: Lịch phân công Việc nhà, Quản lý Quỹ chung (Split Bill), và một Bảng tin Chung. Mục 
tiêu là mang lại sự minh bạch, công bằng và giảm thiểu các tranh cãi không đáng có. 
### 2.Bối cảnh & Vấn đề (Business Problem & Context) 
Hiện trạng (Current State): Khi sống chung (2 người trở lên), việc duy trì trật tự và công bằng tài 
chính thường dựa trên "tự giác" hoặc các thỏa thuận miệng, dẫn đến 03 "nỗi đau" (Pain Points) 
chính: 
1. "Hội chứng Người vô hình" (The Invisibility Syndrome): Luôn có 1-2 người làm việc 
nhà nhiều hơn (đổ rác, rửa bát, lau nhà), trong khi những người khác "quên" hoặc "nghĩ 
là người khác sẽ làm". Điều này gây ra sự bất mãn và ấm ức ngấm ngầm. 
2. "Nhập nhằng Tiền bạc": Việc chia tiền điện, nước, Internet, hoặc tiền đi chợ chung rất 
lộn xộn. 

    o Ví dụ: Bạn A trả tiền điện, bạn B trả tiền nước. Cuối tháng, họ phải tự cộng/trừ/chia 
để xem ai nợ ai, thường xuyên sai sót hoặc... quên luôn. 
3. Giao tiếp Kém hiệu quả: Các thông báo quan trọng (ví dụ: "Tuần này chủ nhà đến sửa điện", "Hết nước rửa bát rồi") bị trôi đi trong các nhóm chat (Zalo, Messenger) vốn đã quá ồn ào. 

Cơ hội (Opportunity): Xây dựng một nền tảng duy nhất, chuyên biệt cho việc sống chung. Biến 
các "nghĩa vụ" (việc nhà, tiền bạc) thành một "trò chơi" (game) có luật lệ rõ ràng, minh bạch và 
tự động, nơi mọi đóng góp đều được ghi nhận. 
### 3.Đối tượng Người dùng (Target Audience) 
Chân dung người dùng (Persona): "Người ở Ghép" (The Flatmate) 
• Mô tả: Là sinh viên ở chung 4-6 người, hoặc nhóm người đi làm thuê chung một căn hộ. 
• Nhu cầu: 
    
-   Cần sự công bằng và minh bạch (ai đã làm, ai đã trả). 
    
-   Muốn một cách đơn giản để biết việc gì cần làm tiếp theo. 
    
-   Muốn chia tiền nhanh chóng mà không phải tính toán phức tạp. 
### 4. Yêu cầu Chức năng (Functional Requirements - FRs) 
Đây là mô tả chi tiết các tính năng mà hệ thống bắt buộc phải làm được. 

FR1: Module "Lịch Việc nhà" (Chore Wheel) 

• FR1.1: Tạo Việc nhà (Task): Người quản lý "nhà" (admin) có thể tạo các việc nhà lặp lại (ví dụ: "Đổ rác" - hàng ngày, "Lau nhà" - hàng tuần, "Vệ sinh tủ lạnh" - hàng tháng). 

• FR1.2: Phân công Tự động: Hệ thống phải có khả năng tự động xoay vòng (rotate) việc nhà cho các thành viên. (Ví dụ: Tuần này A đổ rác, tuần sau B đổ rác). 

• FR1.3: Xác nhận Hoàn thành: Khi một người hoàn thành việc, họ bấm "Hoàn thành". Hệ thống sẽ ghi lại. 

• FR1.4: "Game hóa" (Gamification): 

-    Mỗi việc nhà hoàn thành sẽ được tính điểm (việc khó nhiều điểm, việc dễ ít điểm). 

-    Hiển thị một "Bảng xếp hạng" hàng tháng để vinh danh "Thành viên Tích cực". (Điều này tạo động lực và bằng chứng xã hội).

FR2: Module "Quỹ chung & Chia tiền" (Shared Wallet & Splitter) 

• FR2.1: Thêm Chi tiêu: Bất kỳ thành viên nào cũng có thể thêm một khoản chi chung (ví dụ: "Tiền điện tháng 11: 500.000đ" hoặc "Đi chợ: 200.000đ"). 

• FR2.2: Phân chia Linh hoạt (Splitting): Khi thêm chi tiêu, người trả có thể chọn cách 
chia: 
-    Chia đều (ví dụ: 500k chia 5 người). 
-    Chia theo tỷ lệ (ví dụ: Bạn A dùng điều hòa nhiều hơn nên trả 30%, còn lại chia 
đều). 
-    Chia theo người (ví dụ: Tiền đi chợ 200k nhưng chỉ có A và B ăn, nên chỉ chia 2). 

• FR2.3: Bảng cân đối "Ai nợ Ai" (Balance Sheet): Đây là tính năng "ăn tiền". Ứng dụng 
phải tự động tính toán và hiển thị một giao diện đơn giản: 
-    Ví dụ: "A đang nợ B: 50.000đ", "C đang nợ A: 20.000đ". 

-    Hệ thống phải đủ thông minh để tối giản nợ (ví dụ: A nợ B 50k, B nợ C 50k -> Hệ thống gợi ý: A trả thẳng C 50k). 

• FR2.4: Chốt/Thanh toán Nợ: Khi A trả tiền cho B, B có thể bấm "Xác nhận đã nhận" và số nợ sẽ về 0. 

FR3: Module "Bảng tin Chung" (House Bulletin) 

• FR3.1: Ghi chú Chung (Notes): Một nơi duy nhất để ghim các thông tin quan trọng (ví dụ: "Mật khẩu Wifi: ...", "Số điện thoại chủ nhà: ..."). 

• FR3.2: Danh sách Mua sắm Chung (Shared List): Bất kỳ ai cũng có thể thêm vào (ví dụ: "Hết giấy vệ sinh", "Cần mua nước rửa bát"). Người đi chợ có thể xem và mua, sau đó chuyển khoản mục đó sang module Chi tiêu (FR2). 

### 5.Yêu cầu Phi chức năng (Non-Functional Requirements - NFRs) 

• NFR1: Tính đồng bộ (Synchronization): Dữ liệu phải được cập nhật thời gian thực (realtime). Khi A thêm một khoản chi, B phải thấy ngay lập tức. (Sử dụng WebSocket hoặc 
Firestore là lý tưởng). 

• NFR2: Trải nghiệm Người dùng (UX): Thao tác thêm chi tiêu và xác nhận việc nhà phải cực kỳ nhanh (dưới 3 cú chạm) vì đây là các hành động lặp lại hàng ngày. 

• NFR3: Tính chính xác (Accuracy): Thuật toán tính toán nợ (FR2.3) phải chính xác tuyệt đối. 

• NFR4: Thông báo (Notifications): Gửi thông báo đẩy khi: 

-    "Đến lượt bạn đổ rác!" (FR1.2). 
-    "Bạn A vừa thêm một khoản chi mới, bạn nợ A 100.000đ" (FR2.3). 

### 6.Ràng buộc & Giả định (Constraints & Assumptions) 
• Ràng buộc 1: Ứng dụng không xử lý giao dịch tiền thật. Nó chỉ là một "cuốn sổ" ghi nợ và theo dõi. Việc thanh toán thật vẫn diễn ra bên ngoài (chuyển khoản, tiền mặt). 

• Giả định 1 (Lớn nhất): Cần có ít nhất một người trong nhà "chủ trì" (admin) để thiết lập các việc nhà và quy tắc ban đầu.

• Giả định 2: Các thành viên trung thực trong việc nhập chi tiêu (FR2.1) và xác nhận hoàn thành công việc (FR1.3). (Yếu tố "Bảng xếp hạng" sẽ giúp thúc đẩy điều này).
