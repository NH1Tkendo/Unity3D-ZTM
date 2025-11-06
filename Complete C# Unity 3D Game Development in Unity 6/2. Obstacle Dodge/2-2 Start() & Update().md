## Start và Update - Di chuyển Game Object

Bài học giới thiệu sự khác biệt giữa hai phương thức Start và Update trong Unity, đồng thời hướng dẫn viết code cơ bản để di chuyển đối tượng trên màn hình.

## Thiết lập dự án mới

**Tạo project Unity**:

- Mở Unity Hub → Projects → New Project
    
- Chọn Universal 3D làm rendering pipeline (phù hợp cho hầu hết các dự án prototype)
    
- Đặt tên: "Obstacle Dodge"
    
- Tắt Unity Cloud nếu không cần thiết
    
- Click Create Project (mất khoảng 1 phút)
    

**Thêm các đối tượng cơ bản**:

- Right-click trong Hierarchy → 3D Object → Plane (đổi tên thành "Ground")
    
- Phóng to plane bằng công cụ Scale (phím R)
    
- Right-click → 3D Object → Cube (đổi tên thành "Dodgy" - tên nhân vật)
    
- Nén cube theo trục Y để tạo hình dáng đặc biệt
    

## Tạo Materials để tô màu

**Material cho nền**:

- Right-click trong Assets → Create → Material → đặt tên "Dark"
    
- Chọn màu tối trong Base Map
    
- Kéo thả lên Ground
    
- Giảm Smoothness xuống 0 để tạo bề mặt mờ (matte)
    

**Material cho nhân vật**:

- Tạo material mới tên "Green"
    
- Click vào color picker → nhập mã Hexadecimal ở dưới cùng để có màu chính xác
    
- Kéo thả lên Dodgy
    

## Tổ chức thư mục

Tạo cấu trúc thư mục trong Assets:

- Folder "Materials": chứa các material đã tạo
    
- Folder "Scripts": chứa các script code
    

## Tạo và gắn Script

**Tạo script Mover**:

- Trong folder Scripts: Right-click → Create → MonoBehaviour Script
    
- **Quan trọng**: Đổi tên thành "Mover" ngay lập tức trước khi click chuột ra chỗ khác (tránh bị lưu tên mặc định)
    

**Gắn script vào game object** (3 cách):

1. Kéo thả script từ Assets lên game object trong Hierarchy
    
2. Click vào game object → kéo script vào vùng trống ở Inspector
    
3. Click Add Component → tìm "Mover" → chọn
    

## Hiểu về Transform và Translate

**Transform component**:

- Là component chứa thông tin Position, Rotation, Scale của game object
    
- Mỗi game object đều có Transform
    

**Phương thức Translate**:

csharp

`transform.Translate(1, 0, 0);`

- `transform`: tham chiếu đến Transform component
    
- Toán tử `.` (dot operator): truy cập các phương thức và thuộc tính
    
- `Translate()`: phương thức di chuyển đối tượng
    
- Ba tham số: X, Y, Z (hoặc Z) - chỉ hướng và khoảng cách di chuyển
    

## Start vs Update

**Start method**:

- Được gọi một lần duy nhất khi game object được kích hoạt
    
- Chạy ngay khi nhấn Play
    
- Dùng để khởi tạo ban đầu
    

**Ví dụ**: Đặt code trong Start

csharp

`void Start() {     transform.Translate(1f, 0f, 0f); }`

→ Nhân vật di chuyển 1 đơn vị sang phải một lần khi game bắt đầu

**Update method**:

- Được gọi mỗi frame (khung hình)
    
- Với 60 FPS (frames per second), sẽ chạy 60 lần/giây
    
- Dùng cho các hành động liên tục
    

**Ví dụ**: Đặt code trong Update

csharp

`void Update() {     transform.Translate(0.01f, 0f, 0f); }`

→ Nhân vật di chuyển liên tục mỗi frame

## Float và Double

**Vấn đề với số thập phân**:

csharp

`transform.Translate(0.01, 0, 0); // Lỗi: không thể convert từ double sang float`

**Giải pháp**: Thêm hậu tố `f` để chỉ định kiểu float

csharp

`transform.Translate(0.01f, 0f, 0f); // Đúng`

- Float: số thập phân với độ chính xác vừa phải, thường dùng trong Unity
    
- Double: số thập phân với độ chính xác cao hơn, ít dùng trong game development
    

## Điều chỉnh Camera

- Chọn Main Camera trong Hierarchy
    
- Nhấn F để focus
    
- Di chuyển và xoay camera để đóng khung nhân vật trong Game window
    
- Dùng công cụ Move và Rotate để điều chỉnh góc nhìn phù hợp
    

## Lưu ý quan trọng

- **Luôn nhớ Save script** (Ctrl+S) trước khi test trong Unity
    
- Các thay đổi trong Play Mode sẽ **không được lưu** khi thoát Play Mode
    
- Giá trị di chuyển 0.01f mỗi frame tạo chuyển động mượt mà, còn 1f quá nhanh