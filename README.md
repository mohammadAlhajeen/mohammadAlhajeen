# Mohammad Alhajeen

**Backend Engineer** — focused on scalable backend systems, production-oriented architecture, and real-world transactional workflows.

I enjoy building systems that go beyond CRUD — focusing on consistency, domain modeling, backend architecture, and infrastructure-oriented engineering.

---

## What I Work On

* Scalable backend systems
* Domain-Driven Design (DDD)
* Authentication & identity infrastructure
* Transactional workflows & concurrency
* Consistency under real-world edge cases (price drift, stale data, race conditions)
* Caching strategies
* E-commerce architecture
* Production deployment & infrastructure

---

## Main Projects

### Kawn — Multi-Vendor E-Commerce Marketplace
**[Architecture docs →](https://github.com/mohammadAlhajeen/bun_commerce-public)** · *source private*

A production-oriented marketplace built solo — 215+ REST endpoints, 107K+ LOC — and deployed to production.

* modular monolith with microservice-ready domain boundaries
* variant-first catalog model (persists only purchasable variants — no Cartesian-product explosion)
* cart validation engine with price-drift and stock reconciliation
* snapshot-based checkout with atomic, database-level inventory reservation
* domain events for cross-domain consistency without tight coupling
* bilingual (Arabic / English) PostgreSQL full-text search
* standardized read model with a Caffeine cache and event-driven eviction
* delivery workflows and PostGIS geospatial addressing

**Tech:** Java · Spring Boot · PostgreSQL · PostGIS · Caffeine · Flyway · Docker · Nginx · React · Next.js

---

### Sooqna — Handmade Marketplace (Graduation Project)
**[Public repo →](https://github.com/mohammadAlhajeen/suqnna-public)**

A multi-tenant marketplace for the handmade economy, built with a five-person team — I led backend architecture and deployment.

* multi-tenant backend: 100+ seller companies with strict data isolation
* wallet / escrow with deposit-hold logic for pre-order flows
* in-stock and pre-order product types, each with its own lifecycle
* Arabic full-text search (tsvector + GIN) and JSONB attribute modeling
* load-validated with Apache JMeter at 300 concurrent users — search ~145 ms (p95 280 ms), order creation ~234 ms

**Tech:** Java · Spring Boot · PostgreSQL · React · Docker · Nginx · AWS S3

---

### Bun Identity — Spring Boot Identity Starter (Open Source)
**[Repo →](https://github.com/mohammadAlhajeen/bun-identity)**

An identity starter for developers who want full ownership of their auth layer without adopting a heavy IAM product.

* JWT authentication and OAuth2 login
* opaque refresh tokens with rotation
* guest sessions and device-aware flows
* UUID-based public / internal identity mapping
* rate limiting and a full documentation suite

**Tech:** Java · Spring Boot · Spring Security · PostgreSQL · Flyway · Docker

---

## Tech Stack

**Backend** — Java 21–25 · Spring Boot · Spring Security · Hibernate / JPA · Flyway
**Database & Infrastructure** — PostgreSQL · PostGIS · Caffeine · Redis · Docker · Nginx · Linux
**Architecture** — Domain-Driven Design · Modular Monolith · Domain Events · Transactional Modeling · Database-Level Inventory Reservation · Read-Model Caching
**Frontend** — React · Next.js · Tailwind CSS

---

## Philosophy

Backend engineering isn't about writing endpoints. It's about:

* designing correct systems
* understanding trade-offs
* handling real-world edge cases
* building maintainable architecture
* thinking beyond frameworks

---

## Connect

* **LinkedIn** — https://linkedin.com/in/mohamed-alhajeen
* **GitHub** — https://github.com/mohammadAlhajeen
* **Email** — hajeen595@gmail.com
