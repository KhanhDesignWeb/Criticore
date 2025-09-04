# Criticore
Github để develop criticore
# Kiến trúc

Dự án được triển khai theo mô hình Microservices, bao gồm:

- **Services:**
  - `CourseService/`
    - `# Quản lý thông tin khóa học`
    - `Course.API/`
    - `Course.Application/`
    - `Course.Domain/`
    - `Course.Infrastructure/`
  - `IdentityService/`
    - `# Quản lý xác thực & phân quyền (login, register, JWT, roles)`
    - `Identity.API/`
    - `Identity.Application/`
    - `Identity.Infrastructure/`
    - `Identity.Domain/`
  - `PaymentService/`
    - `# Quản lý thanh toán`
    - `Payment.API/`
    - `Payment.Application/`
    - `Payment.Infrastructure/`
    - `Payment.Domain/`

- **API Gateways:**
  - `OcelotApiGateway/`
    - `# Cổng giao tiếp duy nhất cho Frontend gọi đến các service`
    - `Controllers/`
    - `appsettings.json`
    - `ocelot.json`
    - `OcelotApiGateway.http`
    - `Program.cs`

- **BuildingBlocks:**
  - `EventBus/`
    - `# Cung cấp cơ chế truyền thông giữa các service (SharedKernel, EventBus, Common)`
  - `Shared/`
    - `# Các thành phần chung được chia sẻ (SharedKernel, EventBus, Common)`

- **WebApps:**
  - `Front-end/`
    - `# Giao diện người dùng, tích hợp với API Gateway`
    - `wwwroot/`
    - `Pages/`
    - `appsettings.json`
    - `Program.cs`
