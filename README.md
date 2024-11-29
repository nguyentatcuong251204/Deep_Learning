sequenceDiagram
    participant Khách hàng
    participant Quản lý dự án
    participant Cơ sở dữ liệu
    participant Thông báo
    participant Nhân viên
    
    Khách hàng->>Quản lý dự án: Tạo công việc
    Quản lý dự án->>Cơ sở dữ liệu: Tạo bản ghi công việc
    Cơ sở dữ liệu->>Quản lý dự án: Lưu vào cơ sở dữ liệu
    Quản lý dự án->>Quản lý dự án: Phân công nhiệm vụ 
    Quản lý dự án->>Thông báo: Gửi thông báo
    Thông báo->>Nhân viên: Nhân viên nhận thông báo
    Thông báo->>Khách hàng: Khách hàng nhận thông báo

