# BillSphere — Multi-Tenant SaaS Subscription & Billing Platform

A multi-tenant microservices platform for subscription management and usage-based billing modeled on how real SaaS companies (Stripe Billing, Chargebee, Razorpay) handle tenant isolation, metered usage, and automated invoicing at scale.


---

## Overview

Most billing systems look simple until you have to handle **multiple tenants sharing
infrastructure, usage-based pricing, failed payments, and automated invoice generation** all without one tenant's data or traffic ever leaking into another's. This project solves that.

Core problems tackled:
- **Tenant isolation** — every request is scoped to a tenant via JWT claims, enforced at the gateway and service level
- **Usage-based billing** — track per-tenant API usage and translate it into monthly invoices
- **Resilient payment collection** — Razorpay webhook handling with automated suspension on repeated failures
- **Centralized service coordination** — service discovery, config, and routing via Spring Cloud

---

## Tech Stack

| Category | Technology |
|---|---|
| Language | Java 17 |
| Framework | Spring Boot |
| Service Discovery | Netflix Eureka |
| API Gateway | Spring Cloud Gateway |
| Config Management | Spring Cloud Config Server |
| Inter-Service Comm | Feign Client |
| Messaging | Apache Kafka |
| Security | Spring Security, JWT |
| Caching / Rate Limiting | Redis (Token Bucket) |
| Batch Processing | Spring Batch |
| Payments | Razorpay (Webhooks) |
| Database | PostgreSQL |
| Containerization | Docker, Docker Compose |

---

## Key Features

- [ ] Multi-tenant architecture with JWT-based tenant isolation
- [ ] Tenant, Billing, and Notification microservices
- [ ] Eureka-based service discovery + Spring Cloud Gateway routing
- [ ] Feign Client + Kafka for inter-service communication
- [ ] Centralized configuration via Spring Cloud Config Server
- [ ] Per-tenant API rate limiting (Redis, Token Bucket algorithm)
- [ ] Spring Batch job for automated monthly invoice generation
- [ ] Razorpay webhook integration for payment collection
- [ ] Automated tenant suspension on repeated payment failure

---
