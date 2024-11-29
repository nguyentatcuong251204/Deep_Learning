sequenceDiagram
    participant KhachHang as Khách Hàng
    participant QuảnLýTácVụ as Quản Lý Dự Án
    participant CSDL as Cơ Sở Dữ Liệu
    participant ThôngBáo as Thông Báo
    participant NhânViên as Nhân Viên
    
    KhachHang->>QuảnLýTácVụ: Tạo tác vụ
    QuảnLýTácVụ->>CSDL: Tạo bản ghi tác vụ
    CSDL->>QuảnLýTácVụ: Lưu vào cơ sở dữ liệu
    QuảnLýTácVụ->>QuảnLýTácVụ: Phân công tác vụ cho nhân viên
    QuảnLýTácVụ->>ThôngBáo: Gửi thông báo
    ThôngBáo->>NhânViên: Tác vụ được giao
    ThôngBáo->>KhachHang: Tác vụ đã được giao

sequenceDiagram
    participant NgườiDùng as Người Dùng
    participant ỨngDụng as Ứng Dụng
    participant MáyChủ as Máy Chủ
    participant CSDL as Cơ Sở Dữ Liệu
    
    NgườiDùng->>ỨngDụng: Nhập tên đăng nhập và mật khẩu
    ỨngDụng->>MáyChủ: Gửi yêu cầu đăng nhập (username, password)
    MáyChủ->>CSDL: Kiểm tra thông tin tài khoản
    CSDL-->>MáyChủ: Kết quả xác thực (Hợp lệ/Không hợp lệ)
    MáyChủ-->>ỨngDụng: Phản hồi đăng nhập (Thành công/Thất bại)
    ỨngDụng-->>NgườiDùng: Hiển thị kết quả đăng nhập

