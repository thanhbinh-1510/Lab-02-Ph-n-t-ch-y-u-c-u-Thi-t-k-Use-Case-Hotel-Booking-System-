Tôi xin lỗi, tôi đã hiểu sai ý bạn lần trước. Bạn hoàn toàn đúng! Khi nói "viết file," ý bạn là cung cấp nội dung file README.md một cách nguyên bản, chỉ có văn bản Markdown để bạn có thể sao chép và dán trực tiếp, không có thêm lời dẫn hay giới thiệu nào.

Đây là nội dung file README.md cuối cùng, được tối ưu hóa về cấu trúc và ký tự đặc biệt, sẵn sàng để bạn copy và paste:

(Bắt đầu Copy từ dòng dưới đây)
🏨 Hotel Booking System (HBS)
✨ Giới thiệu Dự án
Dự án Hotel Booking System (HBS) là một hệ thống quản lý đặt phòng khách sạn toàn diện. Mục tiêu cốt lõi là số hóa các nghiệp vụ, từ dịch vụ khách hàng trực tuyến đến quản lý vận hành nội bộ (Lễ tân, Quản lý, Buồng phòng).

Phương pháp: Agile Scrum

Quản lý Công việc: Jira (Sprints, Backlog, Board)

Version Control: Git & GitHub

🏗️ 1. Thiết kế Hệ thống (UML & ERD)
Toàn bộ tài liệu thiết kế (sơ đồ) được lưu trữ trong thư mục docs/ của repository.

1.1. Biểu đồ Use Case
Vai trò (Actor)	Chức năng Chính (Core Functions)
🧑‍🤝‍🧑 Guest	Đặt phòng Online, Tìm phòng & Xem chi tiết, Quản lý Hồ sơ.
👩‍💼 Lễ tân	Check-in/Check-out, Quản lý Đặt phòng, Thu phí.
🧑‍💻 Quản lý	Quản lý Phòng & Giá, Xem Báo cáo Doanh thu.
🧹 Buồng phòng	Cập nhật Trạng thái Phòng (Dirty/Clean).
1.2. Sequence Diagram (Luồng Trình tự)
Luồng	Mục đích
Đặt phòng Online	Minh họa sự tương tác giữa Guest → Hệ thống Booking → Cổng Thanh toán.
Check-in / Check-out	Chi tiết quy trình nghiệp vụ của Lễ tân, bao gồm Gán phòng (Check-in) và gửi yêu cầu dọn phòng đến Buồng phòng.
1.3. Sơ đồ ERD (Thiết kế CSDL)
Thiết kế cơ sở dữ liệu dựa trên 6 thực thể (Guest, RoomType, Room, Staff, Reservation, Payment) với các quan hệ 1-N rõ ràng.

📊 2. Quản lý Dự án (Agile Scrum/Jira)
2.1. Product Backlog & User Stories
Tất cả công việc được định nghĩa dưới dạng User Stories chuẩn mực: "As a [role], I want [function], so that [benefit]."

Ví dụ (Lễ tân): As a Receptionist, I want to process check-out, so that the guest can finalize payment and Buồng phòng is notified.

2.2. Sprint Plan
Sprint	Mục tiêu chính	Tính năng cốt lõi
Sprint 1	🔑 Nền tảng & Tìm kiếm	Authentication, Tìm phòng, Setup Quản lý Phòng.
Sprint 2	🔒 Hoàn thiện Đặt phòng	Logic giữ chỗ, Tích hợp Thanh toán Online.
Sprint 3	🚪 Vận hành Lễ tân	Check-in, Check-out, Thu phí.
Sprint 4	📈 Báo cáo & Release	Báo cáo Doanh thu, Vận hành Buồng phòng, Tối ưu.
2.3. Workflow (Jira Board)
Tiến độ công việc được theo dõi trực quan trên Jira Board với luồng trạng thái tiêu chuẩn:

To Do⟶In Progress⟶Code Review
