🏨 Hotel Booking System (HBS)
📌 Giới thiệu Dự án
Dự án Hotel Booking System (HBS) là một hệ thống quản lý đặt phòng khách sạn toàn diện. Mục tiêu là số hóa các nghiệp vụ cốt lõi, từ dịch vụ khách hàng (đặt phòng online) đến vận hành nội bộ (Check-in/out, Báo cáo).

Dự án được triển khai theo phương pháp Agile Scrum, sử dụng Jira để quản lý và GitHub để kiểm soát phiên bản.

🏗️ 1. Thiết kế Hệ thống (UML & ERD)
Toàn bộ tài liệu thiết kế chi tiết (sơ đồ) được lưu trữ trong thư mục docs/ của repository này.

1.1. Biểu đồ Use Case
Vai trò (Actor)	Chức năng Chính (Core Functions)
Guest	Đặt phòng Online, Tìm phòng & Xem chi tiết, Quản lý Hồ sơ.
Lễ tân	Check-in/Check-out, Quản lý Đặt phòng, Thu phí.
Quản lý	Quản lý Phòng & Giá, Xem Báo cáo Doanh thu.
Buồng phòng	Cập nhật Trạng thái Phòng (Dirty/Clean).
1.2. Sequence Diagram (Luồng Trình tự)
Luồng	Mục đích
Đặt phòng Online	Minh họa sự tương tác giữa Guest → Hệ thống Booking → Cổng Thanh toán, xử lý thành công/thất bại của giao dịch.
Check-in / Check-out	Chi tiết quy trình nghiệp vụ của Lễ tân, bao gồm: Gán phòng (Check-in), Thu phí, và gửi yêu cầu dọn phòng (Yêu cầu dọn phòng) đến Buồng phòng.
1.3. Sơ đồ ERD (Thiết kế CSDL)
Thiết kế cơ sở dữ liệu dựa trên 6 thực thể chính, liên kết bằng các quan hệ 1-N:

Entities: Guest, RoomType, Room, Staff, Reservation, Payment.

Mối quan hệ chính: Guest 1–N Reservation, Room 1–N Reservation, Reservation 1–N Payment.

🚀 2. Quản lý Dự án (Agile Scrum/Jira)
2.1. Product Backlog & User Stories
Tất cả công việc được định nghĩa dưới dạng User Stories chuẩn mực:

"As a [role], I want [function], so that [benefit]."

2.2. Sprint Plan
Sprint	Mục tiêu chính	Tính năng cốt lõi
Sprint 1	Nền tảng & Tìm kiếm	Authentication, Tìm phòng, Setup Quản lý Phòng.
Sprint 2	Hoàn thiện Đặt phòng	Logic giữ chỗ, Tích hợp Thanh toán Online.
Sprint 3	Vận hành Lễ tân	Check-in, Check-out, Thu phí.
Sprint 4	Báo cáo & Release	Báo cáo Doanh thu, Vận hành Buồng phòng, Tối ưu & Release.
2.3. Workflow (Jira Board)
Tiến độ công việc được theo dõi trực quan trên Jira Board với luồng trạng thái tiêu chuẩn:

To Do⟶In Progress⟶Code Review⟶Testing⟶Done
(Tài liệu này tổng hợp kết quả của Bài Lab 02: Phân tích & Thiết kế Hệ thống Đặt phòng Khách sạn)



dr hãy trình bày md



Tuyệt vời! Bạn muốn tôi trình bày lại file README.md với định dạng Markdown (MD) tối ưu, chuyên nghiệp và nổi bật nhất để bạn chỉ cần sao chép (copy) toàn bộ và dán (paste) vào Repository GitHub của mình.

Đây là phiên bản cuối cùng, được tối ưu hóa về mặt trình bày:

🏨 Hotel Booking System (HBS)
📌 Giới thiệu Dự án
Dự án Hotel Booking System (HBS) là một hệ thống quản lý đặt phòng khách sạn toàn diện. Mục tiêu là số hóa các nghiệp vụ cốt lõi, từ dịch vụ khách hàng (đặt phòng online) đến vận hành nội bộ (Lễ tân, Quản lý, Buồng phòng).

Dự án này được triển khai theo phương pháp Agile Scrum, sử dụng Jira để quản lý tiến độ và GitHub để kiểm soát phiên bản và lưu trữ tài liệu.

🏗️ 1. Thiết kế Hệ thống (UML & ERD)
Toàn bộ tài liệu thiết kế chi tiết (sơ đồ) được lưu trữ trong thư mục docs/ của repository.

1.1. Biểu đồ Use Case
Vai trò (Actor)	Chức năng Chính (Core Functions)
Guest	Đặt phòng Online, Tìm phòng & Xem chi tiết, Quản lý Hồ sơ.
Lễ tân	Check-in/Check-out, Quản lý Đặt phòng, Thu phí.
Quản lý	Quản lý Phòng & Giá, Xem Báo cáo Doanh thu.
Buồng phòng	Cập nhật Trạng thái Phòng (Dirty/Clean).
1.2. Sequence Diagram (Luồng Trình tự)
Luồng	Mục đích
Đặt phòng Online	Minh họa sự tương tác giữa Guest → Hệ thống Booking → Cổng Thanh toán, xử lý thành công hoặc thất bại của giao dịch.
Check-in / Check-out	Chi tiết quy trình nghiệp vụ của Lễ tân, bao gồm: Gán phòng (Check-in), Thu phí, và gửi yêu cầu dọn phòng (Yêu cầu dọn phòng) đến Buồng phòng.
1.3. Sơ đồ ERD (Thiết kế CSDL)
Thiết kế cơ sở dữ liệu dựa trên 6 thực thể chính, liên kết bằng các quan hệ 1-N để đảm bảo tính toàn vẹn dữ liệu:

Entities: Guest, RoomType, Room, Staff, Reservation, Payment.

Mối quan hệ chính: Guest 1–N Reservation, Room 1–N Reservation, Reservation 1–N Payment.

🚀 2. Quản lý Dự án (Agile Scrum/Jira)
2.1. Product Backlog & User Stories
Tất cả công việc được định nghĩa dưới dạng User Stories chuẩn mực: "As a [role], I want [function], so that [benefit]."

Ví dụ (Guest): As a Guest, I want to search for available rooms by date, so that I can choose the best room that fits my needs.

Ví dụ (Lễ tân): As a Receptionist, I want to process check-out, so that the guest can finalize payment and Buồng phòng is notified.

2.2. Sprint Plan
Sprint	Mục tiêu chính	Tính năng cốt lõi
Sprint 1	Nền tảng & Tìm kiếm	Authentication, Tìm phòng, Setup Quản lý Phòng.
Sprint 2	Hoàn thiện Đặt phòng	Logic giữ chỗ, Tích hợp Thanh toán Online.
Sprint 3	Vận hành Lễ tân	Check-in, Check-out, Thu phí.
Sprint 4	Báo cáo & Release	Báo cáo Doanh thu, Vận hành Buồng phòng, Tối ưu & Release.
2.3. Workflow (Jira Board)
Tiến độ công việc được theo dõi trực quan trên Jira Board với luồng trạng thái tiêu chuẩn:

To Do⟶In Progress⟶Code Review⟶Testing⟶Done
