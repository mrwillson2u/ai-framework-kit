# API Contract

> **Status:** Draft
> **Last Updated:** YYYY-MM-DD
> **Owner:** [Name]

---

## Overview

Summary of API architecture and design principles.

`[TODO]`

**API Style:** `[TODO: REST, GraphQL, gRPC, etc.]`

**Base URL:** `[TODO: e.g., https://api.example.com/v1]`

---

## Authentication

| Method | Description |
|--------|-------------|
| `[TODO: Bearer token, API key, OAuth, etc.]` | |

### Auth Flow

```
[TODO: Describe auth flow or link to diagram]
```

---

## Common Headers

| Header | Required | Description |
|--------|----------|-------------|
| Authorization | Yes | Bearer token |
| Content-Type | Yes | application/json |
| X-Request-ID | No | Request tracing |
| `[TODO]` | | |

---

## Error Handling

### Error Response Format

```json
{
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Human readable message",
    "details": []
  }
}
```

### Standard Error Codes

| Code | HTTP Status | Description |
|------|-------------|-------------|
| VALIDATION_ERROR | 400 | Invalid input |
| UNAUTHORIZED | 401 | Auth required |
| FORBIDDEN | 403 | Insufficient permissions |
| NOT_FOUND | 404 | Resource not found |
| RATE_LIMITED | 429 | Too many requests |
| INTERNAL_ERROR | 500 | Server error |

---

## Rate Limiting

| Tier | Limit | Window |
|------|-------|--------|
| Default | `[TODO]` | per minute |
| Authenticated | `[TODO]` | per minute |

---

## Versioning Strategy

`[TODO: URL path (/v1/), header, query param]`

---

## Endpoints

### Resource: Users

#### GET /users

**Description:** List all users

**Query Parameters:**

| Param | Type | Required | Description |
|-------|------|----------|-------------|
| page | int | No | Page number (default: 1) |
| limit | int | No | Items per page (default: 20) |
| `[TODO]` | | | |

**Response:** `200 OK`

```json
{
  "data": [
    {
      "id": "uuid",
      "email": "user@example.com",
      "created_at": "2025-01-01T00:00:00Z"
    }
  ],
  "pagination": {
    "page": 1,
    "limit": 20,
    "total": 100
  }
}
```

---

#### GET /users/:id

**Description:** Get a single user

**Path Parameters:**

| Param | Type | Description |
|-------|------|-------------|
| id | UUID | User ID |

**Response:** `200 OK`

```json
{
  "id": "uuid",
  "email": "user@example.com",
  "created_at": "2025-01-01T00:00:00Z"
}
```

**Errors:**
- `404` — User not found

---

#### POST /users

**Description:** Create a new user

**Request Body:**

```json
{
  "email": "user@example.com",
  "password": "securepassword"
}
```

**Response:** `201 Created`

```json
{
  "id": "uuid",
  "email": "user@example.com",
  "created_at": "2025-01-01T00:00:00Z"
}
```

**Errors:**
- `400` — Validation error
- `409` — Email already exists

---

### Resource: [Name]

*(Copy endpoint templates above for each resource)*

---

## Webhooks

### Webhook: [Event Name]

**Trigger:** `[TODO]`

**Payload:**

```json
{
  "event": "user.created",
  "timestamp": "2025-01-01T00:00:00Z",
  "data": {}
}
```

**Retry Policy:** `[TODO]`

---

## SDK / Client Libraries

| Language | Link | Status |
|----------|------|--------|
| `[TODO]` | | |

---

## OpenAPI / Swagger

`[TODO: Link to spec file or note if not yet generated]`

---

## Open Questions

- `[TODO]`
