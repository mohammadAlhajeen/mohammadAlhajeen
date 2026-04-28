Hi, I'm Mohammad Alhajeen

Java Backend Engineer | Spring Boot · DDD | Building Real Systems

---

About Me

I’m a backend engineer focused on building scalable, production-ready systems, not just writing code.

- Strong in Domain-Driven Design (DDD)
-  Building systems with Spring Boot + PostgreSQL
-  Focused on performance, caching, and real-world constraints
-  Currently building a marketplace for the Arab world

---

 What I’m Building

 Kawn (كون)

A marketplace designed for real-world commerce challenges in the Arab region.

Key ideas behind it:

- Real-time inventory handling (Redis + Lua)
- Smart cart validation engine (Preview vs Reconcile)
- Flexible pricing & offers system
- Geospatial delivery pricing (PostGIS)
- Built with DDD modular architecture

---

 Engineering Mindset

I care about:

- Clean architecture over quick hacks
- Real-world constraints (not ideal scenarios)
- System design, not just endpoints
- Trade-offs and scalability

---

Tech Stack

Backend:

- Java
- Spring Boot
- Spring Security (JWT, OAuth2)

Database:

- PostgreSQL
- PostGIS

Caching & Performance:

- Redis
- Caffeine

Infrastructure:

- Docker
- Nginx

---

 Highlight Concepts I Work With

- Cart Validation Engine (self-healing carts)
- Snapshot-based checkout
- Soft reservation (Redis TTL)
- Domain events between bounded contexts
- Multi-layer caching strategies
- Media serving via Nginx + backend coordination

---

 Currently Learning / Exploring

- Virtual Threads (Java)
- GraalVM
- Advanced system design patterns

---

 Connect With Me

- LinkedIn: https://www.linkedin.com/in/mohamed-alhajeen
- Portfolio (coming soon…)

---

 Fun Fact

I don’t just build features —
I build systems that survive real users.
---

## Projects

### [Kawn â€” Multi-Vendor Marketplace](https://github.com/mohammadAlhajeen/bun_commerce-public)
Full-stack marketplace platform targeting the Palestinian and Arab market.  
- Cart validation engine (Preview/Reconcile cycle) for real-time price and stock conflict detection  
- Snapshot-based checkout with Redis Lua atomic soft reservations  
- Three-tier caching: Caffeine â†’ Redis â†’ PostgreSQL  
- Domain-driven design with clean aggregate boundaries across 10+ domains  
- Production deployment: Docker + Nginx on VPS (Ubuntu 24.04)

### [Authentication Service](https://github.com/mohammadAlhajeen/spring_jwt_Oauth2)
Dedicated identity and auth layer using OAuth2 + JWT.  
- Stateless JWT with custom claims (device_id, scope, public_id)  
- Magic Link (OTT) + Guest Checkout via phone number  
- Secure internal/public UUID mapping with caching

### [Multi-Role Order Management System](https://github.com/mohammadAlhajeen/spring-multi-user-auth-jwt)
Multi-role backend (Admin, Company, Customer, Driver) with full order lifecycle, RBAC, and role-based state transitions.

---

## Currently

- ًںژ“ B.Sc. Software Engineering â€” University of Palestine (Top of Specialization, 2026)
- ًں”¨ Shipping Kawn to production
- ًں“‌ Writing about Java, Spring Boot, and system design on [LinkedIn](https://linkedin.com/in/mohamed-alhajeen-832b6621a/)
