## Biến (Variables) trong C#

Bài học giới thiệu khái niệm biến, các kiểu dữ liệu cơ bản trong C#, và cách sử dụng biến để tạo code linh hoạt hơn.

## Khái niệm biến

Biến như một cái hộp dùng để lưu trữ, thao tác và tham chiếu thông tin. Mỗi biến có ba thành phần:

- **Tên biến**: Cách gọi để tham chiếu đến giá trị bên trong
    
- **Dữ liệu**: Giá trị hiện tại lưu trong biến (có thể thay đổi)
    
- **Kiểu dữ liệu**: Xác định loại thông tin mà biến chứa
    

**Ví dụ**: Biến `hitpoints` (điểm máu) chứa giá trị 20. Giá trị này có thể tăng khi nhặt thuốc hoặc giảm khi bị tấn công.

## Các kiểu dữ liệu cơ bản

**Integer (int)** - Số nguyên

csharp

`int hitpoints = 20; int score = 0;`

- Dùng cho những giá trị là số toàn bộ (không có phần thập phân)
    

**Float** - Số thập phân

csharp

`float speed = 0.01f; float damageMultiplier = 1.5f;`

- Dùng cho những giá trị có phần thập phân
    
- **Quan trọng**: Phải thêm hậu tố `f` ở cuối để chỉ định kiểu float
    

**Boolean (bool)** - Giá trị True/False

csharp

`bool isAlive = true; bool isActive = false;`

- Chỉ có hai giá trị: `true` hoặc `false`
    
- Thường đặt tên bắt đầu bằng "is" (isAlive, isEnemy, isActive)
    
- Dùng trong các câu lệnh điều kiện
    

**String** - Chuỗi ký tự

csharp

`string playerName = "Rick"; string gameName = "Obstacle Dodge";`

- Chứa chữ cái, số, và ký tự đặc biệt
    
- Phải bao quanh bằng dấu ngoặc kép `" "`
    

## Quy ước đặt tên biến

- Ký tự đầu tiên viết thường (lowercase)
    
- Ký tự đầu của các từ tiếp theo viết hoa (camelCase)
    
- **Ví dụ**: `xValue`, `playerHealth`, `isMoving`, `characterName`
    

## Tạo biến trong script Mover

**Vị trí khai báo biến**:

- Đặt biến ở phía trên, ngoài phương thức Start và Update
    
- Giúp dễ quản lý tất cả biến ở một vị trí
    

**Ví dụ - Tạo biến để thay thế giá trị hardcoded**:

csharp

`float xValue = 0.01f; void Update() {     transform.Translate(xValue, 0f, 0f); }`

**Lợi ích khi sử dụng biến**:

- **Dễ quản lý**: Tất cả biến được nhóm ở trên cùng, dễ tìm kiếm
    
- **Tiết kiệm thời gian**: Chỉ cần thay đổi một chỗ thay vì phải sửa nhiều nơi
    
- **Linh hoạt**: Có thể thay đổi giá trị dễ dàng mà không cần chỉnh sửa logic code
    
- **Giảm lỗi**: Tránh nhầm lẫn khi phải sửa nhiều giá trị giống nhau ở những chỗ khác nhau
    

## Thực hành: Tạo các biến X, Y, Z

**Khai báo ba biến**:

csharp

`float xValue = 0f; float yValue = 0.05f; float zValue = 0f; void Update() {     transform.Translate(xValue, yValue, zValue); }`

**Quan trọng về thứ tự**: Tham số luôn theo thứ tự **X, Y, Z** - không thay đổi thứ tự này.

## Các trục chuyển động (Axes)

Khi xem trong Unity Scene:

- **Trục X (màu đỏ)**: Di chuyển sang trái/phải
    
- **Trục Y (màu xanh lá)**: Di chuyển lên/xuống
    
- **Trục Z (màu xanh dương)**: Di chuyển về phía trước/sau
    

## Ví dụ hoàn thiện: Nhân vật bay thẳng lên trên

csharp

`float xValue = 0f; float yValue = 0.05f; float zValue = 0f; void Update() {     transform.Translate(xValue, yValue, zValue); }`

- `xValue = 0f`: Không di chuyển ngang
    
- `yValue = 0.05f`: Di chuyển lên với tốc độ 0.05 đơn vị mỗi frame
    
- `zValue = 0f`: Không di chuyển về phía trước/sau
    

Kết quả: Nhân vật sẽ bay thẳng lên không gian.

## Lưu ý khi sử dụng biến

- Luôn nhớ lưu script trước khi bấm Play
    
- Giá trị của biến có thể thay đổi trong Inspector để test nhanh
    
- Sử dụng tên biến rõ ràng, dễ hiểu để code dễ bảo trì