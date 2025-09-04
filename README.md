# Criticore
Github để develop criticore
# Kiến trúc

Dự án được triển khai theo mô hình Microservices, bao gồm:

- **Services:**
  - `src/`
    - `Services/`
      - `identity/`
        - `# Quản lý xác thực & phân quyền (login, register, JWT, roles)`
        - `identity.API/`
        - `Identity.Application/`
        - `Identity.Infrastructure/`
      - `Teacher/`
        - `# Quản lý thông tin giáo viên (cho Teacher)`
        - `Teacher.API/`
        - `Teacher.Application/`
        - `Teacher.Infrastructure/`
      - `Student/`
        - `# Quản lý thông tin học sinh (cho Student)`
        - `Student.API/`
        - `Student.Application/`
        - `Student.Infrastructure/`
      - `Admin/`
        - `# Quản lý thông tin, thống kê quản trị viên`
        - `Admin.API/`
        - `Admin.Application/`
        - `Admin.Infrastructure/`

- **API Gateway:**
  - `# Công giải tiếp nhận và định tuyến (SharedKernel, EventBus, Common)`

- **WebClient:**
  - `# Frontend (React / Razor Pages) không qua API Gateway`
