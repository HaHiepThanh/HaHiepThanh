<!--
  SETUP: Place this file (named README.md) in a repository whose name matches
  your GitHub username — i.e. HaHiepThanh/HaHiepThanh — and set it to Public.
  GitHub will automatically render it on your profile page.
-->

<h1 align="center">Ha Hiep Thanh</h1>

<p align="center">
  <b>Aspiring DevOps Engineer</b> · Fourth-year Software Engineering student
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

## About Me

I'm a fourth-year student working toward a career as a **DevOps Engineer**. I have hands-on experience building applications across several backend and frontend frameworks, and I'm currently focused on deepening my skills in infrastructure, containerization, and cloud computing.

- Career direction: **DevOps / Platform Engineering**
- Currently learning: **Kubernetes, Proxmox, Google Cloud Platform**
- Interested in: microservice architecture, deployment automation (CI/CD), and infrastructure optimization

---

## Tech Stack

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

## Featured Projects

### Resona — Music Streaming Platform

A full-stack music streaming application split across two repositories: [**resona**](https://github.com/HaHiepThanh/resona) (Angular frontend) and [**resona_core**](https://github.com/HaHiepThanh/resona_core) (NestJS backend).

**Frontend — Angular 19**
- Centralized state management with **NgRx** (Store + Effects) across 11 domains: track, playlist, queue, play, history, favorite, comment, search, category, profile, and auth
- UI built on **Angular Material + CDK**: player bar, drag-and-drop play queue, synchronized lyrics, comment threads, and auth dialogs
- User authentication via **Firebase Authentication** (`@angular/fire`), plus custom pipes for image resolution, duration formatting, and lyrics parsing

**Backend — NestJS 11 (TypeScript)**
- **Domain-driven architecture**: 11 self-contained modules (track, playlist, playlist_tracks, category, comment, queue, history, notification, profile, auth, supabase), each with its own controller, service, entity, and DTOs
- **Chunked file upload**: the client splits audio files into parts and the server reassembles them using Node.js streams, allowing large uploads without exhausting memory
- **FFmpeg audio pipeline**: automatic transcoding to AAC/M4A, ADTS → ASC remuxing, and the `+faststart` flag so browsers can read metadata as soon as playback begins; accurate duration probing via `ffprobe` and tag extraction with `music-metadata`
- **Supabase** for object storage and the **PostgreSQL** database, accessed through **TypeORM** with fully modeled relations (ManyToOne / OneToMany / ManyToMany, cascade delete)
- Secured by a **Firebase Admin SDK** middleware that verifies ID tokens, with request validation through `class-validator` and a global `ValidationPipe`
- Containerized with **Docker** (`node:20-bullseye` image with FFmpeg preinstalled)

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

### [Microservices — Employee Management](https://github.com/HaHiepThanh/Microservices-EmployeeManagement)

An HR management system built on a **microservice architecture** with five independent services (auth, employee, department, attendance, payroll), following the **database-per-service** pattern — each service owns its own MySQL instance.

- **Synchronous communication:** REST (`RestClient`) for the employee → department flow, and **gRPC / Protocol Buffers** for high-performance calls from employee → payroll and attendance
- **Asynchronous communication:** **RabbitMQ (Spring AMQP)** powering an event-driven design — auth and employee publish events that consumers process independently
- **Security:** stateless Spring Security with **JWT**, OAuth2 Resource Server, and **RBAC** across three roles (ADMIN / HR / EMPLOYEE)
- **Deployment:** multi-stage Docker builds, Docker Compose with `healthcheck` and `depends_on: service_healthy` orchestration, images published to Docker Hub
- **Design patterns:** Adapter (isolating external DTO coupling), Builder, and Singleton — each documented with its exact location in the codebase

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

### [SA Seminar — E-Commerce Microservices](https://github.com/HaHiepThanh/sa-seminar-microservice)

A microservice-based e-commerce platform built on **Micronaut**, comprising six services: catalog, inventory, user, cart, order-payment, and mail. Its centerpiece is a **real-time group-buy** feature.

- **Real-time delivery:** **WebSocket** and **Server-Sent Events (SSE)** push live group-buy state to clients, with Nginx specifically tuned (`proxy_buffering off`, HTTP/1.1) so streams aren't buffered
- **API Gateway:** **Nginx** acts as a reverse proxy, routing all traffic to the right service by path while also serving the static frontend
- **Inter-service communication:** **gRPC** (catalog/order ↔ inventory) combined with **RabbitMQ** for asynchronous events (order placed → stock deducted → confirmation email sent)
- **Data layer:** Micronaut Data (Hibernate JPA & JDBC), **Flyway migrations**, HikariCP connection pooling, MySQL 8
- **Security:** Micronaut Security **JWT** with **BCrypt** password hashing
- **Also featuring:** reactive programming with **Project Reactor**, auto-generated API docs via **OpenAPI / Swagger**, a mail service built on Jakarta Mail, and tests written with **JUnit 5**

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

## GitHub Stats

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
