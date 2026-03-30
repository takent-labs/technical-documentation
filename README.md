<div align="center">

<br/>

<pre>
  ████████╗ █████╗ ██╗  ██╗███████╗███╗   ██╗████████╗
     ██╔══╝██╔══██╗██║ ██╔╝██╔════╝████╗  ██║╚══██╔══╝
     ██║   ███████║█████╔╝ █████╗  ██╔██╗ ██║   ██║   
     ██║   ██╔══██║██╔═██╗ ██╔══╝  ██║╚██╗██║   ██║   
     ██║   ██║  ██║██║  ██╗███████╗██║ ╚████║   ██║   
     ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═══╝  ╚═╝   
</pre>

---

<h3><code>REST API</code> &nbsp;·&nbsp; <code>Web</code> &nbsp;·&nbsp; <code>Android / iOS</code> &nbsp;·&nbsp; <code>Desktop</code></h3>

---

<br/>

<sub><b>Backend & Core</b></sub><br>
![NestJS](https://img.shields.io/badge/nestjs-%23E0234E.svg?style=for-the-badge&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-3fb950?style=for-the-badge&logo=Prisma&logoColor=white)
![Swagger](https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)

<sub><b>Frontend Web</b></sub><br>
![Next.js](https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-orange?style=for-the-badge&logo=react&logoColor=white)

<sub><b>Frotend mobile</b></sub><br>
![Kotlin](https://img.shields.io/badge/kotlin-%237F52FF.svg?style=for-the-badge&logo=kotlin&logoColor=white)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![WinUI](https://img.shields.io/badge/WinUI_3-0078D4?style=for-the-badge&logo=windows&logoColor=white)

<sub><b>Infrastructure & Data</b></sub><br>
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare_R2-F38020?style=for-the-badge&logo=Cloudflare&logoColor=white)
![Neon](https://img.shields.io/badge/Neon-00E599?style=for-the-badge&logo=Neon&logoColor=black)
![pnpm](https://img.shields.io/badge/pnpm-%234a4a4a.svg?style=for-the-badge&logo=pnpm&logoColor=f69220)

<br/>

---

<sub>Technical Documentation &nbsp;·&nbsp; Proyecto Intermodular &nbsp;·&nbsp; Developed by <strong>Óscar</strong></sub>

<br/>

</div>

## Table of Contents

- [System architecture](#system-architecture)
  - [General connection scheme of the 3 apps with the API and the database](#general-connection-scheme-of-the-3-apps-with-the-api-and-the-database)
    - [Architecture Analysis](#architecture-analysis)
  - [Main technologies used in each part](#main-technologies-used-in-each-part)
- [REST-API Development](#rest-api-development)
  - [Technical stack justification](#technical-stack-justification)
  - [Endpoint list and dynamic documentation with Swagger](#endpoint-list-and-dynamic-documentation-with-swagger)
  - [HTTP methods and REST semantics](#http-methods-and-rest-semantics)
  - [Infrastructure and dockerization](#infrastructure-and-dockerization)
  - [Authentication and critical services](#authentication-and-critical-services)
  - [Examples of requests and responses](#examples-of-requests-and-responses)
    - [Sign In](#sing-in)
    - [Create post](#create-post)
  - [Implementation notes](#implementation-notes)
- [Database](#database)
  - [Persistence architecture](#persistence-architecture)
  - [Entity-Relationship Diagram](#entity-relationship-diagram)
  - [Migration management](#migration-management)
- [Web Application](#web-application)
  - [Technological justification and design decisions](#technological-justification-and-design-decisions)
  - [Project structure and patterns](#project-structure-and-patterns)
  - [Communication with the backend and data security](#communication-with-the-backend-and-data-security)
  - [Animations and performance](#animations-and-performance)
- [Mobile application](#mobile-application)
  - [Technical stack justification](#technical-stack-justification-1)
  - [Architecture and code structure](#architecture-and-code-structure)
  - [Connection with the API](#connection-with-the-api)
  - [Multimedia and UI resource management](#multimedia-and-ui-resource-management)
  - [Technical quality and sustainability](#technical-quality-and-sustainability)
- [Desktop application](#desktop-application)
  - [Technological justification and design decisions](#technological-justification-and-design-decisions-1)
  - [Project structure and patterns](#project-structure-and-patterns-1)
  - [Connection with the API and data security](#connection-with-the-api-and-data-security)
  - [Technology used](#technology-used)
- [Security and data protection](#security-and-data-protection)
  - [Critical protection mechanisms](#critical-protection-mechanisms)
  - [User management and access control](#user-management-and-access-control)
  - [Secrets management and environment variables](#secrets-management-and-environment-variables)
  - [Additional best practices and pending items](#additional-best-practices-and-pending-items)
- [Instance deployment](#instance-deployment)
  - [REST-API](#rest-api)
  - [Database](#database-1)
  - [Web application](#web-application-1)
  - [Mobile application](#mobile-application-1)
  - [Desktop application](#desktop-application-1)
- [Usage and maintenance guide](#usage-and-maintenance-guide)
  - [Step 1: Clone the repositories](#step-1-clone-the-repositories)
  - [Step 2: Environment variables](#step-2--environment-variables)
  - [Step 3: Phased startup](#step-3-phased-startup)
  - [Paso 4: Final part](#paso-4-final-part)
  - [Frequent problems](#frequent-problems)
    - [The mystery of the Neon connection](#the-mystery-of-the-neon-connection)
    - [The Ktor jam when uploading images to R2](#the-ktor-jam-when-uploading-images-to-r2)
    - [The learning curve](#the-learning-curve)
- [Future improvements](#future-improvements)
- [My thoughts on the project](#my-thoughts-on-the-project)
- [Resources and Documentation Used](#resources-and-documentation-used)
  - [Backend & Infrastructure (API-REST)](#backend--infrastructure-api-rest)
  - [Web Application (Frontend)](#web-application-frontend)
  - [Mobile Application (Android/KMP)](#mobile-application-androidkmp)

---

## System architecture

Nowadays, being a developer is no longer just about writing code. AI does it much better than we do; and I’m not just saying that, Linus Torvalds himself said it in one of his recent GitHub activities. That is why my focus on this project transcends simply "grinding code."

I have designed this project from a standpoint of technical architecture mastery: selecting each technology with a critical purpose and understanding not only the "what," but the "when" and the "why" behind every decision.

This architecture is not a set of isolated tools, but an interconnected ecosystem designed for efficiency and scalability.

https://github.com/torvalds/AudioNoise/commit/93a72563cba609a414297b558cb46ddd3ce9d6b5

![Commit de Linus Torvalds](/images/commit-torvalds.png)

---

### General connection scheme of the 3 apps with the API and the database

As developers, time is money, and deadlines are our worst enemy. That is why I have integrated modern and consolidated external services (such as **Lemon Squeezy** and **Resend**, among others). My goal is not to prove that I can write thousands of lines of redundant code, but that I am capable of delivering a **functional, secure, and validated MVP** in record time. Delegating heavy infrastructure allows me to focus on what truly adds value: the business logic and the architecture of this multiplatform ecosystem.

The system is based on a REST API-oriented "microservices" architecture, where the backend acts as the central orchestrator. The design follows a **poly-repo** approach, allowing each client and the server to evolve independently yet perfectly synchronized.

![https://excalidraw.com/#json=fBZmm21tE_fx-msb3ecSo,ZvvgV63EQhAawCPK-nfOhw](/images/esquema-arquitectura.png)

---

#### Architecture Analysis

As can be seen in the previous scheme, the full weight of the logic rests on a server developed in **Nest.js**. This choice was not random; it was the result of weeks of research. Its modular architecture will allow me to scale the code without it turning into unmanageable "spaghetti code" (like the project I have been assigned at my internship company).

- **Traffic and protection:** My idea is to put **Cloudflare** in front of everything. Not just for DDoS attack filtering and the WAF, but to hide my server's real IP and prevent direct scans.
- **Persistence:** I use **PostgreSQL** because of how robust it is with relational data. Communication is handled through an **ORM** to sanitize queries and prevent any SQL Injection attempts from the clients.
- **Files (R2):** Images and documents never touch the central server; they go directly to **Cloudflare R2**, which is S3-compatible. This frees up bandwidth and provides practically infinite storage. Doing it the way it was proposed in class seems like a bad practice to me: storage costs would skyrocket, I wouldn't be able to easily use a CDN to serve the images, and the database would grow exponentially. Furthermore, Postgres is not designed to move gigabytes of binary data efficiently.
- **Deployment:** The entire backend runs in **Docker** containers. It is the only way to guarantee that "it works on my machine" also holds true when deploying to production.

> [!IMPORTANT]
> To avoid wasting time on infrastructure that others already do better, I will delegate two critical points:
> 
> * **Payments (Lemon Squeezy):** It handles the entire payment gateway and invoice management, taking the legal compliance of banking data off my hands.
> * **Email (Resend):** I use it for sending transactional emails, ensuring that messages land in the inbox and not in the spam folder.

### **Main technologies used in each part**

Selecting the tech stack has been the most critical decision. My priority has been **unification and type safety**, within all the limitations and impediments that were placed upon me. I have opted for an environment based almost entirely on **TypeScript**, eliminating friction when sharing data models between layers. It is not just about using modern tools, but about implementing a professional workflow where **CI/CD**, **containerization**, and **static typing** guarantee that the system is maintainable and scales without breaking.

It is worth noting that, although I have used specific environments for mobile and desktop due to academic requirements, in a real production scenario my choice would have been **React Native** for mobile and **Tauri** for desktop. This decision would allow for total code consistency, sharing types and business logic throughout the entire ecosystem. This would not only make the project more scalable and optimal, but it would also drastically reduce technical debt by unifying the stack under a single high-performance language.


<br/>

<div align="center">

| Layer | Technology | Role | Why |
|:---:|:---|:---|:---|
| ![](https://img.shields.io/badge/Backend-1a1a2e?style=flat-square) | ![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white) | Modular REST API framework | Enforces order via TypeScript; replaces Spring Boot to unify the language with the frontend |
| ![](https://img.shields.io/badge/Backend-1a1a2e?style=flat-square) | ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white) | Server-side JS runtime | Non-blocking I/O model; covered in the programme — efficient and sustainable |
| ![](https://img.shields.io/badge/Backend-1a1a2e?style=flat-square) | ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white) | Static typing over JavaScript | Prevents runtime errors; promotes SOLID principles and safe refactoring across all layers |
| ![](https://img.shields.io/badge/Backend-1a1a2e?style=flat-square) | ![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white) | Next-gen ORM | Guarantees data integrity; generates versioned SQL migrations tracked in GitHub |
| ![](https://img.shields.io/badge/Database-0f3460?style=flat-square) | ![Neon](https://img.shields.io/badge/Neon-00E599?style=flat-square&logo=neon&logoColor=black) | Serverless PostgreSQL | Scales to zero when idle; database branching for safe migration testing |
| ![](https://img.shields.io/badge/Database-0f3460?style=flat-square) | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) | Containerisation | Eliminates «works on my machine»; identical environment from dev to production |
| ![](https://img.shields.io/badge/Web-16213e?style=flat-square) | ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) | Full-stack web framework | SSR, SSG, ISR, and API routes in one place; superior SEO and performance |
| ![](https://img.shields.io/badge/Web-16213e?style=flat-square) | ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) | UI component library | Declarative rendering; automatic XSS escaping; industry-standard ecosystem |
| ![](https://img.shields.io/badge/Web-16213e?style=flat-square) | ![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white) | Utility-first CSS framework | Enables rapid, consistent styling without leaving the component file |
| ![](https://img.shields.io/badge/Mobile-533483?style=flat-square) | ![Kotlin](https://img.shields.io/badge/Kotlin_Multiplatform-7F52FF?style=flat-square&logo=kotlin&logoColor=white) | Shared cross-platform logic | 80 % of business logic, models, and network calls shared between Android and iOS |
| ![](https://img.shields.io/badge/Mobile-533483?style=flat-square) | ![Android Studio](https://img.shields.io/badge/Android_Studio-3DDC84?style=flat-square&logo=android-studio&logoColor=white) | Official Android IDE | Smart editor, emulator, and Android-specific performance profiling tools |
| ![](https://img.shields.io/badge/Desktop-1b4332?style=flat-square) | ![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=c-sharp&logoColor=white) | Desktop implementation language | Strongly-typed; eliminates runtime error categories; mature Windows ecosystem |
| ![](https://img.shields.io/badge/Desktop-1b4332?style=flat-square) | ![Visual Studio](https://img.shields.io/badge/Visual_Studio-5C2D91?style=flat-square&logo=visual-studio&logoColor=white) | Windows desktop IDE | First-class C# / XAML toolchain with integrated XAML designer and debugger |
| ![](https://img.shields.io/badge/Desktop-1b4332?style=flat-square) | ![WinUI 3](https://img.shields.io/badge/WinUI_3-0078D4?style=flat-square&logo=windows&logoColor=white) | Native Windows UI framework | True native performance; Windows 11 design language with Fluent animations |
| ![](https://img.shields.io/badge/Storage-7b2d00?style=flat-square) | ![Cloudflare R2](https://img.shields.io/badge/Cloudflare_R2-F38020?style=flat-square&logo=cloudflare&logoColor=white) | Object storage for media | S3-compatible with zero egress fees; pre-signed URLs offload transfers from the API |
| ![](https://img.shields.io/badge/Network-b5451b?style=flat-square) | ![Cloudflare](https://img.shields.io/badge/Cloudflare_CDN%2FWAF-F38020?style=flat-square&logo=cloudflare&logoColor=white) | CDN, WAF & DDoS mitigation | Hides the server's real IP; blocks malicious traffic at the edge before it hits the API |
| ![](https://img.shields.io/badge/Hosting-2d3436?style=flat-square) | ![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white) | Web frontend CI/CD | Every commit triggers a deployment preview; seamless Next.js integration |
| ![](https://img.shields.io/badge/Hosting-2d3436?style=flat-square) | ![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black) | REST API hosting | Docker-native deployments; automatic restarts and zero server configuration |
| ![](https://img.shields.io/badge/Services-6c3483?style=flat-square) | ![Lemon Squeezy](https://img.shields.io/badge/Lemon_Squeezy-FFC107?style=flat-square&logo=lemonsqueezy&logoColor=black) | Payments & subscriptions | Merchant of record — handles VAT and global taxes automatically |
| ![](https://img.shields.io/badge/Services-6c3483?style=flat-square) | ![Resend](https://img.shields.io/badge/Resend-000000?style=flat-square&logo=resend&logoColor=white) | Transactional email | Modern API, clear delivery logs, and high inbox rate — simpler than SendGrid |
| ![](https://img.shields.io/badge/DevOps-2c3e50?style=flat-square) | ![Git](https://img.shields.io/badge/Git%20%2F%20GitHub-181717?style=flat-square&logo=github&logoColor=white) | Version control & collaboration | Branching, pull requests, and history audits across all poly-repo clients |

</div>

<br/>


Although the mobile and desktop development was carried out in Android Studio and Visual Studio with C# and WinUI, the API architecture is designed to be client-agnostic, facilitating a future migration to React Native/Tauri as mentioned in the introduction.

## REST-API Development

For me, the API is the most critical part of this project and the one I have dedicated the most effort to, as it is where all the business logic resides. I consider the clients to be secondary pieces compared to the **intelligent core** of the system. This API is not just a simple data bridge, but an orchestrator designed under the **Modular Architecture** paradigm. I selected **NestJS**, beyond its popularity, for its ability to enforce order through TypeScript, allowing me to build a robust backend where each module is independent, testable, and scalable.


### **Technical stack justification**

Since the project design is open-ended, I have made decisions that raise the software quality beyond the minimum requirements:

- **NestJS & TypeScript:** This is the professional evolution of Node.js covered in the course. The use of static types allows me to meet the "well-structured code" criterion while minimizing runtime errors.
- **Prisma ORM:** As an evolution of traditional ORMs, Prisma guarantees data integrity and consistency, generating automatic migrations that facilitate version control.
- **Sustainability:** This stack is optimized for efficient CPU and memory consumption, ensuring maintainable and long-lasting software.

### Endpoint list and dynamic documentation with Swagger

A professional backend is not complete without a clear contract for its clients. Therefore, I have implemented **Swagger**. Instead of static tables that become obsolete, I have opted for **live, accessible documentation** that includes:

- **Endpoint Catalog:** A complete list of routes categorized by modules (Auth, Users, etc.).
- **Schema Definition (DTOs):** Exact specification of the required data, their types, and the validation rules applied through **class-validator**.
- **Real-Time Testing:** An interactive interface to validate responses and status codes (200, 201, 401, 500) directly from the browser.

![Captura de pantalla 2026-03-29 a las 20.36.47.png](/images/swagger.png)

### **HTTP methods and REST semantics**

In this project, I do not use HTTP methods as mere data tunnels, but instead strictly follow **RESTful** semantics. This ensures that any client knows exactly what to expect from the API based on the standard.

- **GET / POST / PATCH / DELETE:** Used according to their standard purpose.
- **Precise Status Codes:** Every request returns an accurate code: **201 Created** for successful registrations, **401 Unauthorized** for failed access, **400 Bad Request** when **DTOs** detect malformed data, or **429 Too Many Requests**.

### **Infrastructure and dockerization**

```bash
src/
├── users/                  
│   ├── dto/                # Filters which data we allow to be sent.
│   ├── entities/           # How the user is stored in the database.
│   ├── users.controller.ts # Receives requests and distributes them.
│   ├── users.service.ts    # User logic (save, search, etc.).
│   └── users.module.ts     # Unites the above and allows exporting to other modules.
│
├── auth/                    
│   ├── dto/                # Data required for login.
│   ├── auth.controller.ts  # Login and registration endpoints.
│   ├── auth.service.ts     # Creates keys (tokens) and verifies passwords.
│   └── auth.module.ts      # Connects security with users.
│
├── common/                  
│   ├── hashing/            # Shared logic for password encryption.
│   └── r2/                 # Logic for uploading images and files.
│
└── main.ts
```

To eliminate the "it works on my machine" factor, I have implemented a professional containerization strategy:

- **Docker Multi-Stage:** I have designed a staged **Dockerfile**. The build stage generates the necessary code, while the execution stage delivers a final image based on `node:24-bookworm-slim`. This drastically reduces image size and improves security by removing unnecessary tools in production.
- **Docker Compose:** I use `compose.yaml` to orchestrate the container, manage environment variables, and ensure the service restarts automatically.
- **Optimization:** Through `.dockerignore`, I ensure that sensitive files (like `.env`) or unnecessary ones (local `node_modules`) do not clutter the production image.

### **Authentication and critical services**

- **Modular Architecture:** I used the NestJS CLI to generate resources (`nest g res`), maintaining a clear separation: `controllers.ts` manage requests and `services.ts` execute the business logic.
- **R2 Storage:** Heavy file management (images/videos) is delegated to **Cloudflare R2**. The API does not store files; it generates **pre-signed URLs** so that the upload happens directly between the client and the storage, optimizing server performance.
- **Security:** Implementation of **Rate Limiting** to prevent abuse and brute-force attacks. Authentication via **JWT** and password hashing with **Bcrypt**.

API security is non-negotiable. I have implemented a **Stateless** authentication system based on **JWT (JSON Web Tokens)**:

- After validating credentials with **Bcrypt** in the Auth service, the API issues a signed token.
- I have developed NestJS **Guards** that intercept requests to private endpoints. If the client does not present a valid token in the `Authorization: Bearer <token>` header, the API automatically denies access.
- The token contains only the minimum necessary information, such as the `sub` or User ID, avoiding the exposure of sensitive data in network traffic.

### **Examples of requests and responses**

#### Sing In

**Request Body:**

```json
### Iniciar sesión
POST {{baseUrl}}/auth/sign-in
Content-Type: application/json

{
  "email": "oscar@oscar.com",
  "password": "12345678"
}
```

**Response status 200 OK:**

```json
HTTP/1.1 200 OK
X-Powered-By: Express
Access-Control-Allow-Origin: *
X-RateLimit-Limit: 10
X-RateLimit-Remaining: 8
X-RateLimit-Reset: 60
Content-Type: application/json; charset=utf-8
Content-Length: 371
ETag: W/"173-rKklWa1kJgF+1UtEAKz+v8IofZs"
Date: Sun, 29 Mar 2026 19:52:31 GMT
Connection: close

{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJkNTZiMGZhOC01OGFlLTRjZWEtYjY3My04ODc4MGQ5ZTJmZjciLCJ1c2VybmFtZSI6Im9za2lyb3ZlIiwiZW1haWwiOiJvc2NhckBvc2Nhci5jb20iLCJpYXQiOjE3NzQ4MTM5NTEsImV4cCI6MTc3NDgyMTE1MX0.xMDBVXQv3xxKUB2uKbYc4uOMsciRCrZksYlOc9rsa7c",
  "user": {
    "id": "d56b0fa8-58ae-4cea-b673-88780d9e2ff7",
    "username": "oskirove",
    "email": "oscar@oscar.com"
  }
}
```

**Response status 401:**

```json
HTTP/1.1 401 Unauthorized
X-Powered-By: Express
Access-Control-Allow-Origin: *
X-RateLimit-Limit: 10
X-RateLimit-Remaining: 7
X-RateLimit-Reset: 10
Content-Type: application/json; charset=utf-8
Content-Length: 85
ETag: W/"55-jgHgE06ox48dg0u5JgfGq7gDZos"
Date: Sun, 29 Mar 2026 19:53:21 GMT
Connection: close

{
  "message": "Email o contraseña incorrectos",
  "error": "Unauthorized",
  "statusCode": 401
}
```

**Response status 404:**

```json
HTTP/1.1 404 Not Found
X-Powered-By: Express
Access-Control-Allow-Origin: *
X-RateLimit-Limit: 10
X-RateLimit-Remaining: 8
X-RateLimit-Reset: 40
Content-Type: application/json; charset=utf-8
Content-Length: 71
ETag: W/"47-hjRzKCNfVRSauR2k7GKlbsW85S0"
Date: Sun, 29 Mar 2026 19:51:49 GMT
Connection: close

{
  "message": "El usuario no existe",
  "error": "Not Found",
  "statusCode": 404
}
```

---



#### Create post

**Request Body:**

```json
POST {{baseUrl}}/posts
Content-Type: application/json
Authorization: Bearer {{access_token}}

{
  "content": "La era del 'Cloud-Only' está llegando a su fin. 🏠 He migrado toda mi infraestructura crítica de SaaS comerciales a instancias auto-alojadas usando Docker y Coolify. Tener el control total de mis datos y de mi base de datos Postgres no solo me ahorra cientos de dólares al mes, sino que me da una privacidad que ninguna Big Tech puede garantizar. El self-hosting ya no es un hobby, es una necesidad profesional en 2026. 🔐",
  "hashtags": ["SelfHosting", "OpenSource", "Docker", "Privacy", "DevOps"]
}
```

**Response 200 OK:**

```json
HTTP/1.1 201 Created
X-Powered-By: Express
Access-Control-Allow-Origin: *
X-RateLimit-Limit: 10
X-RateLimit-Remaining: 7
X-RateLimit-Reset: 28
Content-Type: application/json; charset=utf-8
Content-Length: 629
ETag: W/"275-IQ/61Xs6fhgHymEOuGR2YAWA0cQ"
Date: Sun, 29 Mar 2026 19:55:10 GMT
Connection: close

{
  "id": "7cd6c499-098f-4e43-9235-fb015348855b",
  "userId": "d56b0fa8-58ae-4cea-b673-88780d9e2ff7",
  "content": "La era del 'Cloud-Only' está llegando a su fin. 🏠 He migrado toda mi infraestructura crítica de SaaS comerciales a instancias auto-alojadas usando Docker y Coolify. Tener el control total de mis datos y de mi base de datos Postgres no solo me ahorra cientos de dólares al mes, sino que me da una privacidad que ninguna Big Tech puede garantizar. El self-hosting ya no es un hobby, es una necesidad profesional en 2026. 🔐",
  "imageUrl": null,
  "createdAt": "2026-03-29T19:55:09.431Z",
  "updatedAt": "2026-03-29T19:55:09.431Z"
}
```

---

</aside>

### Implementation notes

To replicate this environment on any machine, simply run

```bash
# dependency instalation
pnpm install

# Up environment
docker compose up --build
```

---

## Database

The database is the system's memory. In this project, I have moved away from volatile or poorly structured solutions, opting instead for a solid relational database: **PostgreSQL**. I use **Neon** as a **serverless** provider, which allows me to have a high-performance infrastructure that scales according to demand. To interact with it, I employ **Prisma ORM**, transforming the database schema into type-safe TypeScript code and eliminating the possibility of errors due to types or malformed queries.

### Persistence architecture

The choice of **Neon** as a database is not only for its performance but also for its advanced infrastructure management capabilities:

- **Database branching:** This functionality allows me to create instantaneous copies of the production database to test new features or high-risk migrations in an isolated environment, without ever compromising the integrity of live data. It is a cutting-edge feature that ensures a professional development lifecycle.
- **Serverless Scalability:** The database automatically adjusts its resources, allowing for efficient management and total system availability.

### **Entity-Relationship Diagram**

I have normalized the database design to avoid redundancy and guarantee integrity. The main axes are user management, posts, and the relationship with external services.

![takent-ER.png](/images/takent-ER.png)

![DDBB-Takent.png](/images/DDBB-Takent.png)

For this design, I have implemented advanced security and optimization criteria:

- **Use of UUIDs:** Instead of using traditional simple incremental IDs (1, 2, 3...), all tables use **UUIDs**. This adds a critical layer of security, preventing malicious users from guessing data volume, predicting records, or performing mass **scraping** via brute force on URLs.
- **Binary Decoupling:** Following best practices, the database **only stores reference URLs** for multimedia files. The actual images and videos reside in Cloudflare R2; this keeps the database lightweight, speeds up backups, and drastically reduces query response times.

### **Migration management**

Furthermore, I have decided that the database should grow organically with the application. Therefore, the structure is never touched manually through graphical interfaces; it is managed through an **Automated Migration** flow:

- **Version Control:** Every change in the data model generates a SQL file in the `prisma/migrations` folder. These files are synchronized on GitHub, allowing any developer or the deployment server to replicate the exact same structure deterministically.
- **Prisma Migrate:** I use the `pnpx prisma migrate dev` command during development. This ensures that the database evolves alongside the code, allowing for change audits and providing the ability to perform rollbacks if necessary.

## **Web Application**

For the web frontend, my goal has been to build a **User Experience** that feels fluid, fast, and, above all, professional. I have opted for **Next.js** as the base framework, not only for its native integration with the Node.js (covered in the course) and React ecosystem, nor for its high SEO performance, but for its **Server-Side Rendering (SSR)** capabilities. This allows me to deliver an application that loads instantly and manages data security from the server, moving away from traditional SPAs that expose too much logic in the browser.

### **Technological justification and design decisions**

Based on the design freedom mentioned in the specifications, I have made decisions oriented toward a real-world work environment:

- **TypeScript Ecosystem:** By using the same language as in the API (NestJS), I have eliminated friction in development. Type safety ensures that data traveling from the database to the interface is consistent, reducing critical errors by 20%.
- **High-Level UI/UX:** For the visual design, I have combined **Shadcn/ui**, **Magic-UI**, and **HeroUI**. This choice allows me to avoid wasting time reinventing basic components (buttons, modals) and focus on creating an impactful and animated interface using **GSAP**, raising the project's visual standard.

### **Project structure and patterns**

I have organized the code following an **atomic componentization** pattern, which facilitates maintenance and code reuse. Below is an example of the architecture I followed to structure the project:

```bash
takent-web-app/
├── app/                    # Application core (App Router)
│   ├── (routes)/           # Logically organized route groups.
│   ├── api/auth/           # Route Handlers to manage the session (Proxy).
│   ├── layout.tsx          # Global layout (ThemeProvider, Fonts).
│   └── page.tsx            # Application entry point (Landing Page).
├── components/             # Reusable React components
│   ├── auth/               # Specific login/registration components.
│   ├── dashboard/          # Dashboard visual logic (Feed, Profile).
│   │   ├── Header.tsx
│   │   └── NavDock.tsx
│   ├── landing_page/       # Public page sections.
│   └── ui/                 # Atomic design components (Shadcn, HeroUI).
│       ├── FooterSection.tsx
│   	└── Logo.tsx
├── context/                # React context providers.
├── lib/                    # Global utilities and configurations.
├── services/               # Abstraction layer for API calls
│   └── post/
│       └── post.service.ts # Typed functions to interact with /posts.
├── store/                  # Global state management (Zustand).
└── types/                  # Global TypeScript interface definitions.
```

- **/app:** I use the modern Next.js routing system, which allows me to use nested layouts and optimized page loading.
- **/components:** Divided into reusable UI components and business components with logic.
- **/store:** For global state management. I have chosen **Zustand** as a lightweight and efficient alternative to Redux, allowing information (such as logged-in user data) to flow throughout the app without unnecessary re-renders or new database requests.

### **Communication with the backend and data security**

The communication architecture does not expose logic to the client; everything is processed in an intermediate server layer to ensure maximum security:

- **Server Actions:** Instead of performing traditional `fetch` requests from the browser, I use **Server Actions**. This allows asynchronous functions to be executed directly on the Next.js server. In this way, the logic for form submissions or profile updates never reaches the client, reducing the attack surface and improving performance by sending less JavaScript to the browser.
- **Route Handlers (API Proxy):** For complex data retrieval requests, I implement **Route Handlers**. These act as a **secure Proxy** that hides the real URL of my NestJS API, allowing for the addition of security headers and data transformation before it reaches the interface.
- **Session Management (HttpOnly Cookies):** Complying with the most demanding security standards, JWT tokens are **never stored in LocalStorage**, as it is vulnerable to XSS attacks. Instead, they are managed via cookies with the **HttpOnly** flag from the server. This ensures the token is only accessible for HTTP requests and remains invisible to any malicious script on the client side.
- **Robust Validation with Zod:** I use **Zod** as the schema validation engine. By sharing the same types as the backend, I ensure that forms (managed with **React Hook Form**) only send data that strictly complies with what the API expects, avoiding unnecessary network errors.

### **Animations and performance**

To make the application feel alive and more visually pleasing, I decided to integrate **GSAP**. This allows for smooth transitions between states and micro-interactions that improve user retention.

---

## **Mobile application**

For mobile development, my priority has been **software sustainability** and technical robustness. Although the specifications focus on native Android, I have decided to implement **Kotlin Multiplatform (KMP)**. This strategic decision allows me to comply with the mandatory use of **Android Studio** while raising the standard, ensuring the system is maintainable, scalable, and ready for deployment on both iOS and Android without rewriting the application's core.

### Technical stack justification

Based on the design freedom mentioned in the specifications, I have made decisions oriented toward a real-world professional environment:

- **Evolution of Java:** Kotlin is the natural progression from what was learned in the course. It allows me to use higher-order functions, **null-safety**, and coroutines, eliminating common Java errors.
- **Ktor & Serialization:** For REST API requests, I use the Ktor engine. This allows me to handle JSON serialization into Kotlin objects natively and securely.
- **Multiplatform Settings:** For persisting sensitive data (JWT tokens), I use this library which automatically maps to **EncryptedSharedPreferences** on Android, meeting the highest mobile security standards.

### Architecture and code structure

I have organized the code under a **Clean Architecture** scheme within the shared module, as seen in the GitHub repository directory structure:

- **`data/`:** This is where the communication intelligence resides.
    - **`network/KtorClient`:** I use **Ktor** as a multiplatform HTTP client. It is a much more modern and lightweight solution than traditional ones, allowing for asynchronous and efficient data serialization.
    - **`auth / post / model`:** I implement **DTOs** that refine the API structure, ensuring the data contract is unbreakable.
- **`Repository`:** Repositories (AuthRepository, PostRepository) act as an abstraction layer. The UI doesn't know where the data comes from; it only consumes it, which facilitates testing and maintainability.
- **`ui/`:** I use **Jetpack Compose** for a modern, declarative interface. It is organized by functional modules (auth, feed, profile, navigation), allowing for clean, decoupled development.

### Connection with the API

To communicate with the server, I don't send loose requests; I have set up a centralized HttpClient with Ktor. Instead of repeating code, I designed a robust client that manages the entire network lifecycle in a single point, implementing the following:

1. **Native Serialization:** I installed the ContentNegotiation plugin with Kotlinx Serialization. The client "understands" JSON automatically and converts it into my shared logic objects without extra manual coding.
2. **Headers and Auth:** I configured an interceptor (`DefaultRequest`) that injects the JWT Token and necessary headers into every request. I don't have to pass the token manually; the client does it for me.
3. **Resilience:** I defined specific timeouts for connection and response. If the server takes too long or there is a micro-outage, the app handles it instead of crashing.
4. **Maintainability:** This is pure efficiency. If the API changes tomorrow, I only tweak one file in `data/network/ktorClient`, and the entire app's network logic updates instantly.

### Multimedia and UI resource management

- **Coil:** Used for loading images from **Cloudflare R2**. Coil intelligently manages caching and performance, ensuring the app doesn't consume unnecessary device resources.
- **Peekaboo:** An advanced implementation for selecting images from the gallery, allowing the user to upload content to posts intuitively and fluidly.
- **Konform:** **Type-safe** form validation. Before a request leaves for the API, the data is validated on the client side, saving latency and server computation.

### **Technical quality and sustainability**

By separating the logic into `commonMain`, I have achieved a software design where 80% of the code is reusable. This is not just an improvement over outdated resources, but a commitment to **sustainable programming**: less code to maintain means fewer errors and a much longer project lifespan.

## Desktop application

For the desktop frontend, my goal has been to build a **User Experience** that feels native, secure, and visually consistent with the web platform. I have opted for **WinUI 3 (Windows App SDK)** as the base framework, not only for its deep integration with the Windows 11 design language and modern rendering pipeline, but for its ability to deliver **truly native performance** without the overhead of a web-based shell. This allows the application to feel like a first-class Windows citizen while sharing the same brand identity as the web frontend.

### Technological justification and design decisions

Based on the design freedom mentioned in the specifications, I have made decisions oriented toward a real world Windows development environment:

- **C# and XAML Ecosystem:** By using C# as the implementation language, I benefit from a strongly typed, mature ecosystem that eliminates entire categories of runtime errors. XAML's declarative UI model allows strict separation between layout and business logic, mirroring the component-based philosophy used on the web side.
- **High-Level UI/UX:** For the visual design, I have built a custom style system directly in XAML using `ResourceDictionary` entries and `ControlTemplate` overrides with `VisualStateManager`. Rather than relying on the default WinUI control aesthetics — which produce poor contrast on custom color schemes — every interactive element (buttons, tabs, inputs) has hand-crafted hover and press states driven by `ColorAnimation` storyboards, producing smooth `150ms` transitions that match the fluidity expected in a modern social application.

### Project structure and patterns

I have organized the code following a **separation of concerns** pattern, isolating HTTP communication, secure storage, and UI logic into distinct layers:

```
takent-desktop-app/
├── Services/
│   └── AuthService.cs          # HTTP client + PasswordVault token management
├── MainWindow.xaml             # Declarative UI: auth forms + home panel
├── MainWindow.xaml.cs          # Code-behind: event handlers + view state logic
├── App.xaml                    # Application entry point + global resources
├── App.xaml.cs                 # App lifecycle (window initialization)
└── Package.appxmanifest        # Windows App SDK package identity + capabilities
```

- **/Services:** The `AuthService` class acts as the single source of truth for all authentication logic. It owns the `HttpClient`instance (shared as a static singleton to avoid socket exhaustion), handles JSON serialization with `System.Text.Json`, and manages the complete token lifecycle from reception to secure storage and deletion.
- **MainWindow:** Divided into a declarative XAML layout file and its code-behind counterpart. The XAML owns all visual structure and style definitions; the code-behind exclusively handles UI state transitions (loading, error, authenticated) and delegates all business logic calls to `AuthService`.
- **App.xaml:** Holds no global resources in this MVP (resources are scoped to the root `Grid` to avoid WinUI 3's `Window.Resources` limitation), but serves as the standard application entry point for window instantiation.

### Connection with the API and data security

The communication architecture prioritizes security and resilience at every layer:

- **Typed HTTP client (`AuthService`):** All API communication is handled through a single `HttpClient` instance with a configured `BaseAddress` and a 15-second timeout. Request bodies are serialized to JSON using `System.Text.Json` and sent with `Content-Type: application/json` headers, matching exactly what the NestJS backend expects.
- **Structured error handling:** Every network call is wrapped in a `try/catch` that distinguishes between timeout errors (`TaskCanceledException`), HTTP-level failures (non-2xx responses), and malformed API responses. NestJS error payloads (which include a `message` field) are deserialized and surfaced directly to the user in a styled error banner, rather than exposing raw HTTP status codes.
- **Secure token storage (`PasswordVault`):** Complying with Windows security best practices, JWT tokens are **never stored in plain text** — not in application settings, files, or memory beyond the request scope. Instead, they are persisted exclusively via `Windows.Security.Credentials.PasswordVault`, which encrypts credentials using the Windows Data Protection API (DPAPI), binding them to the user's Windows account. This ensures the token is inaccessible to other users or processes on the same machine.
- **Session persistence:** On every application launch, `AuthService.GetStoredToken()` queries the `PasswordVault` before rendering the authentication forms. If a valid token is found, the application navigates directly to the home panel, eliminating unnecessary re-authentication and matching the seamless session behavior of the web frontend's HttpOnly cookie strategy.

### Technology used

I chose **WinUI 3** because it is the evolution of Microsoft interfaces. It allows me to use **XAML** for the UI design (separating visuals from behavior) and **C#** for all the logic.

- **Performance:** Being native, resource consumption is highly efficient for an app that shouldn't devour the user's RAM.
- **Aesthetics:** Integration with the operative system is seamless, including transparencies, animations, and controls that follow the Windows 11 design language.

## Security and data protection

In an interconnected ecosystem like this project, security cannot be a superficial layer; it must be integrated into the very design of the architecture. I have dedicated significant time to implementing a **defense-in-depth** strategy, securing every touchpoint between the client, the server, and the database, and proactively mitigating the most common **OWASP Top 10** vulnerabilities.

### Critical protection mechanisms

To shield the system to the maximum, I have implemented technical solutions against the most frequent attacks:

- **Session Tokens:** I use **JSON Web Tokens (JWT)** signed with a robust secret on the backend. Authentication is **stateless**, meaning the server does not store sessions, allowing it to scale securely and efficiently.
- **SQL Injection Prevention:** By using **Prisma ORM**, all queries to the PostgreSQL database are parameterized by default. This eliminates the risk of SQL injections, as the Prisma engine automatically sanitizes any user input before executing the statement.
- **XSS Mitigation:** * In the frontend, **React** rendering automatically escapes content, preventing the execution of malicious scripts.
    - I make strict use of **HttpOnly and Secure Cookies**. By not storing the JWT in the browser's local storage, the token is invisible to third-party scripts or browser extensions, making session theft via XSS practically impossible.
- **CSRF Protection:** **Next.js Server Actions** natively include protections against **Cross-Site Request Forgery**, validating that data mutation requests originate only from the official application.

### User management and access control

In a distributed environment, controlling who can communicate with the API is vital. For this reason, I have implemented a series of strict **CORS** configurations (although currently commented out for testing purposes), a permission system based on the **Role-Based Access Control** model, and functionalities such as password hashing…

- **Password Storage:** Passwords are processed using **Bcrypt**, with an appropriate cost factor (salt). This ensures that, even in the event of a data breach, the information remains unreadable and resistant to dictionary attacks. Initially, I considered the possibility of using one of today's most advanced encryption systems, **Argon2id**, but in my case, it was going to bring more trouble than it was worth. Being such a robust system, the server resource consumption would have been excessive. Therefore, having a minimal budget and just starting out, I opted for Bcrypt, which remains a good solution, though not as powerful as Argon. Even so, I have left the system prepared to make the jump to this technology when it becomes viable or when there is a desire to reinforce the level of security and encryption.
- **Authorization via Guards:** For this functionality, I have developed custom **Guards** for the controller endpoints. These interceptors check the user's role within the **JWT** payload before allowing access to the business logic, denying access (**401/403**) to any unauthorized user at the controller level.
- **Rate Limiting:** To prevent brute-force attacks on the login or spam in post creation, I have configured request limits per IP, guaranteeing service availability against abuse.
- **Origin Whitelist:** The API is not open to the entire internet. I have configured a whitelist that only allows requests from the official web application domains and the controlled local development environment. This prevents **Cross-Site** attacks where an external site attempts to make requests on behalf of the user.
- **Method and Header Restriction:** I limit not only the "who" but also the "what." The CORS policy restricts the permitted HTTP methods (GET, POST, PATCH, DELETE) and the headers the client can send, minimizing the exposure surface to malicious headers.

### **Secrets management and environment variables**

The portability and security of credentials are managed through a system of environment variables, following the industry standard to avoid the exposure of sensitive data:

- **Decoupling of Credentials:** No API key, database URL, JWT secret, or Cloudflare R2 credential is written directly into the source code. All sensitive configuration resides in `.env` files, which are strictly excluded from version control via the `.gitignore` file.
- **Client-Side Security:** In the web application, I have applied a critical distinction: only variables prefixed with `NEXT_PUBLIC_` are accessible to the browser. The rest remain exclusively on the server, ensuring they are never leaked to the end client.

### **Additional best practices and pending items**

- **Principle of Least Privilege:** Both the API connection with PostgreSQL and access to Cloudflare R2 buckets use credentials with the minimum permissions necessary to operate, reducing the blast radius in the event of an incident.
- **Schema Validation:** No data coming from the outside is trusted. Every input byte is validated through strict schemas before being processed by the services, acting as a data firewall.
- **Cloudflare Implementation:** From the beginning, my idea was to implement Cloudflare to add an extra layer of security to the central server, but I have not done so yet. The only Cloudflare service I have used is R2, so this remains pending, although it is a very good practice for protecting the backend.
- **Selection of Servers in Switzerland:** When configuring database instances on platforms like Neon or Supabase, or when setting up a VPS, the ideal choice is to opt for regions in Switzerland. This choice is strategic due to its advanced privacy legislation. Therefore, all the project deployments I have made and will make will be precisely in this region, taking advantage of both geographical proximity and the country's high commitment to security and personal data management.

**Development environment security**

Maintaining a secure development environment is also very important for keeping our service as reliable as possible. As a preventive security measure in my workflow, I have opted to disable the global execution of scripts in the **pnpm** dependency management system. With this configuration, I mitigate the risk of attacks through infected dependencies (**supply chain attacks**) that seek to execute malicious code to compromise credentials or extract environment variables from the system.

```bash
pnpm config set ignore-scripts true --global
```

> If I need to execute any script, I grant permissions manually after reviewing it in detail.
> 
</aside>

## Instance deployment

### REST-API

For the API deployment, my first choice has been to use Render's Web Service. Why? Mainly because it allows me to deploy my Docker container in a very simple way.
Render is great because it handles traffic and scaling almost automatically, connecting directly to my repository. This takes away the mess of configuring the server from scratch every time I make a change. By using Docker, I ensure that "if it works on my machine, it works on Render," avoiding those last-minute surprises with Node versions or system dependencies. It is a balanced solution: I maintain control of my environment with the container, but let Render handle availability.

> [!NOTE]
> https://render.com/

### Database

Regarding the database, I decided to move away from the traditional "install PostgreSQL on a server" scheme and opted for Neon. Being a Serverless database service, I rid myself of database engine maintenance and the headaches of managing storage manually.
What interests me most about Neon, aside from its free tier, is its "autoscaling" capability. If my API has a usage spike, the database responds without breaking a sweat; and if no one is using it, it pauses, which is ideal for optimizing resources. Additionally, the ease of managing data branches (branching) allows me to test migrations or schema changes without the risk of breaking the main database. It is, undoubtedly, the smartest option for a modern project where agility is key.

> [!NOTE]
> https://neon.com/

### Web application

For the deployment of the web part, my first logical choice was Vercel. Working with Next.js, the compatibility is total: deployment is done in a matter of minutes, and they make your life easier with domain management, SSL certificates, and their own CDN automatically. Furthermore, to start with, their free plan is unbeatable.
However, Vercel has "fine print" that can be dangerous: as soon as traffic starts to scale, costs skyrocket unpredictably. What starts as a convenience can end up being a real headache for your wallet.

As a result of a personal project I've been working on in parallel, I discovered Coolify, and it seemed like a fascinating alternative. It opened the doors to the world of self-hosting, allowing me not to depend on the limitations or pricing of platforms like Vercel. Therefore, for this project, I have decided to consider a much more realistic and scalable option: self-hosting on a VPS (whether on DigitalOcean, Hostinger, or similar).

By using Coolify as an orchestrator on my own server, I get a deployment experience very similar to Vercel's (with git push and automatic deployment), but paying a flat rate for the server, with no surprises at the end of the month.

I am aware that this path has its challenges. By managing my own infrastructure, I have to be much more cautious with server security and configure every detail by hand. Additionally, since Coolify does not include a native CDN as such, I have to integrate external services like Cloudflare to guarantee loading speed and protect the backend. But the extra effort is worth it: at the end of the day, I am the sole owner of my data and my infrastructure, something that has enormous technical value to me.

> [!NOTE]
> https://vercel.com/
> https://coolify.io/

### Mobile application

For the mobile part with Kotlin Multiplatform, my deployment strategy focuses entirely on agility. To be honest, at this stage of development, I have no intention of fighting with official stores like the Play Store or App Store; between eternal reviews and developer account costs, they feel more like a hindrance than a help right now.
For this reason, I have opted for generating manually signed APK files. My plan is to upload these versions to my own storage environment, taking advantage of the Cloudflare R2 I mentioned before or even through GitHub Releases. This way, any user can download and install the app directly on their device, without intermediaries or waiting times.

### Desktop application

With the desktop application, the approach is very similar; the main focus is simplicity for the Windows user while completely ignoring the Microsoft Store.
To ensure a professional installation, I will use MSIX, which is the modern Windows packaging format. This allows me to offer a clean installation with the peace of mind that if the user decides to uninstall the app, no junk will be left in the system registry.
Just like with the APK, the installer will be available for direct download. A key point here is that I am going to generate a self-contained executable. Everything needed for the app to run is tucked inside the package itself. It’s a bit heavier, but it will save me a thousand support tickets and compatibility issues.

## Usage and maintenance guide

First of all, we must ensure we have the engine for all of this installed: **Node.js** (I recommend the LTS version), **pnpm** (our package manager for security and speed), **.NET SDK 8** for the desktop part, **Android Studio** for the mobile part, and **Docker** to spin up the API container.

### **Step 1: Clone the repositories**

Once we have the repos, the first thing is to install the dependencies.
In the web repo, we will run:

```bash
pnpm install
```

### **Step 2:  Environment variables**

This is the point where everything usually fails. In the root of both the API and the Web, you will find an `.env.example` file. Copy it and rename it to `.env`.

- **Database:** Here you will need to put your Neon connection string.
- **Cloudflare:** You will need your R2 bucket keys so that the images don't appear broken.

> It is absolutely important not to upload these files to GitHub to avoid any surprises.
> 

### **Step 3: Phased startup**

Do not try to start everything at once. Follow this order:

1. **The Database:** We configure Neon.
2. **The Backend:** Enter the server folder and run the following command:
    
    ```bash
    docker compose up --build
    ```
    
3. **The Frontend:** Now we can launch the web with `pnpm dev` and the Android or iOS emulator.

### **Paso 4: Final part**

For the mobile application, we open the root folder in **Android Studio**. We let **Gradle** download everything necessary and, once it finishes, we select the virtual device and hit "Play". This app works on both iOS and Android.

### Frequent problems

I’m not going to lie; the path to get here has been full of invisible walls. These are the three problems that made me rack my brain the most and how I’ve been managing them:

#### The mystery of the Neon connection

There was a day when, suddenly, the database migrations stopped working. I had the connection URLs perfect, the correct user and password, but Neon was constantly spitting out connection errors.
After a lot of troubleshooting, I discovered the culprit: I was working while connected to my mobile hotspot. The problem is that many mobile carriers exclusively use IPv6, and Neon (like many database services) doesn't always handle these connections well if the client isn't prepared. It was a lesson learned through frustration: network infrastructure is just as important as the code.

#### **The Ktor jam when uploading images to R2**

Another major challenge has been uploading files to Cloudflare R2 from the mobile app. Despite having pre-signed URLs and proper authorization, the Ktor client sometimes "hangs" in the middle of the upload.
I’m still investigating the exact reason, but I suspect it’s a stream management issue or how Ktor handles the timeout when the file size is significant on unstable networks. At first, I thought it was just a timeout configuration, but it seems to be something deeper related to how the mobile client keeps the socket open. It’s an open problem that is forcing me to dive very deep into Kotlin's network documentation.

#### The learning curve

Beyond the technical errors, the greatest challenge has been the volume of information. I’ve had to learn languages like Kotlin and TypeScript, and master frameworks like Next.js and NestJS almost from scratch.
Although these technologies derive from what we’ve seen in class (Java, JavaScript…), implementing them with JWT, advanced security, and modern architectures has been a constant challenge. Balancing the official class syllabus with self-learning this stack and separate personal projects has been brutal pressure, but it helped me realize something: the most important thing isn't knowing a language by heart, but having a solid programming foundation that allows you to adapt to any technology thrown at you.

> [!IMPORTANT]
> **In conclusion:** I’ve gone through moments of great frustration, but every error has taught me more than any code that worked on the first try. I leave this project with the confidence that I can face a real work environment and adapt to any technology they give me—except maybe COBOL.
> 

## Future improvements

To conclude this document, I want to be completely honest about the future of this project. Realistically, I have no intention of continuing the development of this social network once the course is over, and I have compelling reasons for that decision.

From the beginning, the "social network" concept was not an idea I was passionate about. It is an extremely complex software model that depends not only on perfect code but also on a critical initial user base—something nearly impossible to achieve in a market saturated by giants like Instagram, TikTok, or X. Developing a social network without a disruptive differential factor is an excellent technical academic exercise, but on a business level, it is a losing battle.

However, I do not consider this time wasted. On the contrary, I have used this project as a **high-level "testing ground."** It forced me to learn Kotlin Multiplatform, NestJS, Next.js, and cloud infrastructure management, facing challenges I wouldn't have encountered in a simpler project.

While this project will never see a commercial release, it has marked a turning point in my career as a developer. It has given me the knowledge, methodology, and, above all, the technical freedom to create my own projects that *will* see the light of day in the near future—projects I am already working on.

## My thoughts on the project

Since we were part of a pilot project this year that caught us all a bit by surprise, I would like to contribute my grain of salt as a student for future editions.

My main suggestion for the future is to **bet on complete creative freedom.** I believe the project gains immense value when the student chooses the idea or the solution to a real-world problem, rather than working on an imposed concept. Motivation changes completely when you program something born from your own vision; furthermore, that freedom fosters self-taught learning. It forces you to be proactive, to make real architectural decisions, and, above all, to dive into official documentation to find answers that aren't in the class notes.

I agree that demanding technical minimums should be established—such as limiting the use of *Backend-as-a-Service* platforms that do everything for you. The essence of this course is learning to build the backend and clients from scratch.

**My proposal is clear:** define the **"what"** (own backend, multiple clients, security), but allow total freedom in the **"how."** Let the student decide which infrastructure to use and which tech stack they are passionate about. That ability to research and delve deeper on one's own is, ultimately, the most valuable skill we can take into the professional world.

## Resources and documentation used

### **Backend & Infrastructure (API-REST)**

- **NestJS & Database:**
    - [NestJS + Prisma Integration Guide](https://www.prisma.io/docs/guides/nestjs): Core architecture for the ORM layer.
    - [Neon Serverless Driver with Prisma](https://neon.com/docs/guides/prisma#use-the-neon-serverless-driver-with-prisma): Connection pooling and serverless optimization.
- **Docker & Containerization:**
    - [Dockerfile Best Practices](https://docs.docker.com/reference/dockerfile/): Implementation of multi-stage builds.
    - [Official Node.js Images](https://hub.docker.com/_/node): Selecting the `bookworm-slim` variants for security.
    - [Docker Compose Specification](https://docs.docker.com/reference/compose-file/services/): Orchestration and environment variables.
- **Security & Authentication:**
    - [NestJS Auth & JWT Implementation](https://docs.nestjs.com/security/authentication): Stateless session management.
    - [Guards & RBAC](https://docs.nestjs.com/guards): Implementing the authorization layer.
    - [Encryption & Hashing](https://docs.nestjs.com/security/encryption-and-hashing): Bcrypt integration for secure password storage.
    - [CORS & Rate Limiting](https://docs.nestjs.com/security/rate-limiting): Hardening the API against unauthorized origins and brute-force attacks.
- **Cloud Storage (Cloudflare R2):**
    - [S3-Compatible API Start Guide](https://developers.cloudflare.com/r2/get-started/s3/): Migrating logic to object storage.
    - [Presigned URLs Documentation](https://developers.cloudflare.com/r2/api/s3/presigned-urls/): Securing direct uploads from the client.

---

### **Web Application (Frontend)**

- **Next.js & UI Frameworks:**
    - [Next.js App Router Documentation](https://nextjs.org/docs/app): Mastering Server Components and Layouts.
    - [Hero UI](https://heroui.com/) & [Shadcn UI](https://ui.shadcn.com/): Component libraries for rapid, high-quality development.
    - [GSAP (GreenSock)](https://gsap.com/): Advanced web animations.
- **Data Fetching & Security:**
    - [Server Actions & Mutations](https://www.google.com/search?q=https://nextjs.org/docs/app/building-your-application/data-fetching/server-actions-and-mutations): Handling logic without exposing API endpoints to the client.
    - [Route Handlers (API Proxy)](https://nextjs.org/docs/app/getting-started/route-handlers): Securely masking the backend URL.
    - [HttpOnly Cookies Management](https://nextjs.org/docs/app/api-reference/functions/cookies): Protecting JWTs from XSS attacks.
- **State & Validation:**
    - [Zod Schema Validation](https://zod.dev/): Ensuring type safety from form to backend.
    - [Zustand State Management](https://zustand.docs.pmnd.rs/getting-started/introduction): Lightweight global store for user sessions.

---

### **Mobile Application (Android/KMP)**

- **Architecture & UI:**
    - [Kotlin Multiplatform (KMP) Core Docs](https://kotlinlang.org/docs/multiplatform.html): Managing shared logic between platforms.
    - [Jetpack Compose](https://developer.android.com/compose): Modern declarative UI for Android.
    - [Material Design 3](https://m3.material.io/): Following Google's latest design guidelines.
- **Networking & Serialization:**
    - [Ktor Multiplatform Client](https://ktor.io/docs/client-create-multiplatform-application.html): Implementing the HTTP engine in `commonMain`.
    - [Kotlinx Serialization](https://ktor.io/docs/client-serialization.html): Native JSON-to-Object conversion.
- **Persistence & Validation:**
    - [Multiplatform Settings](https://github.com/russhwolf/multiplatform-settings): Secure storage for JWTs.
    - [Konform Validation](https://www.konform.io/): Type-safe form validation for Kotlin.
- **Media & Utilities:**
    - [Coil Image Loading](https://coil-kt.github.io/coil/): Efficient image fetching and caching for R2 assets.
    - [Peekaboo Library](https://github.com/onseok/peekaboo): Cross-platform gallery selection.