# Mohammad Alhajeen â€” Backend Engineer

Backend engineer focused on designing production-grade, scalable systems with strong consistency guarantees.

Currently building **[Kawn](https://github.com/mohammadAlhajeen/bun_commerce-public)** â€” a full-stack multi-vendor e-commerce marketplace for the Arab market.  
Solo developer آ· 215+ REST endpoints آ· 107K+ lines of code آ· Live on VPS

---

## Tech Stack

**Backend** آ· Java 21 آ· Spring Boot آ· Spring Security 6 آ· Hibernate آ· Flyway  
**Database** آ· PostgreSQL آ· PostGIS آ· Redis آ· Caffeine  
**Architecture** آ· DDD آ· Modular Monolith آ· Domain Events آ· Soft Reservation Pattern  
**Auth** آ· JWT آ· OAuth2 آ· Magic Link (OTT)  
**Frontend** آ· React آ· Next.js آ· Tailwind CSS آ· RTL Arabic  
**DevOps** آ· Docker آ· Nginx آ· Linux آ· VPS

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
