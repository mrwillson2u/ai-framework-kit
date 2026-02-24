# Data Model

> **Status:** Draft
> **Last Updated:** YYYY-MM-DD
> **Owner:** [Name]

---

## Overview

Summary of data architecture approach.

`[TODO]`

---

## Entity Relationship Diagram

```
[TODO: ASCII diagram or link to diagram file]

┌──────────────┐       ┌──────────────┐
│    User      │──────▶│    Order     │
│              │ 1:N   │              │
└──────────────┘       └──────────────┘
                              │
                              │ 1:N
                              ▼
                       ┌──────────────┐
                       │  OrderItem   │
                       │              │
                       └──────────────┘
```

---

## Entities

### Entity: User

| Field | Type | Constraints | Description |
|-------|------|-------------|-------------|
| id | UUID | PK | Unique identifier |
| email | string | unique, not null | |
| created_at | timestamp | not null | |
| updated_at | timestamp | not null | |
| `[TODO]` | | | |

**Relationships:**
- Has many `[TODO]`
- Belongs to `[TODO]`

**Indexes:**
- `[TODO]`

---

### Entity: [Name]

*(Copy template above for each entity)*

---

## Relationships Summary

| From | To | Type | Description |
|------|-----|------|-------------|
| User | Order | 1:N | User places many orders |
| `[TODO]` | | | |

---

## Enums / Lookup Tables

### [EnumName]

| Value | Description |
|-------|-------------|
| `[TODO]` | |

---

## Data Lifecycle

### Retention Policies

| Data Type | Retention Period | Reason |
|-----------|-----------------|--------|
| `[TODO]` | | |

### Archival Strategy

`[TODO]`

### Deletion / GDPR Compliance

`[TODO]`

---

## Database Choice

| Attribute | Value |
|-----------|-------|
| **Database** | `[TODO: PostgreSQL, MySQL, MongoDB, etc.]` |
| **Rationale** | *(see Decision Log #)* |
| **Hosting** | `[TODO]` |
| **Backup Strategy** | `[TODO]` |

---

## Migrations Strategy

`[TODO: tool, naming conventions, rollback approach]`

---

## Sample Queries

### [Query Name]

```sql
-- [Description]
SELECT * FROM users WHERE ...
```

---

## Open Questions

- `[TODO]`
