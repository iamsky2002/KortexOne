# KortexOne

> **A portfolio project built like a production, multi-tenant SaaS — using Java, Spring Boot, and React.**

A full-stack application where organizations manage their documents and team, with **secure multi-tenant access control**, **subscription billing**, and an integrated **AI document-Q&A** feature. Built end-to-end: Spring Boot REST backend, React + TypeScript frontend, PostgreSQL, and Docker.

![Status](https://img.shields.io/badge/status-under%20active%20development-orange)
![Java](https://img.shields.io/badge/Java-21-007396?logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5-6DB33F?logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-JWT%20%2B%20RBAC-6DB33F?logo=springsecurity&logoColor=white)
![React](https://img.shields.io/badge/React-TypeScript-61DAFB?logo=react&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-4169E1?logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?logo=docker&logoColor=white)

---

## 📌 Overview

**KortexOne** is a full-stack **Java + Spring Boot** application that demonstrates how a real multi-tenant SaaS product is engineered — from secure authentication and role-based access to subscription billing and a clean React frontend.

Each organization gets isolated data, role-based permissions (Admin / Member / Viewer), and a metered Free / Pro plan. Teams can upload documents and ask questions about them in plain language — answered by an AI layer that stays grounded in the uploaded content, with source citations.

> The focus is **solid backend engineering and full-stack delivery** — with payments and an AI feature integrated as part of a complete product.

---

## 🏗️ Engineering Highlights

What this project demonstrates as a **Java full-stack backend**:

- **Layered Spring Boot architecture** — Controller → Service → Repository, DTOs, clean separation of concerns
- **Spring Security** — stateless **JWT** authentication, **BCrypt** password hashing, method-level **RBAC** (`@PreAuthorize`)
- **Multi-tenancy** — shared-schema design with per-request tenant isolation (no organization can ever see another's data)
- **Spring Data JPA** — entity modeling, relationships, soft deletes, pagination
- **Payment integration** — **Razorpay** subscriptions with secure webhook handling (HMAC signature verification + idempotency) and invoice PDF generation
- **AI integration** — Spring AI + retrieval-augmented Q&A over uploaded documents (PostgreSQL `pgvector`), with citations
- **Production practices** — global exception handling (`@RestControllerAdvice`), structured MDC logging, OpenAPI/Swagger docs, **Testcontainers** integration tests
- **Containerized** — Docker + Docker Compose for backend, database, and frontend

---

## ✨ Features

- 🔐 **Auth & access control** — organization sign-up, JWT login, roles (Admin / Member / Viewer), team invites
- 🏢 **Multi-tenant isolation** — every organization's data is fully separated
- 📄 **Document management** — upload, list, and manage documents per organization
- 💳 **Subscription billing** — Razorpay-powered Free / Pro plans, usage quotas, downloadable invoices
- 📊 **Dashboard & audit log** — usage stats, team management, activity tracking
- 🤖 **AI document Q&A** — ask questions, get answers grounded in your documents with source citations

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Backend** | **Java 21 · Spring Boot 3.5 · Spring Security (JWT + RBAC) · Spring Data JPA** |
| **Frontend** | React · TypeScript · Tailwind CSS · Mantine · TanStack React Query |
| **Database** | PostgreSQL 16 (with `pgvector` extension for the AI feature) |
| **Payments** | Razorpay — subscriptions, webhooks, invoice PDFs |
| **AI layer** | Spring AI · Google Gemini · retrieval-augmented generation |
| **Testing & quality** | JUnit 5 · Mockito · Testcontainers · OpenAPI / Swagger · MDC logging |
| **Infrastructure** | Docker · Docker Compose · (deploy: AWS EC2 / Railway + Vercel) |

---

## 🗺️ Build Roadmap

Built lean and incremental — backend foundations first, then features.

| Phase | Focus |
|---|---|
| **0** | Project setup + cross-cutting (Docker, error handling, MDC logging, Swagger) |
| **1** | Multi-tenant auth + organizations + RBAC + React frontend base |
| **2** | Document management (storage abstraction) |
| **3** | AI document Q&A (Spring AI + pgvector + citations) |
| **4** | Payments — Razorpay subscriptions, webhooks, invoices, usage quotas |
| **5** | Dashboard, audit log, integration tests, deployment |

---

## 📌 Status

🚧 **Under active development.** This README will be expanded with a live demo, screenshots, architecture diagrams, and setup instructions as the project progresses.

---

*Built by [SKY](https://github.com/iamsky2002) as a portfolio project — a full-stack, multi-tenant SaaS focused on backend engineering with Java and Spring Boot, including payment and AI integration.*
