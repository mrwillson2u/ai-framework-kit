# System Architecture

> **Status:** Draft
> **Last Updated:** YYYY-MM-DD
> **Owner:** [Name]

---

## Overview

High-level architecture summary.

`[TODO]`

---

## Architecture Diagram

```
[TODO: ASCII diagram or link to diagram file]

┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   Client    │────▶│   API       │────▶│  Database   │
│   (Web/App) │     │   Server    │     │             │
└─────────────┘     └─────────────┘     └─────────────┘
```

---

## Tech Stack

| Layer | Technology | Version | Rationale |
|-------|------------|---------|-----------|
| Frontend | `[TODO]` | | *(see Decision Log #)* |
| Backend | `[TODO]` | | |
| Database | `[TODO]` | | |
| Cache | `[TODO]` | | |
| Queue | `[TODO]` | | |
| Search | `[TODO]` | | |
| Auth | `[TODO]` | | |
| Hosting | `[TODO]` | | |
| CDN | `[TODO]` | | |
| CI/CD | `[TODO]` | | |
| Monitoring | `[TODO]` | | |

---

## Services / Components

### Service 1: [Name]

| Attribute | Value |
|-----------|-------|
| **Responsibility** | `[TODO]` |
| **Technology** | `[TODO]` |
| **Exposes** | `[TODO: API, events, etc.]` |
| **Consumes** | `[TODO]` |
| **Data Owned** | `[TODO]` |
| **Scaling Strategy** | `[TODO]` |

### Service 2: [Name]

*(Copy template above)*

---

## Data Flow

### Primary Flow: [Name]

```
[Source] → [Service A] → [Service B] → [Destination]
```

| Step | From | To | Data | Protocol |
|------|------|-----|------|----------|
| 1 | `[TODO]` | | | |

---

## Communication Patterns

| Pattern | Where Used | Notes |
|---------|------------|-------|
| REST API | `[TODO]` | |
| GraphQL | `[TODO]` | |
| WebSocket | `[TODO]` | |
| Event/Queue | `[TODO]` | |
| gRPC | `[TODO]` | |

---

## Non-Functional Requirements

### Scalability

| Metric | Current Target | Future Target |
|--------|---------------|---------------|
| Concurrent users | `[TODO]` | |
| Requests/sec | `[TODO]` | |
| Data volume | `[TODO]` | |

### Reliability

| Metric | Target |
|--------|--------|
| Uptime SLA | `[TODO]` |
| RTO (Recovery Time Objective) | `[TODO]` |
| RPO (Recovery Point Objective) | `[TODO]` |

### Security

| Requirement | Implementation |
|-------------|----------------|
| Authentication | `[TODO]` |
| Authorization | `[TODO]` |
| Data encryption (at rest) | `[TODO]` |
| Data encryption (in transit) | `[TODO]` |
| Secrets management | `[TODO]` |
| Audit logging | `[TODO]` |

### Observability

| Type | Tool | Notes |
|------|------|-------|
| Logging | `[TODO]` | |
| Metrics | `[TODO]` | |
| Tracing | `[TODO]` | |
| Alerting | `[TODO]` | |

---

## Infrastructure

### Hosting

| Environment | Provider | Region | Notes |
|-------------|----------|--------|-------|
| Development | `[TODO]` | | |
| Staging | `[TODO]` | | |
| Production | `[TODO]` | | |

### Infrastructure as Code

`[TODO: Terraform, Pulumi, CloudFormation, etc.]`

---

## Third-Party Dependencies

| Service | Purpose | Criticality | Fallback |
|---------|---------|-------------|----------|
| `[TODO]` | | | |

---

## Open Questions

- `[TODO]`
