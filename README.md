<!-- HEADER SECTION -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=26&pause=1100&color=4F9EFF&center=true&vCenter=true&width=720&lines=Hi%2C+I'm+Rasid+Raja+Khan;Java+Backend+Developer;Spring+Boot+%7C+REST+APIs+%7C+Clean+Code;Focused+on+Practical+Backend+Skills" alt="Typing Intro" />
</p>

<h1 align="center">👨‍💻 Java Backend Developer</h1>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=khanrasidraja&style=flat-square&color=0F6CBD" alt="Profile Views" />
  <img src="https://img.shields.io/badge/Focus-Backend%20APIs-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Practice-DSA-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/Learning-Testing%20Patterns-success?style=flat-square" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/wave.svg" width="100%" alt="Divider" />
</p>

<p align="center">
  I build clean, testable, containerized backend services with Spring Boot, secure APIs with JWT, and work with both SQL & NoSQL storage.
</p>

---

### 🔧 Core Tech (Practical Focus)

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,spring,mysql,mongodb,docker,git,linux,maven,postman" alt="Tech Icons" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Spring%20Boot-REST%20%7C%20Validation%20%7C%20JPA-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Improving-Testing%20%7C%20Design%20Patterns-yellow?style=flat-square" />
</p>

---

### 🧩 What I Build (Abstracted Modules)

| Module | Purpose | Stack | Notes |
|--------|---------|-------|-------|
| Auth & Users | Register/Login + Roles | Spring Boot, JWT | Stateless endpoints |
| Quiz / Assessment | Attempt tracking + scoring | REST + MongoDB | Basic concurrency |
| Inventory CRUD APIs | Stock adjustments | Spring Data JPA + MySQL | Indexed queries |
| Core Data Layer | Repositories + DTO mapping | JPA / MongoTemplate | Separation of concerns |
| Deployable Service | Portable backend | Docker + EC2 | External config |
| Testing Basics | Service + Controller | JUnit | Expanding coverage |

---

### 🧠 Strength Areas
- REST API structure (CRUD, pagination, validation, DTO separation)
- Basic JWT authentication (access token, protected routes)
- Relational modeling + indexing (MySQL)
- Document modeling (MongoDB)
- Containerization (Docker)
- Layered architecture (Controller → Service → Repository)
- Structured error & logging patterns
- Consistent problem-solving (LeetCode & GFG)

---

### 🔐 Simple Auth Flow

```mermaid
sequenceDiagram
  autonumber
  participant C as Client
  participant A as Auth API
  participant DB as User Store
  C->>A: POST /auth/login
  A->>DB: Verify credentials
  DB-->>A: User record
  A-->>C: JWT token
  C->>A: GET /secure (Bearer token)
  A->>A: Validate token (signature, expiry)
  A-->>C: Protected response
```

---

### 🗂 Folder Pattern

```text
src/
 ├─ controller/    # REST endpoints
 ├─ service/       # Business logic
 ├─ repository/    # Data access
 ├─ dto/           # Request/Response models
 ├─ model/         # Entities/Documents
 ├─ config/        # Basic security & settings
 └─ exception/     # Global handlers
```

---

### 🧩 Component Overview

```mermaid
flowchart LR
Client --> API[Controllers]
API --> VAL[Validation]
API --> SRV[Services]
SRV --> SEC[JWT Filter]
SRV --> REPO[(Repositories)]
REPO --> DB[(MySQL / MongoDB)]
SRV --> LOG[(Logging)]
```

---

### ⚙️ Dev Flow

```mermaid
flowchart LR
Edit[IntelliJ] --> Build[Maven]
Build --> Test[JUnit]
Test --> Docker[Build Image]
Docker --> LocalRun[Local Container]
LocalRun --> GitPush[Git Push]
GitPush --> Repo[GitHub]
```

---

### 📊 Visual Stats

<p align="center">
  <!-- If this fails to load, open directly in browser -->
  <img src="https://github-readme-stats.vercel.app/api?username=khanrasidraja&show_icons=true&hide_rank=true&theme=tokyonight&cache_seconds=7200" width="46%" alt="Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=khanrasidraja&layout=compact&theme=tokyonight&cache_seconds=7200" width="46%" alt="Top Langs" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=khanrasidraja&theme=tokyonight" width="60%" alt="Streak" />
</p>

<p align="center">
  <!-- Activity graph (may fail sometimes). Fallback: comment out if blank -->
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=khanrasidraja&theme=tokyo-night" width="96%" alt="Activity Graph" />
</p>

<!-- Snake graphic will only show after workflow below is added -->
<p align="center">
  <img src="https://raw.githubusercontent.com/khanrasidraja/khanrasidraja/output/github-contribution-grid-snake.svg" alt="Contribution Snake Animation (requires workflow)" />
</p>

---

### 📊 Skill Progress (Illustrative)

| Skill | Progress |
|-------|----------|
| Java Core/OOP | ████████████▓▒░ |
| Spring Boot | ███████████▓▒░░ |
| REST API Design | ██████████▓▒░░ |
| MySQL | █████████▓▒░░░ |
| MongoDB | ████████▓▒░░░ |
| Docker | ████████▓▒░░░ |
| Testing (JUnit) | ███████▓▒░░░░ |

---

### 🎯 Current Goals
- Better test coverage (service + controller)
- Cleaner DTO mapping conventions
- Consistent exception + validation responses
- Better schema planning before coding

<details>
<summary><b>Example Error Response Pattern</b></summary>

```json
{
  "timestamp": "2025-09-09T10:12:45Z",
  "path": "/api/products",
  "errors": [
    {"field": "name", "message": "must not be blank"},
    {"field": "price", "message": "must be greater than 0"}
  ]
}
```
</details>

<details>
<summary><b>JWT Filter Snippet</b></summary>

```java
String auth = request.getHeader("Authorization");
if (auth != null && auth.startsWith("Bearer ")) {
   String token = auth.substring(7);
   if (jwtService.valid(token)) {
      UsernamePasswordAuthenticationToken authObj =
          new UsernamePasswordAuthenticationToken(userDetails, null, userDetails.getAuthorities());
      SecurityContextHolder.getContext().setAuthentication(authObj);
   }
}
chain.doFilter(request, response);
```
</details>

---

### 🧭 Short-Term Learning Plan

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title Next 6 Weeks
    section API Quality
    Unified Error Handling :2025-09-05, 7d
    Consistent Validation  :2025-09-12, 6d
    section Testing
    Service Layer Tests    :2025-09-18, 8d
    Controller Tests       :2025-09-26, 8d
    section Deployment
    Multi-Env Docker Setup :2025-10-04, 6d
```

---

### 🤝 Connect

<p align="center">
  <a href="https://www.linkedin.com/in/rashid-r-k-6b6aa5173/"><img src="https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin" /></a>
  <a href="https://leetcode.com/u/RasidKhan123/"><img src="https://img.shields.io/badge/LeetCode-Profile-orange?style=for-the-badge&logo=leetcode" /></a>
  <a href="mailto:khanrasidraja@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-red?style=for-the-badge&logo=gmail" /></a>
  <a href="https://github.com/khanrasidraja"><img src="https://img.shields.io/badge/GitHub-Repos-black?style=for-the-badge&logo=github" /></a>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png" width="100%" alt="Footer Divider" />
</p>

<p align="center"><i>Focused on solid, practical backend fundamentals.</i></p>
