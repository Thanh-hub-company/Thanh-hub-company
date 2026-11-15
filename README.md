<div align="center">

# 👨‍💻 LÊ TUẤN THÀNH

**Java Backend Developer**  
*Học Java Backend | Spring Boot | PostgreSQL | Microservices | DevOps*

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-Thanh--hub--company-24292F?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Thanh-hub-company)
&nbsp;
[![Email](https://img.shields.io/badge/Email-24003852%40caut.edu.vn-64748B?style=for-the-badge&logo=gmail&logoColor=white)](mailto:24003852@caut.edu.vn)

<br/><br/>

<!-- CÁC ICON KỸ NĂNG CĂN GIỮA ĐỒNG BỘ -->
![Java](https://img.shields.io/badge/Java-E76F00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-333333?style=flat-square&logo=linux&logoColor=FCC624)

<br/>

`#java` `#spring-boot` `#postgresql` `#jdbc` `#microservices` `#docker` `#kubernetes` `#ci-cd` `#rest-api` `#devops`

</div>

---

### 📊 Tỷ Lệ Ngôn Ngữ (Languages Breakdown)

| Ngôn ngữ | Tỷ lệ | Phân bổ trực quan |
| :--- | :---: | :--- |
| **Java**       | 62% | `██████████████████████████████                   ` |
| **SQL**        | 14% | `███████                                           ` |
| **YAML**       | 12% | `██████                                           ` |
| **Dockerfile** | 7% | `███                                         ` |
| **Shell**      | 5% | `██                                               ` |

---

### 🎯 Lộ Trình Học Tập (Learning Roadmap)

- [x] **1. JDBC Foundation (100%)** — *CRUD thuần, Connection pool HikariCP, quản lý Transaction*
- [x] **2. Spring REST API (85%)** — *Spring Data JPA, Bean Validation, DTO Pattern, tài liệu OpenAPI*
- [ ] **3. Microservices (65%)** — *Eureka Discovery, Spring Cloud Gateway, Docker Compose đa dịch vụ*
- [ ] **4. DevOps & Cloud (50%)** — *CI/CD GitHub Actions, Dockerfile tối ưu, K8s Manifests, Helm*

---

### 📂 Danh Sách Repositories Tiêu Biểu

| Repository | Mô tả tóm tắt | Công nghệ |
| :--- | :--- | :--- |
| 📦 [**microservices-ecommerce**](#-dự-án-tiêu-biểu-microservices-ecommerce) | Hệ thống phân tán gồm user, order, product, gateway, eureka | `Java` `YAML` |
| 📦 [**spring-boot-rest-api**](https://github.com/Thanh-hub-company) | REST API quản lý sản phẩm, JPA, Validation, Swagger | `Java` |
| 📦 [**jdbc-postgres-playground**](https://github.com/Thanh-hub-company) | CRUD thuần JDBC, quản lý connection pool HikariCP | `Java` `SQL` |
| 📦 [**devops-ci-cd-pipeline**](https://github.com/Thanh-hub-company) | GitHub Actions tự động build, test và deploy lên VPS | `YAML` `Docker` `Shell` |
| 📦 [**k8s-microservices-deploy**](https://github.com/Thanh-hub-company) | Kubernetes manifests, Ingress Controller và Helm chart | `YAML` |
| 📦 [**postgres-sql-practice**](https://github.com/Thanh-hub-company) | Bài tập query, đánh index, transaction, EXPLAIN ANALYZE | `SQL` |

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
├── docker-compose.yml             # Khởi chạy toàn bộ hệ sinh thái & PostgreSQL
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

#### 3. Hướng dẫn khởi chạy nhanh

```bash
# 1. Đóng gói mã nguồn
./mvnw clean package -DskipTests

# 2. Khởi chạy toàn bộ cụm dịch vụ qua Docker Compose
docker compose up -d --build

# 3. Kiểm tra trạng thái các container
docker compose ps
```

#### 4. Danh sách API Endpoints chính qua Gateway (:8080)

| Method | Endpoint | Service phụ trách | Quyền |
| :--- | :--- | :--- | :---: |
| `POST` | `/api/v1/auth/login` | `user-service` | Public |
| `GET` | `/api/v1/products` | `product-service` | Public |
| `POST` | `/api/v1/products` | `product-service` | Admin |
| `POST` | `/api/v1/orders` | `order-service` | User |
| `GET` | `/api/v1/orders/{id}` | `order-service` | User |

#### 5. Trạng thái GitHub Actions gần đây

| Workflow Run | Trạng thái | Nhánh | Ghi chú |
| :--- | :---: | :---: | :--- |
| `CI/CD - Build & Push Images` | ✅ Success | `main` | Đã build và push image lên registry |
| `Unit & Integration Test Suite` | ✅ Success | `main` | 42 tests passed, 0 failures |
| `Nightly Vulnerability Scan` | ❌ Failed | `develop` | Lỗi timeout tải cơ sở dữ liệu CVE |
| `Deploy Staging to VPS` | ✅ Success | `main` | Tự động triển khai hoàn tất |

---

### ✦ Nhật Ký Hoạt Động (Recent Activity)

- 🚀 **Released** `v1.1.0` of `microservices-ecommerce`
- 🔀 **Opened PR #12**: `Add Dockerfile and docker-compose for product-service`
- 📦 **Pushed 3 commits** to `order-service`: `feat: add order status workflow`
- ⭐ **Starred** `spring-projects/spring-boot`

---

<div align="center">
  <sub>© 2026 Lê Tuấn Thành • Học tập & Xây dựng hệ thống Java Backend hiệu năng cao</sub>
</div>
