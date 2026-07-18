<!--
  HƯỚNG DẪN: Đặt file này (tên: README.md) trong repo có tên trùng với
  username GitHub, tức repo HaHiepThanh/HaHiepThanh, đặt visibility là Public.
  GitHub sẽ tự hiển thị nội dung này trên trang profile.
-->

<h1 align="center">Hà Hiệp Thanh</h1>

<p align="center">
  <b>Aspiring DevOps Engineer</b> · Sinh viên năm 3
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/hahiepthanh/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="https://www.facebook.com/hahiepthanhhhtt/">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=flat&logo=facebook&logoColor=white" alt="Facebook"/>
  </a>
  <a href="mailto:hahiepthanhhhtt@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white" alt="Email"/>
  </a>
</p>

---

## Giới thiệu

Tôi là sinh viên năm 3, đang theo đuổi định hướng trở thành **DevOps Engineer**. Tôi có nền tảng phát triển ứng dụng với nhiều framework backend và frontend, đồng thời đang tập trung xây dựng năng lực về hạ tầng, container hóa và điện toán đám mây.

- Định hướng nghề nghiệp: **DevOps / Platform Engineering**
- Đang tìm hiểu sâu về: **Kubernetes, Proxmox, Google Cloud Platform**
- Quan tâm đến: kiến trúc microservice, tự động hóa triển khai (CI/CD), và tối ưu hạ tầng

---

## Công nghệ sử dụng

**Frameworks**

![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Micronaut](https://img.shields.io/badge/Micronaut-000000?style=for-the-badge&logo=micronaut&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![Gin](https://img.shields.io/badge/Gin-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)

**Communication & Messaging**

![gRPC](https://img.shields.io/badge/gRPC-244C5A?style=for-the-badge&logo=grpc&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API-02569B?style=for-the-badge&logo=fastapi&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=for-the-badge&logo=socketdotio&logoColor=white)

**Databases**

![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)

**DevOps & Tools**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)
![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![NGINX](https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)

---

## Dự án tiêu biểu

### Resona – Nền tảng nghe nhạc trực tuyến

Ứng dụng streaming nhạc full-stack, tách thành 2 repo: [**resona**](https://github.com/HaHiepThanh/resona) (Angular frontend) và [**resona_core**](https://github.com/HaHiepThanh/resona_core) (NestJS backend).

**Frontend — Angular 19**
- Quản lý state tập trung bằng **NgRx** (Store + Effects) cho 11 domain: track, playlist, queue, play, history, favorite, comment, search, category, profile, auth
- UI dựng trên **Angular Material + CDK**: player bar, hàng chờ phát (queue) kéo-thả, lời bài hát đồng bộ, bình luận, dialog đăng nhập
- Xác thực người dùng qua **Firebase Authentication** (`@angular/fire`), pipe tùy biến để chuyển đổi ảnh, thời lượng và định dạng lyrics

**Backend — NestJS 11 (TypeScript)**
- Kiến trúc **domain-driven**: 11 module độc lập (track, playlist, playlist_tracks, category, comment, queue, history, notification, profile, auth, supabase), mỗi module đủ controller / service / entity / DTO
- **Upload file theo chunk**: client cắt file nhạc thành nhiều phần, server nhận từng chunk rồi ghép lại bằng Node.js stream — cho phép tải lên file lớn mà không nghẽn bộ nhớ
- **Xử lý audio bằng FFmpeg**: tự động chuyển mã sang AAC/M4A, remux ADTS → ASC, đặt cờ `+faststart` để trình duyệt đọc được metadata ngay khi bắt đầu tải; đọc thời lượng chính xác qua `ffprobe` và bóc metadata bằng `music-metadata`
- **Supabase** làm nơi lưu trữ file (Storage) và cơ sở dữ liệu **PostgreSQL**, truy cập qua **TypeORM** với quan hệ đầy đủ (ManyToOne / OneToMany / ManyToMany, cascade delete)
- Bảo mật bằng **Firebase Admin SDK** middleware xác thực ID token, validation bằng `class-validator` + `ValidationPipe` toàn cục
- Đóng gói **Docker** (image `node:20-bullseye` có cài sẵn FFmpeg)

<p>
  <img src="https://img.shields.io/badge/Angular_19-DD0031?style=flat-square&logo=angular&logoColor=white"/>
  <img src="https://img.shields.io/badge/NgRx-BA2BD2?style=flat-square&logo=reduxsaga&logoColor=white"/>
  <img src="https://img.shields.io/badge/Angular_Material-757575?style=flat-square&logo=materialdesign&logoColor=white"/>
  <img src="https://img.shields.io/badge/RxJS-B7178C?style=flat-square&logo=reactivex&logoColor=white"/>
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeORM-FE0803?style=flat-square&logo=typeorm&logoColor=white"/>
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Firebase_Auth-FFCA28?style=flat-square&logo=firebase&logoColor=black"/>
  <img src="https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
</p>

### [Microservices – Employee Management](https://github.com/HaHiepThanh/Microservices-EmployeeManagement)

Hệ thống quản lý nhân sự theo kiến trúc **microservice** với 5 service độc lập (auth, employee, department, attendance, payroll), áp dụng mô hình **database-per-service** — mỗi service sở hữu một instance MySQL riêng.

- **Giao tiếp đồng bộ:** REST (`RestClient`) cho luồng employee → department, và **gRPC / Protocol Buffers** cho các lời gọi hiệu năng cao employee → payroll & attendance
- **Giao tiếp bất đồng bộ:** **RabbitMQ (Spring AMQP)** cho kiến trúc event-driven — auth và employee publish event, consumer xử lý độc lập
- **Bảo mật:** Spring Security stateless với **JWT**, OAuth2 Resource Server, phân quyền **RBAC** (ADMIN / HR / EMPLOYEE)
- **Triển khai:** Docker multi-stage build, Docker Compose với `healthcheck` + `depends_on: service_healthy`, image publish lên Docker Hub
- **Design patterns:** Adapter (chống coupling với external DTO), Builder, Singleton — có tài liệu chỉ rõ vị trí áp dụng

<p>
  <img src="https://img.shields.io/badge/Java_21-007396?style=flat-square&logo=openjdk&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/>
  <img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white"/>
  <img src="https://img.shields.io/badge/gRPC-244C5A?style=flat-square&logo=grpc&logoColor=white"/>
  <img src="https://img.shields.io/badge/Protobuf-EA4335?style=flat-square&logo=googledocs&logoColor=white"/>
  <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white"/>
  <img src="https://img.shields.io/badge/Hibernate_JPA-59666C?style=flat-square&logo=hibernate&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL_8-4479A1?style=flat-square&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/MapStruct-E10098?style=flat-square&logo=databricks&logoColor=white"/>
  <img src="https://img.shields.io/badge/Lombok-BC4521?style=flat-square&logo=lombok&logoColor=white"/>
  <img src="https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker_Compose-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white"/>
</p>

### [SA Seminar – E-Commerce Microservice](https://github.com/HaHiepThanh/sa-seminar-microservice)

Nền tảng thương mại điện tử microservice xây dựng trên **Micronaut**, gồm 6 service: catalog, inventory, user, cart, order-payment và mail. Trọng tâm là tính năng **group-buy (mua chung) real-time**.

- **Real-time:** **WebSocket** và **Server-Sent Events (SSE)** đẩy trạng thái group-buy về client; Nginx được cấu hình riêng (`proxy_buffering off`, HTTP/1.1) để stream không bị buffer
- **API Gateway:** **Nginx** reverse proxy định tuyến toàn bộ traffic theo path tới từng service, đồng thời serve static frontend
- **Giao tiếp giữa service:** **gRPC** (catalog/order ↔ inventory) kết hợp **RabbitMQ** cho event bất đồng bộ (đặt hàng → trừ tồn kho → gửi mail xác nhận)
- **Data layer:** Micronaut Data (Hibernate JPA & JDBC), **Flyway migration**, HikariCP connection pool, MySQL 8
- **Bảo mật:** Micronaut Security **JWT** + băm mật khẩu **BCrypt**
- **Khác:** lập trình phản ứng với **Project Reactor**, tài liệu API tự sinh bằng **OpenAPI / Swagger**, mail service dùng Jakarta Mail, test với **JUnit 5**

<p>
  <img src="https://img.shields.io/badge/Micronaut-000000?style=flat-square&logo=micronaut&logoColor=white"/>
  <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white"/>
  <img src="https://img.shields.io/badge/Netty-005571?style=flat-square&logo=apachetomcat&logoColor=white"/>
  <img src="https://img.shields.io/badge/gRPC-244C5A?style=flat-square&logo=grpc&logoColor=white"/>
  <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white"/>
  <img src="https://img.shields.io/badge/WebSocket-010101?style=flat-square&logo=socketdotio&logoColor=white"/>
  <img src="https://img.shields.io/badge/SSE-FFB13B?style=flat-square&logo=serverfault&logoColor=white"/>
  <img src="https://img.shields.io/badge/NGINX-009639?style=flat-square&logo=nginx&logoColor=white"/>
  <img src="https://img.shields.io/badge/Project_Reactor-6DB33F?style=flat-square&logo=reactivex&logoColor=white"/>
  <img src="https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white"/>
  <img src="https://img.shields.io/badge/Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL_8-4479A1?style=flat-square&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenAPI-6BA539?style=flat-square&logo=openapiinitiative&logoColor=white"/>
  <img src="https://img.shields.io/badge/JUnit_5-25A162?style=flat-square&logo=junit5&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker_Compose-2496ED?style=flat-square&logo=docker&logoColor=white"/>
</p>

---

## Thống kê GitHub

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=HaHiepThanh&theme=github" alt="Profile Details"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=HaHiepThanh&theme=default&hide_border=true" alt="GitHub Streak" height="180"/>
</p>

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=HaHiepThanh&theme=github" alt="Repos per Language" height="200"/>
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=HaHiepThanh&theme=github" alt="Most Commit Language" height="200"/>
</p>

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=HaHiepThanh&theme=github" alt="Stats" height="200"/>
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=HaHiepThanh&theme=github&utcOffset=7" alt="Productive Time" height="200"/>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=HaHiepThanh&theme=github-compact&hide_border=true" alt="Activity Graph"/>
</p>

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=HaHiepThanh&style=flat&color=blue" alt="Profile views"/>
</p>
