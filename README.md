🏨 Hotel Booking System (HBS)
1. Giới thiệu Dự án
Dự án Hotel Booking System (HBS) là một hệ thống quản lý đặt phòng khách sạn toàn diện được thiết kế để số hóa các quy trình cốt lõi, từ việc đặt phòng online của khách hàng đến các nghiệp vụ quản lý nội bộ như check-in/check-out và buồng phòng.

Dự án này được xây dựng theo phương pháp Agile Scrum, sử dụng Jira để quản lý tiến độ và GitHub để kiểm soát phiên bản.

2. Thiết kế Hệ thống (UML & ERD)
2.1. Biểu đồ Use Case (Mục 1.2)
Biểu đồ Use Case mô tả các chức năng chính của hệ thống, phân chia rõ ràng theo 5 vai trò chính:

Vai trò (Actor)	Chức năng cốt lõi
Guest (Khách hàng)	Đặt phòng Online, Tìm phòng, Xem chi tiết, Thanh toán Online.
Lễ tân	Quản lý Đặt phòng, Check-in Khách hàng, Check-out & Thu phí.
Quản lý	Quản lý Phòng & Giá, Xem Báo cáo Doanh thu.
Buồng phòng	Cập nhật Trạng thái Phòng (sau khi có yêu cầu dọn phòng).
Payment Gateway	Xử lý thanh toán.
2.2. Sequence Diagram (Mục 1.3)
Luồng	Mô tả
Đặt phòng Online	Minh họa sự tương tác giữa Guest → Hệ thống Booking → Cổng Thanh toán, bao gồm các luồng rẽ nhánh (alt) cho Thanh toán thành công và Thanh toán thất bại.
Check-in / Check-out	Mô tả luồng nghiệp vụ của Lễ tân, bao gồm: Gán phòng thực tế (Check-in) và Tổng hợp chi phí, Ghi nhận thanh toán, và gửi yêu cầu Yêu cầu dọn phòng đến Phân hệ Buồng phòng (Check-out).
(Các sơ đồ chi tiết có thể được tìm thấy trong thư mục docs/)

2.3. Sơ đồ Thực thể Quan hệ (ERD) (Mục 1.4)
Thiết kế cơ sở dữ liệu được xây dựng dựa trên 6 thực thể chính, liên kết với nhau bằng các mối quan hệ 1-N:

Thực thể (Bảng)	Khóa chính (PK)	Mối quan hệ 1-N
Guest, RoomType, Room, Staff	GuestID, TypeID, RoomID, StaffID	-
Reservation	ResvID (PK)	FKs: GuestID, RoomID, StaffID
Payment	PaymentID (PK)	FK: ResvID
(Sơ đồ ERD chi tiết có thể được tìm thấy trong thư mục docs/)

3. Quản lý Dự án (Agile Scrum/Jira)
Dự án được quản lý theo mô hình Scrum với các công cụ và quy trình sau:

3.1. Product Backlog (User Stories)
Toàn bộ công việc được định nghĩa dưới dạng User Stories chuẩn: "As a [role], I want [function], so that [benefit]."

Vai trò	Ví dụ User Story
Guest	As a Guest, I want to search for available rooms by date, so that I can choose the best room.
Lễ tân	As a Receptionist, I want to process check-out, so that the guest can finalize payment and Buồng phòng is notified.
Quản lý	As a Manager, I want to view revenue reports, so that I can track business performance.
3.2. Sprint Plan (Kế hoạch 4 Sprints)
Sprint	Mục tiêu chính	Tính năng tập trung
Sprint 1	Nền tảng & Tìm kiếm	Authentication, Tìm phòng, Xem chi tiết.
Sprint 2	Đặt phòng & Thanh toán	Đặt phòng, Logic giữ chỗ, Tích hợp Thanh toán.
Sprint 3	Vận hành Khách sạn	Check-in, Check-out, Thu phí.
Sprint 4	Báo cáo & Release	Báo cáo doanh thu, Vận hành Buồng phòng, Tối ưu & Release.
3.3. Workflow (Jira Board)
Tiến độ công việc được theo dõi trên Jira Board với luồng trạng thái tiêu chuẩn:

To Do → In Progress → Code Review → Testing → Done
