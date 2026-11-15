# 👨‍💻 LÊ TUẤN THÀNH
> **Java Backend Developer**  
> Học Java Backend | Spring Boot | PostgreSQL | Microservices | DevOps
[![LinkedIn](https://img.shields.io/badge/LinkedIn-4F46E5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_LINKEDIN)
[![Gmail](https://img.shields.io/badge/Gmail-64748B?style=flat-square&logo=gmail&logoColor=white)](mailto:your_email@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-24292F?style=flat-square&logo=github&logoColor=white)](https://github.com/YOUR_USERNAME)
---
### ✦ Kỹ Năng & Chủ Đề (Skills & Topics)
`#java` `#spring-boot` `#postgresql` `#jdbc` `#microservices` `#docker` `#kubernetes` `#ci-cd` `#rest-api` `#devops`
![Java](https://img.shields.io/badge/Java-E76F00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-333333?style=flat-square&logo=linux&logoColor=FCC624)
---
### ✦ Tỷ Lệ Ngôn Ngữ (Languages Breakdown)
```text
Java         62%  ███████████████████████████████░░░░░░░░░░░░░░░░░░░░
SQL          14%  ███████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
YAML         12%  ██████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
Dockerfile    7%  ███░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
Shell         5%  ██░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
```
---
### ✦ Lộ Trình Học Tập (Learning Roadmap)
```text
[1] JDBC Foundation      [████████████████████] 100%  • Connection pool HikariCP, CRUD thuần, Transaction
[2] Spring REST API      [█████████████████░░░]  85%  • Spring Data JPA, Validation, DTO, OpenAPI
[3] Microservices        [█████████████░░░░░░░]  65%  • Eureka Discovery, Spring Cloud Gateway, Docker Compose
[4] DevOps & Cloud       [██████████░░░░░░░░░░]  50%  • CI/CD Workflows, Dockerfile, K8s Manifests, Helm
```
---
### ✦ Danh Sách Repositories (Pinned Repositories)
| Repository | Mô tả tóm tắt | Ngôn ngữ / Công nghệ |
| :--- | :--- | :--- |
| 📦 [**microservices-ecommerce**](#-dự-án-tiêu-biểu-microservices-ecommerce) | Hệ thống bán hàng gồm user, order, product, gateway, eureka | `Java` `YAML` |
| 📦 [**spring-boot-rest-api**](https://github.com/YOUR_USERNAME) | REST API quản lý sản phẩm, JPA, Validation, Swagger | `Java` |
| 📦 [**jdbc-postgres-playground**](https://github.com/YOUR_USERNAME) | CRUD thuần JDBC, quản lý connection pool HikariCP | `Java` `SQL` |
| 📦 [**devops-ci-cd-pipeline**](https://github.com/YOUR_USERNAME) | GitHub Actions tự động build, test và deploy lên VPS | `YAML` `Dockerfile` `Shell` |
| 📦 [**k8s-microservices-deploy**](https://github.com/YOUR_USERNAME) | Kubernetes manifests, Ingress Controller và Helm chart | `YAML` |
| 📦 [**postgres-sql-practice**](https://github.com/YOUR_USERNAME) | Bài tập query, đánh index, transaction, EXPLAIN ANALYZE | `SQL` |
---
### 🌟 Dự Án Tiêu Biểu: `microservices-ecommerce`
![Build](https://img.shields.io/badge/Build-Passing-2ea44f?style=flat-square)
![Tests](https://img.shields.io/badge/Tests-Passing-2ea44f?style=flat-square)
![Docker](https://img.shields.io/badge/Docker_Push-Passing-2ea44f?style=flat-square)
![Release](https://img.shields.io/badge/Release-v1.1.0-blue?style=flat-square)
#### 1. Cấu trúc thư mục (File Tree)
```text
microservices-ecommerce/
├── api-gateway/                   # Spring Cloud Gateway (Port 8080)
├── user-service/                  # Quản lý người dùng & JWT Auth (Port 8081)
├── product-service/               # Danh mục sản phẩm & tồn kho (Port 8082)
├── order-service/                 # Xử lý đơn hàng & checkout (Port 8083)
├── .github/workflows/ci.yml       # CI pipeline: test, build, push Docker
├── docker-compose.yml             # Khởi chạy toàn bộ hệ thống & PostgreSQL
├── pom.xml                        # Maven Parent POM
└── README.md
```
#### 2. Sơ đồ kiến trúc (Architecture)
```text
                       [ Client Request ]
                               │
                               ▼
                    ┌─────────────────────┐
                    │ API Gateway (:8080) │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             ▼                 ▼                 ▼
     ┌──────────────┐  ┌──────────────┐  ┌──────────────┐
     │ User Service │  │Product Serv. │  │ Order Service│
     │   (:8081)    │  │   (:8082)    │  │   (:8083)    │
     └──────┬───────┘  └──────┬───────┘  └──────┬───────┘
            │                 │                 │
            ▼                 ▼                 ▼
     [ PostgreSQL ]    [ PostgreSQL ]    [ PostgreSQL ]
```
#### 3. Bảng công nghệ sử dụng
| Thành phần | Công nghệ | Chi tiết |
| :--- | :--- | :--- |
| **Ngôn ngữ** | Java | 17 LTS |
| **Frameworks** | Spring Boot, Spring Data JPA | 3.2.x |
| **Routing / Mesh** | Spring Cloud Gateway, Eureka | 2023.x |
| **Cơ sở dữ liệu** | PostgreSQL | 15 Alpine |
| **Vận hành & CI** | Docker, Docker Compose, GitHub Actions | - |
#### 4. Hướng dẫn khởi chạy nhanh
```bash
# 1. Đóng gói mã nguồn
./mvnw clean package -DskipTests
# 2. Khởi chạy toàn bộ cụm dịch vụ qua Docker Compose
docker compose up -d --build
# 3. Kiểm tra trạng thái container
docker compose ps
```
#### 5. Code mẫu & Cấu hình
**Cấu hình Gateway (`api-gateway/src/main/resources/application.yml`):**
```yaml
server:
  port: 8080
spring:
  application:
    name: api-gateway
  cloud:
    gateway:
      routes:
        - id: product-service
          uri: lb://product-service
          predicates:
            - Path=/api/v1/products/**
        - id: order-service
          uri: lb://order-service
          predicates:
            - Path=/api/v1/orders/**
```
**Nghiệp vụ đặt hàng (`order-service/.../OrderService.java`):**
```java
@Service
@RequiredArgsConstructor
public class OrderService {
    private final OrderRepository orderRepository;
    @Transactional
    public OrderResponse placeOrder(OrderRequest request) {
        Order order = Order.builder()
                .userId(request.getUserId())
                .productId(request.getProductId())
                .quantity(request.getQuantity())
                .status(OrderStatus.PENDING)
                .createdAt(Instant.now())
                .build();
        Order savedOrder = orderRepository.save(order);
        return OrderResponse.fromEntity(savedOrder);
    }
}
```
#### 6. Danh sách API Endpoints qua Gateway (:8080)
| Method | Endpoint | Service | Mô tả | Quyền |
| :--- | :--- | :--- | :--- | :---: |
| `POST` | `/api/v1/auth/login` | `user-service` | Đăng nhập & cấp phát JWT | Public |
| `GET` | `/api/v1/products` | `product-service` | Lấy danh sách sản phẩm | Public |
| `POST` | `/api/v1/products` | `product-service` | Thêm sản phẩm mới | Admin |
| `PUT` | `/api/v1/products/{id}` | `product-service` | Cập nhật thông tin sản phẩm | Admin |
| `POST` | `/api/v1/orders` | `order-service` | Khởi tạo đơn hàng mới | User |
| `GET` | `/api/v1/orders/{id}` | `order-service` | Xem chi tiết đơn hàng | User |
| `DELETE`| `/api/v1/orders/{id}` | `order-service` | Hủy đơn hàng | Admin/User |
#### 7. Trạng thái GitHub Actions gần đây
| Workflow Run | Trạng thái | Nhánh | Ghi chú |
| :--- | :---: | :---: | :--- |
| `CI/CD - Build & Push Images` | ✅ Success | `main` | Đã build và push image lên registry |
| `Unit & Integration Test Suite` | ✅ Success | `main` | 42 tests passed, 0 failures |
| `Nightly Vulnerability Scan` | ❌ Failed | `develop` | Lỗi timeout tải cơ sở dữ liệu CVE |
| `Deploy Staging to VPS` | ✅ Success | `main` | Tự động triển khai hoàn tất |
#### 8. Lịch sử phát hành (Releases)
- **v1.1.0** *(2026-11-14)*: Hoàn thiện luồng kiểm tra tồn kho giữa `order-service` & `product-service`; tích hợp `docker-compose.yml`.
- **v1.0.0** *(2026-10-28)*: Khởi tạo kiến trúc monorepo gồm `api-gateway`, `user-service` và `product-service`.
---
### ✦ Nhật Ký Hoạt Động (Recent Activity)
- 🚀 **Released** `v1.1.0` of `microservices-ecommerce`
- 🔀 **Opened PR #12**: `Add Dockerfile and docker-compose for product-service`
- 📦 **Pushed 3 commits** to `order-service`: `feat: add order status workflow`
- ⭐ **Starred** `spring-projects/spring-boot`
---
*© 2026 Lê Tuấn Thành • Xây dựng hệ thống ổn định và tối ưu hiệu năng*
