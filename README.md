<div align="center">

# Amar Kajević

### Full-Stack Software Engineer

**TypeScript · React · Next.js · Node.js · NestJS**

I design and build production-grade web platforms, event-driven backends and distributed systems — from pixel-perfect frontends to the infrastructure running underneath them.

5+ years of professional experience across frontend and backend engineering, with a focus on the TypeScript ecosystem, distributed architecture, and systems built to survive real-world failure modes — not just demos.

[![Email](https://img.shields.io/badge/Email-kajevic18%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:kajevic18@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Amar%20Kajevic-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/amar-k-0341a81b0/)
[![Portfolio](https://img.shields.io/badge/Portfolio-amar--kajevic.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white)](https://amar-kajevic.vercel.app/)

</div>

---

## What I Build

| Frontend | Backend | Architecture | Data & Messaging | Infrastructure |
|---|---|---|---|---|
| React | Node.js | Microservices | PostgreSQL | Docker |
| Next.js | Express | Event-Driven Design | MongoDB | AWS |
| TypeScript | NestJS | REST APIs | Redis | CI/CD |
| Angular | FastAPI | Distributed Systems | Kafka · RabbitMQ | GitHub Actions |

---

## Featured Work

### 📬 Notifications Platform — Event-Driven Notification Infrastructure

A multi-tenant notification delivery system built to demonstrate *operating* an event-driven architecture correctly — not just wiring brokers together.

**Architecture:** `NestJS Gateway` → `Transactional Outbox` → `Outbox Relay` → `Kafka` → `Email / Webhook Workers`

- Transactional outbox pattern: every notification request writes its row and outbox event in a single DB transaction, so the gateway never publishes directly on the request path and never loses events to a crash mid-flight
- Outbox relay claims batches safely across multiple replicas with `FOR UPDATE SKIP LOCKED`, publishing to Kafka without double-delivery
- Partitioned, replayable, per-key-ordered Kafka topics supporting independent consumer groups per channel
- Automatic retry tracking with attempt counts and failure reasons per event
- Nx monorepo with isolated, independently buildable packages (`gateway`, `libs/kafka`, `libs/contracts`, `libs/database`) so new workers plug in without duplicating logic
- Designed for Kubernetes + KEDA autoscaling and Prometheus/Grafana observability as the system grows

**Stack:** NestJS · TypeScript · Kafka · PostgreSQL (Supabase) · Prisma · Nx · Docker

**[→ View Repository](https://github.com/AmarKajevic/Notifications-Platform)**

<br>

### 🛒 Vendora — Multi-Vendor E-Commerce Platform

A production-oriented marketplace built around multiple user portals, ten backend services and event-driven processing.

**Architecture:** `Nx + pnpm Monorepo` → `API Gateway` → `10 Domain Services` → `MongoDB / Redis / Kafka`

- Customer, seller and admin portals
- Event-driven analytics with Kafka
- TensorFlow.js-powered product recommendations
- Redis-backed application state
- Stripe payments with automated seller onboarding
- Real-time communication with Socket.IO
- JWT + OTP authentication with refresh tokens
- ImageKit media management
- Dockerized services, GitHub Actions + Docker Hub CI/CD

**Stack:** Next.js · React · TypeScript · Node.js · Express · Kafka · Redis · MongoDB · Prisma · Stripe · TensorFlow.js · Socket.IO · Docker

**[→ View Repository](https://github.com/AmarKajevic/Vendora-Multi-vendor-ecommerce-platform)**

<br>

### 💬 Chatty — Real-Time Communication Platform

A real-time communication system focused on WebSockets, presence management, notifications and multi-session users.

**Architecture:** `React` → `Node.js / Express` → `MongoDB + Redis` (↘ `Socket.IO`, ↘ `Google AI`)

- Real-time messaging with Socket.IO
- Multi-session presence tracking with Redis Sets
- JWT authentication with HTTP-only cookies
- Friend system and Connect Codes
- Real-time notifications, typing indicators, read receipts
- Google AI assistant
- Dockerized development environment · live production deployment

**Stack:** React · TypeScript · Node.js · Express · Socket.IO · Redis · MongoDB · JWT · Google AI · Docker

**[→ View Repository](https://github.com/AmarKajevic/Chat-app-socket.io-)** · **[→ Live Demo](https://chatty-ai-app.onrender.com/)**

<br>

### 📄 DocAI — Multi-Tenant AI Document Analysis SaaS

A multi-tenant SaaS where every organization is an isolated workspace, with server-enforced authorization at every layer — never trusting client-supplied identity.

**Architecture:** `Clerk (Auth + Orgs)` → `Next.js 16 App Router` → `Prisma / PostgreSQL` (↘ `Google Gemini`, ↘ `Vercel Blob`)

- Multi-tenant organization workspaces with role-based access (owner/member)
- Server-side membership verification on every API route
- Multi-format document analysis: text, PDF, Word, Markdown
- AI-powered summaries, Q&A, sentiment analysis and structured extraction via Gemini
- Signature-verified Clerk ⇄ Postgres webhook sync
- Authenticated file downloads — no public file exposure
- Monthly usage quotas enforced server-side
- Unit tests (Vitest) + E2E tests (Playwright) + GitHub Actions CI

**Stack:** Next.js 16 · TypeScript · Prisma · PostgreSQL · Clerk · Google Gemini · Vercel Blob · Vitest · Playwright

**[→ View Repository](https://github.com/AmarKajevic/Multi-Tenant-AI-Document-Analysis)** · **[→ Live Demo](https://multi-tenat-ai-saas.vercel.app/)**

---

## Engineering Snapshot

| | |
|---|---|
| **5+ years** | Professional software engineering |
| **10 backend services** | Powering Vendora's marketplace architecture |
| **10k+ records/hour** | Kafka-based supplier sync pipeline (enterprise e-commerce role) |
| **~40% faster APIs** | Redis caching optimization (production systems) |
| **Transactional outbox + Kafka** | Event delivery with zero-loss guarantees (Notifications Platform) |
| **Microservices** | Distributed backend architectures |
| **Cloud & DevOps** | Docker + AWS + CI/CD |

---

## How I Think

I enjoy the engineering problems behind the product.

- **Scalability** — knowing when a simple solution is enough, and when it isn't
- **Architecture** — breaking complex systems into clear, maintainable boundaries
- **Reliability** — outbox patterns, idempotency, retries and failure modes handled on purpose, not by accident
- **Performance** — caching, database optimization and efficient API design
- **User Experience** — building interfaces that feel as good as the systems behind them

---

## Core Stack

| Category | Technologies |
|---|---|
| **Frontend** | TypeScript · React · Next.js · Angular · TailwindCSS |
| **Backend** | Node.js · Express · NestJS · FastAPI · .NET |
| **Architecture** | Microservices · Event-Driven Architecture · REST · Distributed Systems |
| **Data** | PostgreSQL · MySQL · MongoDB · Redis |
| **Messaging** | Kafka · RabbitMQ |
| **Tools** | Prisma · Docker · AWS · CI/CD · GitHub Actions |
| **Security & Integrations** | JWT · OAuth2 · Google Authentication · Stripe · Third-Party APIs |

---

<div align="center">

### Let's Connect

🌍 Open to remote opportunities

[![Email](https://img.shields.io/badge/Email-kajevic18%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:kajevic18@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Amar%20Kajevic-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/amar-k-0341a81b0/)
[![Portfolio](https://img.shields.io/badge/Portfolio-amar--kajevic.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white)](https://amar-kajevic.vercel.app/)

</div>
