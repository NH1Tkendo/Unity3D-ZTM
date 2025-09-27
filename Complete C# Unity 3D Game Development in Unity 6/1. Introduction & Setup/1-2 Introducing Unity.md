# Ghi chú học tập: Làm quen với giao diện Unity và tạo dự án Zany Vehicle

## Mục tiêu
- Hiểu và làm quen với giao diện Unity (Unity Interface).
- Thực hành tạo và thao tác với các đối tượng trò chơi (Game Objects).
- Xây dựng một dự án nhỏ "Zany Vehicle" để thực hành sử dụng các công cụ cơ bản trong Unity.

## Nội dung chi tiết

### Thiết lập dự án mới trong Unity Hub
- **Mô tả**: Tạo một dự án mới trong Unity Hub để bắt đầu làm việc.
- **Hướng dẫn thực hiện**:
  - Mở **Unity Hub** → chọn **Projects** → nhấn **New Project** (góc trên bên phải).
  - Chọn phiên bản **Unity 6** (hoặc phiên bản mới hơn).
  - Chọn mẫu (template): **Universal 3D** (phù hợp cho các dự án cơ bản, không yêu cầu đồ họa cao cấp như High Definition Pipeline).
  - Đặt tên dự án (ví dụ: *My Zany Vehicle*).
  - Chọn vị trí lưu dự án trên ổ cứng.
  - Tắt tùy chọn **Connect to Unity Cloud** (không cần thiết cho dự án này).
  - Nhấn **Create Project** và chờ Unity khởi tạo.
- **Lưu ý**:
  - Nếu giao diện Unity không giống mặc định, vào **Layout** (góc trên bên phải) → chọn **Default**.
  - Có thể điều chỉnh kích thước cửa sổ bằng cách kéo thả giữa các cửa sổ hoặc di chuyển các tab.

### Tổng quan giao diện Unity
- **Các thành phần chính**:
  - **Hierarchy**: Hiển thị danh sách các đối tượng trò chơi (Game Objects) trong cảnh (Scene).
    - Ví dụ: *Main Camera*, *Directional Light*, *Global Volume*.
  - **Scene**: Khu vực trực quan để xem và chỉnh sửa các đối tượng trong không gian 3D.
  - **Inspector**: Hiển thị chi tiết và các thành phần (Components) của đối tượng được chọn.
  - **Project**: Chứa các tài nguyên (Assets) của dự án, như vật liệu (Materials), cảnh (Scenes), v.v.
- **Thành phần của Game Object**:
  - Mỗi Game Object có một **Transform Component** (vị trí, xoay, tỷ lệ).
  - Các thành phần khác (như *Light Component* cho ánh sáng, *Camera Component* cho máy quay) xác định chức năng của Game Object.

### Thao tác điều hướng trong Scene
- **Điều hướng**:
  - **Di chuyển (Pan)**: Giữ nút chuột giữa và kéo (hoặc **Alt + chuột trái**).
  - **Xoay (Rotate)**: Giữ **Alt + chuột trái** và kéo.
  - **Phóng to/thu nhỏ (Zoom)**: Giữ **Alt + chuột phải** và kéo.
  - **Di chuyển tự do (Fly)**: Giữ chuột phải + dùng phím **WASD** để di chuyển, **Q** để hạ xuống, **E** để nâng lên.
- **Thao tác với đối tượng**:
  - **Công cụ di chuyển (Move Tool)**: Phím **W** → kéo các trục (X: đỏ, Y: xanh lá, Z: xanh dương).
  - **Công cụ xoay (Rotate Tool)**: Phím **E** → xoay đối tượng theo các trục.
  - **Công cụ tỷ lệ (Scale Tool)**: Phím **R** → thay đổi kích thước đối tượng.
  - **Đặt lại (Reset)**: Chuột phải vào **Transform** trong Inspector → chọn **Reset** để đưa về vị trí (0, 0, 0).

### Thực hành tạo Zany Vehicle
- **Mô tả**: Tạo một phương tiện đơn giản (xe) bằng cách sử dụng các Game Objects và vật liệu (Materials).
- **Hướng dẫn thực hiện**:
  1. **Tạo thân xe (Car Body)**:
     - Trong **Hierarchy**, chuột phải → **3D Object** → **Cube**.
     - Đổi tên thành *Car Body* trong Hierarchy.
     - Sử dụng phím **R** để điều chỉnh tỷ lệ (scale) thành hình dạng giống thân xe (ví dụ: làm phẳng theo trục Y).
  2. **Tạo bánh xe (Wheel)**:
     - Chuột phải trong **Hierarchy** → **3D Object** → **Cylinder**.
     - Đổi tên thành *Wheel*.
     - Sử dụng **W** để di chuyển, **E** để xoay (ví dụ: xoay 90 độ trên trục X), **R** để điều chỉnh tỷ lệ.
     - Giữ phím **Ctrl** khi xoay để căn chỉnh theo góc 15 độ.
  3. **Tạo vật liệu (Material)**:
     - Trong **Project** → chuột phải → **Create** → **Material**.
     - Đổi tên (ví dụ: *Color1*).
     - Trong **Inspector**, chỉnh sửa màu sắc trong **Base Map** (trước đây gọi là Albedo) bằng cách nhấp vào ô màu (color swatch).
     - Kéo vật liệu từ **Project** vào Game Object trong **Hierarchy** hoặc **Scene** để áp dụng.
  4. **Nhân bản (Duplicate)**:
     - Chọn Game Object (ví dụ: *Wheel*) → nhấn **Ctrl+D** (hoặc **Cmd+D** trên Mac) để nhân bản.
     - Di chuyển bản sao đến vị trí phù hợp (ví dụ: bánh xe thứ hai).
  5. **Tùy chỉnh thêm**:
     - Tạo thêm các đối tượng như kính chắn gió (windscreen), đèn pha (headlights) bằng cách nhân bản và điều chỉnh Cube.
     - Tạo thêm vật liệu mới (nhân bản từ *Color1*) và áp dụng màu khác (ví dụ: màu xanh lá cho thân xe).
- **Lưu ý**:
  - Không cần quá chi tiết hoặc chính xác, mục tiêu là làm quen với giao diện và công cụ.
  - Các đối tượng như *Global Volume* có thể được di chuyển ra khỏi khu vực làm việc để tránh nhầm lẫn.

### Quản lý tài nguyên (Assets)
- **Khái niệm**:
  - **Assets** (trong tab Project) là các tệp được lưu trên ổ cứng (materials, scenes, v.v.).
  - **Game Objects** (trong Hierarchy) là các đối tượng tồn tại trong cảnh hiện tại (Scene).
- **Ví dụ**:
  - Cảnh *Sample Scene* được lưu trong thư mục **Scenes** trên ổ cứng (có thể xem bằng cách chuột phải → **Show in Explorer**).
  - Kích thước tệp *Sample Scene* hiện tại khoảng 12KB.

### Thử thách: Tạo Zany Vehicle
- **Yêu cầu**:
  - Tạo một phương tiện độc đáo bằng cách sử dụng các hình dạng Game Object (Cube, Cylinder, v.v.) và vật liệu.
  - Thêm các yếu tố sáng tạo như mặt đất (ground), đèn pha, hoặc các vật thể khác.
  - Không cần quá phức tạp, chỉ cần dành 5-10 phút.
- **Hướng dẫn nộp bài**:
  - Chụp ảnh màn hình (screenshot) phương tiện đã tạo.
  - Chia sẻ trong phần thảo luận (Discussions) hoặc Q&A của khóa học.

## Ghi chú thêm
- **Lời khuyên**:
  - Không cần lo lắng về việc đặt tên hoàn hảo hoặc làm sai, đây chỉ là bài tập thực hành.
  - Thử nghiệm với các công cụ di chuyển, xoay, tỷ lệ để làm quen.
  - Hierarchy có thể trở nên lộn xộn khi thêm nhiều đối tượng, nhưng không cần chỉnh sửa ngay trong dự án này.
- **Mục đích**:
  - Làm quen với giao diện Unity và các thao tác cơ bản.
  - Tăng sự tự tin khi làm việc với Game Objects và Assets.

## Kết luận
- Bài giảng này giới thiệu cách sử dụng giao diện Unity, tạo và chỉnh sửa Game Objects, cũng như áp dụng vật liệu.
- Dự án *Zany Vehicle* là một bài tập thú vị để thực hành các kỹ năng cơ bản, chuẩn bị cho các dự án phức tạp hơn trong khóa học.