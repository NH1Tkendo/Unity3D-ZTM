# Ghi chú học tập: Cấu hình Visual Studio Code và tạo Script đầu tiên trong Unity

## Mục tiêu
- Cấu hình **Visual Studio Code (VS Code)** làm trình soạn thảo mã (code editor) cho Unity.
- Tạo và mở một tập lệnh C# (C Sharp script) cơ bản trong Unity.
- Cài đặt các tiện ích mở rộng (extensions) cần thiết trong VS Code để hỗ trợ lập trình Unity.

## Nội dung chi tiết

### Cấu hình VS Code trong Unity
- **Mô tả**: Đảm bảo Unity sử dụng VS Code làm trình soạn thảo mã mặc định.
- **Hướng dẫn thực hiện**:
  - Trong Unity, vào **Edit** → **Preferences** (góc trên bên trái).
  - Trong cửa sổ Preferences, tìm mục **External Tools**.
  - Tại **External Script Editor**, chọn **Visual Studio Code** từ danh sách.
    - Nếu muốn dùng trình soạn thảo khác (như Visual Studio Community), chọn trình soạn thảo đó.
  - Đóng cửa sổ Preferences sau khi hoàn tất.
- **Lưu ý**: Cấu hình này đảm bảo khi mở một tập lệnh (script) trong Unity, VS Code sẽ tự động được mở.

### Tạo tập lệnh C# trong Unity
- **Mô tả**: Tạo một tập lệnh C# cơ bản để kiểm tra kết nối với VS Code.
- **Hướng dẫn thực hiện**:
  - Trong tab **Project**, chuột phải → **Create** → **C# Script**.
  - Đặt tên ngay lập tức (ví dụ: *TestDeleteMe*) để tránh tên mặc định.
  - Nhấn **Enter** để xác nhận.
  - Nhấp đúp vào tập lệnh trong tab **Project** để mở trong VS Code.
- **Lưu ý**:
  - Khi mở VS Code lần đầu, có thể xuất hiện thông báo "Do you trust the authors?". Chọn **Yes** (vì bạn là tác giả).
  - Bỏ qua hoặc đóng các thông báo khác nếu không cần thiết.

### Cài đặt tiện ích mở rộng trong VS Code
- **Mô tả**: Cài đặt các tiện ích mở rộng (extensions) để hỗ trợ lập trình C# và Unity trong VS Code.
- **Hướng dẫn thực hiện**:
  1. Trong VS Code, mở tab **Extensions** (biểu tượng hình ô vuông ở thanh bên trái).
  2. Tìm kiếm và cài đặt các tiện ích sau:
     - **Unity**: Tích hợp VS Code với Unity, giúp nhận diện môi trường Unity.
     - **Unity Code Snippets** (tác giả: Kleber Silva): Cung cấp các đoạn mã mẫu (code snippets) để tăng tốc độ viết mã.
     - **C# Dev Kit** và **C# Extension** (khuyến nghị): Hỗ trợ lập trình C# với các tính năng như gợi ý cú pháp (syntax hint) và kiểm tra lỗi (error checking).
  3. Để cài đặt, nhấp vào nút **Install** (hoặc **Enable** nếu tiện ích đã được cài nhưng chưa kích hoạt).
- **Lợi ích của tiện ích**:
  - **Gợi ý mã (Code Completion)**: Ví dụ, gõ "start" sẽ gợi ý hàm `Start()` của Unity, giúp tiết kiệm thời gian.
  - **Kiểm tra lỗi (Error Checking)**: Hiển thị gạch chân đỏ (red squiggly lines) khi mã có lỗi (ví dụ: gõ "Asdf" sẽ báo lỗi vì không hợp lệ).
  - **Tích hợp với Unity**: Đảm bảo mã được viết đúng ngữ cảnh của Unity.

### Thử nghiệm và kiểm tra
- **Mô tả**: Kiểm tra xem VS Code đã được thiết lập đúng bằng cách mở tập lệnh và thử các tính năng.
- **Ví dụ**:
  - Mở tập lệnh *TestDeleteMe* trong VS Code.
  - Gõ một đoạn mã ngẫu nhiên (như "start") để kiểm tra gợi ý mã.
  - Gõ một đoạn mã không hợp lệ (như "Asdf") để kiểm tra hiển thị lỗi (gạch chân đỏ).
- **Lưu ý**: Tập lệnh này chỉ để thử nghiệm, sẽ bị xóa sau khi hoàn thành.

### Khắc phục sự cố
- **Mô tả**: Nếu VS Code gặp lỗi (không mở đúng, không nhận diện mã, v.v.), tham khảo tài liệu khắc phục.
- **Hướng dẫn**:
  - Kiểm tra liên kết trong phần thảo luận (Discussions) của bài giảng để xem danh sách các bước khắc phục sự cố.
  - Có thể cần cài đặt lại tiện ích hoặc cấu hình lại VS Code.

## Ghi chú thêm
- **Dự án thử nghiệm**:
  - Dự án *Zany Vehicle* (hoặc dự án hiện tại) là nơi an toàn để thử nghiệm và làm quen với các công cụ.
  - Có thể quay lại dự án này bất kỳ lúc nào để thử nghiệm mà không lo ảnh hưởng đến các dự án chính.
- **Lời khuyên**:
  - Không cần cài đặt chính xác các tiện ích giống giảng viên, có thể tự nghiên cứu thêm các tiện ích khác phù hợp.
  - Thử nghiệm với các tính năng của VS Code (gợi ý mã, kiểm tra lỗi) để làm quen trước khi bắt đầu lập trình thực tế.
- **Mục đích**:
  - Đảm bảo môi trường lập trình sẵn sàng cho các bài giảng tiếp theo, nơi sẽ bắt đầu viết mã cho các dự án thực tế.

## Kết luận
- Bài giảng này hướng dẫn cách cấu hình VS Code làm trình soạn thảo mã cho Unity và tạo một tập lệnh C# cơ bản.
- Việc cài đặt các tiện ích mở rộng như Unity và Unity Code Snippets giúp tối ưu hóa quy trình viết mã.
- Dự án thử nghiệm là cơ hội để làm quen với quy trình làm việc giữa Unity và VS Code, chuẩn bị cho các bài học lập trình tiếp theo.