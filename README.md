# Criticore
Github để develop criticore
## ⚙️ Kiến trúc
Dự án được triển khai theo mô hình **Microservices**, bao gồm:

src/
├── Services/
│ ├── Identity/ # Quản lý xác thực & phân quyền (login, register, JWT, roles)
│ │ ├── Identity.API
│ │ ├── Identity.Application
│ │ └── Identity.Infrastructure
│ │
│ ├── Teacher/ # Quản lý lớp học, nhóm, thảo luận (cho Teacher)
│ │ ├── Teacher.API
│ │ ├── Teacher.Application
│ │ └── Teacher.Infrastructure
│ │
│ ├── Student/ # Quản lý lớp học, thanh toán, thảo luận (cho Student)
│ │ ├── Student.API
│ │ ├── Student.Application
│ │ └── Student.Infrastructure
│ │
│ └── Admin/ # Quản trị hệ thống, thống kê doanh thu
│ ├── Admin.API
│ ├── Admin.Application
│ └── Admin.Infrastructure
│
├── API.Gateway/ # Cổng giao tiếp duy nhất cho Frontend gọi đến các service
│
├── BuildingBlocks/ # Các thư viện tái sử dụng (SharedKernel, EventBus, Common)
│
└── WebClient.React/ # Frontend (Razor Pages) kết nối qua API Gateway
