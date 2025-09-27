# Ghi chú học tập: Thiết lập môi trường phát triển Unity và Visual Studio Code

## Mục tiêu
- Cài đặt **Unity Hub** và **Unity 6** để bắt đầu phát triển trò chơi.
- Cài đặt **Visual Studio Code** (VS Code) làm trình soạn thảo mã (code editor).
- Hiểu vai trò của công cụ phát triển trò chơi (game engine) và trình soạn thảo mã.

## Nội dung chi tiết

### Cài đặt Unity Hub
- **Mô tả**:
  - Unity Hub là công cụ quản lý các phiên bản Unity và các dự án.
  - Tải Unity Hub từ trang web chính thức: [unity.com/download](https://unity.com/download).
- **Hướng dẫn cài đặt**:
  - Tải file cài đặt từ nút "Download" trên trang web.
  - Thực hiện cài đặt theo hướng dẫn trên màn hình (chọn "Yes" khi được yêu cầu).
  - Nếu cần, tạo tài khoản Unity miễn phí bằng email để đăng nhập.
- **Lưu ý**:
  - Unity Hub hiển thị các mục như Projects, Installs, Learn, Community.
  - Chọn mục **Installs** → **Install Editor** → chọn phiên bản **Unity 6 Preview** (hoặc phiên bản chính thức LTS - Long Term Support).
  - Đề xuất cài đặt thêm **WebGL Build Support** để hỗ trợ xuất trò chơi lên website.
  - Có thể bỏ qua các tùy chọn như Android hoặc iOS build support vì khóa học không tập trung vào phát triển game di động.
  - Có thể quay lại cài đặt thêm các thành phần sau nếu cần.

### Cài đặt Visual Studio Code
- **Mô tả**:
  - Visual Studio Code (VS Code) là trình soạn thảo mã được sử dụng trong khóa học vì giao diện đồng nhất trên Windows và Mac.
- **Hướng dẫn cài đặt**:
  - Tải VS Code từ trang web chính thức theo hệ điều hành (Windows/Mac).
  - Thực hiện cài đặt theo hướng dẫn, chấp nhận các thiết lập mặc định.
- **Lưu ý**:
  - VS Code sẽ được cấu hình chi tiết trong các bài giảng sau.
  - Có thể cài đặt song song với Unity Hub, để quá trình tải diễn ra trong nền.

### Khái niệm cơ bản
- **Công cụ phát triển trò chơi (Game Engine)**:
  - Unity là một công cụ phát triển trò chơi cung cấp giao diện trực quan và các hệ thống tích hợp sẵn:
    - Hệ thống vật lý (physics system).
    - Hệ thống hiển thị đồ họa (rendering).
    - Hệ thống âm thanh (audio system).
  - So sánh với các game engine khác: Unreal, Godot, Game Maker.
  - Lợi ích: Giúp rút ngắn thời gian phát triển bằng cách cung cấp các công cụ và mã có sẵn.
- **Trình soạn thảo mã (Code Editor)**:
  - VS Code là nơi viết mã nguồn (code) để điều khiển Unity.
  - Cung cấp các tính năng như gợi ý cú pháp (syntax hint), kiểm tra lỗi (error checking).
  - So sánh với các trình soạn thảo khác: Visual Studio Community, Rider, Notepad++.
  - Mã nguồn được lưu dưới dạng **tệp C# (C Sharp scripts)**, chứa các lệnh để điều khiển hành vi của đối tượng trong trò chơi (game object).
- **Cách hoạt động**:
  - Viết mã trong VS Code → lưu thành tệp C# → Unity đọc và thực thi các lệnh.
  - Ví dụ: Lệnh di chuyển một đối tượng trong game (move game object forward by 10 units).

## Ghi chú thêm
- **Lưu ý về phiên bản**:
  - Sử dụng Unity 6 hoặc phiên bản mới hơn để đảm bảo tương thích với nội dung khóa học.
  - Nếu gặp vấn đề, có thể quay lại cài đặt đúng phiên bản Unity 6 để đồng bộ giao diện với giảng viên.
- **Thời gian cài đặt**:
  - Thời gian tải và cài đặt phụ thuộc vào tốc độ internet.
  - Có thể thực hiện đồng thời việc tải Unity Hub và VS Code để tiết kiệm thời gian.
- **Khuyến nghị**:
  - Làm quen với giao diện Unity Hub (Projects, Installs, Learn, Community).
  - Không cần lo lắng về các tùy chọn cài đặt bổ sung (Android/iOS) vào thời điểm này, có thể quay lại sau.

## Kết luận
- Phần này tập trung vào thiết lập môi trường phát triển với Unity Hub, Unity 6, và VS Code.
- Hiểu rõ vai trò của game engine và code editor sẽ giúp người học dễ dàng tiếp cận các bài giảng tiếp theo.
- Cần hoàn thành cài đặt trước khi chuyển sang các bài thực hành lập trình và xây dựng trò chơi.