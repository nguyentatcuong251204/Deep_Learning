```mermaid
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


