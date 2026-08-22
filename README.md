# Mohammad Alhajeen

**Backend Engineer** · Java · Spring Boot · PostgreSQL

I build and run production systems end to end: architecture, data modeling, deployment, and infrastructure.

Most of my work sits in transactional systems where correctness under concurrency matters more than feature count.

## What I work on

* Transactional workflows and concurrency
* Domain-Driven Design and modular architecture
* PostgreSQL data modeling, indexing, and query performance
* Authentication and identity infrastructure
* Caching strategies and read-model design
* Production deployment, CI/CD, and infrastructure

## Main projects

### Kawn: Multi-Vendor E-Commerce Marketplace

**[Live site](https://kawn.shop)** · **[Architecture docs](https://github.com/mohammadAlhajeen/bun_commerce-public)**

Built solo. Source private, architecture fully documented in the public repo.

A modular monolith of 15 domain modules exposing 215+ REST endpoints, with microservice-ready domain boundaries.

* Variant-first catalog with category-driven attribute inheritance over a hierarchical taxonomy (recursive CTEs), supporting tracked and on-demand inventory and faceted filtering without Cartesian-product explosion.
* Cart Preview/Reconcile engine that detects and repairs price drift and stock conflicts before checkout, feeding a snapshot-based checkout with an atomic reserve/consume/release/commit inventory protocol. The protocol is implemented as conditional single-statement updates guarded at the database, which prevents overselling without application-level locks or optimistic versioning. Order lifecycle modeled with domain events.
* Bilingual Arabic/English full-text search over PostgreSQL generated tsvector columns, GIN indexes, and ts_rank relevance ranking, behind one global endpoint returning products and stores from decoupled modules.
* One ProductCard read model reused across listing, search, collections, homepage, and store pages, hydrated through Caffeine with independent cache boundaries per read model and event-driven post-commit eviction.
* Plan-based subscriptions with upgrade, scheduled downgrade, renewal, grace period, automatic free-plan fallback, and pre-action quota enforcement.
* PostGIS geospatial addressing built from official government address data parsed into Flyway migrations, powering delivery routing and location-aware product discovery.
* Public-UUID to internal-ID identity mapping for multi-role auth, JWT with opaque refresh-token rotation, OAuth2 social login, optimistic locking, soft deletes, and role-segmented REST APIs.

**Testing:** integration-tested with Testcontainers against real PostgreSQL, running 101 concurrent reservations against 100 units of stock and asserting no oversell. Load-tested with JMeter using a weighted traffic mix over a seeded dataset of 7,200 products, 14,430 variants, and 122 stores: 1,100+ req/s at ~126 ms mean, p95 ~150 ms, zero errors.

**Deployment:** AWS EC2 behind a hardened Nginx and SSL reverse proxy on Ubuntu 24.04. GitHub Actions runs the test suite as a release gate, builds and publishes the Docker image to GHCR, then triggers deployment via AWS Systems Manager Run Command with Docker Compose. Production secrets stay on the host, so neither the image nor the pipeline carries credentials.

**Stack:** Java 21+ · Spring Boot · PostgreSQL · PostGIS · Caffeine · Flyway · Docker · Nginx · AWS

### Sooqna: Handmade Marketplace

**[Repo](https://github.com/mohammadAlhajeen/suqnna-public)**

Graduation project, University of Palestine. Built by a five-person Agile team under Dr. Sameh Abu Hassira. I led backend architecture, schema design, and production deployment.

* Wallet/escrow system with deposit-hold before order confirmation, supporting both full-payment and deposit-based pre-order flows with financial traceability through transaction logs.
* Two product types, in-stock and pre-order, each with its own lifecycle, inventory logic, and payment path, reflecting the variable timelines and limited quantities of artisan production.
* Multi-tenant backend supporting 100+ seller companies with strict data isolation enforced through company-scoped access patterns and service-level tenant boundaries. Each seller gets a public storefront with structured sections, custom slugs, and theme management.
* Schema design with JSONB attribute and shipping payloads and performance-oriented indexes on high-traffic queries. Arabic full-text search over tsvector and GIN.
* Functional and security testing with JUnit, Mockito, and Postman.

**Stack:** Java · Spring Boot · PostgreSQL · React.js · Docker · Nginx · AWS S3

### Bun Identity: Spring Boot Identity Starter

**[Repo](https://github.com/mohammadAlhajeen/bun-identity)**

Open source. An identity starter for teams that want to keep their auth layer in-house without adopting a heavy IAM product.

* JWT authentication with opaque refresh tokens stored as SHA-256 hashes and rotated on every use. Reuse detection revokes the user's entire token family and locks the account on replay.
* Device-aware sessions with typed revocation reasons, enabling per-device logout.
* OAuth2 social login and guest sessions.
* Caffeine-backed rate limiting on public endpoints.
* Architecture guardrail tests enforcing layering and keeping project-specific code out of the starter.
* Full documentation suite.

**Stack:** Spring Boot 4 · Java 21 · Spring Security · PostgreSQL · Flyway · Docker

## Tech stack

**Languages and backend:** Java 21+, SQL · Spring Boot, Spring Security, Spring Data JPA, Hibernate, Flyway

**Data:** PostgreSQL, PostGIS, MySQL · Caffeine

**Architecture and API:** Modular Monolith, Domain-Driven Design, Domain Events, Optimistic Locking · REST, JWT, OAuth2, Swagger/OpenAPI

**Testing:** JUnit, Mockito, Testcontainers, JMeter, Postman

**Ops and CI/CD:** Docker, Docker Compose, GitHub Actions, GHCR, AWS (EC2, Systems Manager), Nginx, Linux, VPS setup and security hardening

**Frontend familiarity:** React, Next.js, TypeScript

## Contact

* LinkedIn: [in/mohamed-alhajeen](https://linkedin.com/in/mohamed-alhajeen)
* Email: hajeen595@gmail.com
