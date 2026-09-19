---
title: Express.js Fundamentals
tags: []
created: '2026-09-19'
source: VaultAgent
---
# Express.js Fundamentals

> Course notes from Express.js learning journey

## Core Concepts

### Creating an Express Application
```javascript
const express = require('express');
const app = express(); // Creates an Express application instance (server instance)
```

- `express()` is a **factory function** that returns a new Express application object
- This `app` object is the **main server instance** — it holds all middleware, routes, and configuration
- Think of it as the "brain" of your backend server

### Starting the Server
```javascript
const PORT = 3000;
app.listen(PORT, () => {
  console.log(`Server running on http://localhost:${PORT}`);
});
```

- `app.listen(port, callback)` **binds the server to a TCP port** and starts listening for incoming HTTP requests
- The callback runs once the server is successfully listening
- **Port** = a numbered communication endpoint (0–65535) that identifies a specific process/service on a machine
  - Common ports: 80 (HTTP), 443 (HTTPS), 3000/5000/8080 (dev servers)
  - Only one process can listen on a port at a time

---

## Request & Response Objects

### The Request Object (`req`)
```javascript
app.get('/users', (req, res) => {
  // req contains ALL incoming request data
});
```

| Property / Method | Purpose |
|-------------------|---------|
| `req.params` | Route parameters (e.g., `/users/:id` → `req.params.id`) |
| `req.query` | Query string parameters (e.g., `/search?q=express` → `req.query.q`) |
| `req.body` | **Parsed request body** (requires middleware: `express.json()` or `express.urlencoded()`) |
| `req.headers` | HTTP headers sent by client |
| `req.cookies` | Cookies (requires `cookie-parser` middleware) |
| `req.method` | HTTP method (GET, POST, PUT, DELETE, etc.) |
| `req.url` / `req.path` | Request URL / path |
| `req.ip` | Client IP address |

**Why `req`?** → To **access data sent from the frontend/client** — form inputs, JSON payloads, URL params, headers, auth tokens, etc.

### The Response Object (`res`)
```javascript
app.get('/users', (req, res) => {
  // res used to send data back to client
});
```

| Method | Purpose |
|--------|---------|
| `res.send(body)` | Sends response (string, Buffer, object, array) — auto-sets Content-Type |
| `res.json(obj)` | Sends JSON response (auto-sets `Content-Type: application/json`) |
| `res.status(code)` | Sets HTTP status code (chainable: `res.status(404).send('Not found')`) |
| `res.sendFile(path)` | Sends a file as attachment |
| `res.redirect(url)` | Redirects client to another URL |
| `res.cookie(name, val)` | Sets a cookie |
| `res.set(header, value)` | Sets response header |

**Why `res`?** → To **send data back to the frontend/client** — HTML, JSON, files, redirects, status codes, cookies.

---

## What is an API?

**API (Application Programming Interface)** = A contract/interface that defines how two software components communicate.

- **Client** (frontend, mobile app, another service) → makes requests
- **Server** (Express app) → processes requests, returns responses
- Communication typically over **HTTP/HTTPS** using **JSON** as data format

### Types of APIs

| Type | Description | Example |
|------|-------------|---------|
| **REST API** | Resource-based, stateless, uses HTTP verbs | GitHub API, Twitter API |
| **GraphQL API** | Query language, client specifies exact data shape | GitHub GraphQL, Shopify |
| **gRPC** | High-performance RPC using Protocol Buffers | Internal microservices |
| **WebSocket** | Full-duplex persistent connection | Real-time chat, live updates |
| **SOAP** | XML-based, strict contract (legacy enterprise) | Banking, legacy systems |

---

## What is a RESTful API?

**REST (Representational State Transfer)** = Architectural style for designing networked applications.

### Core Principles

| Principle | Meaning |
|-----------|---------|
| **Stateless** | Each request contains all info needed; server stores no client context between requests |
| **Resource-Based** | Everything is a **resource** (noun) identified by a URL — `/users`, `/posts/123` |
| **HTTP Verbs** | Actions map to HTTP methods: `GET` (read), `POST` (create), `PUT/PATCH` (update), `DELETE` (remove) |
| **Uniform Interface** | Consistent naming, standard status codes, predictable structure |
| **Cacheable** | Responses can be cached (via headers) to improve performance |
| **Layered System** | Client doesn't know if talking to origin server, proxy, load balancer, etc. |

### RESTful Route Conventions

| Action | HTTP Method | Endpoint | Description |
|--------|-------------|----------|-------------|
| List all | `GET` | `/users` | Retrieve collection |
| Get one | `GET` | `/users/:id` | Retrieve single resource |
| Create | `POST` | `/users` | Create new resource |
| Update (full) | `PUT` | `/users/:id` | Replace entire resource |
| Update (partial) | `PATCH` | `/users/:id` | Partially update resource |
| Delete | `DELETE` | `/users/:id` | Remove resource |

### Example: RESTful User Routes
```javascript
// GET    /users          → List all users
// GET    /users/:id      → Get user by ID
// POST   /users          → Create new user
// PUT    /users/:id      → Replace user
// PATCH  /users/:id      → Partial update
// DELETE /users/:id      → Delete user

app.get('/users', (req, res) => { /* ... */ });
app.get('/users/:id', (req, res) => { /* ... */ });
app.post('/users', express.json(), (req, res) => { /* ... */ });
app.put('/users/:id', express.json(), (req, res) => { /* ... */ });
app.patch('/users/:id', express.json(), (req, res) => { /* ... */ });
app.delete('/users/:id', (req, res) => { /* ... */ });
```

---

## Common Corrections / Clarifications

> **Your understanding was mostly correct!** Here are minor refinements:

| Your Statement | Clarification |
|----------------|---------------|
| "`app=express()` creates a server instance" | ✅ Correct — creates the **Express application instance** (which *is* the server) |
| "`app.listen` starts the server" | ✅ Correct — binds to port and begins accepting connections |
| "`req` used to access data sent from frontend" | ✅ Correct — `req.body`, `req.params`, `req.query`, `req.headers` |
| "`res` used to send data to frontend" | ✅ Correct — `res.json()`, `res.send()`, `res.status()`, etc. |
| "What is API, types of API, what is RESTful API" | ✅ Covered above with definitions and comparison table |

---

## Related Notes (Wikilinks)

- [[Express-JS-Course/Middleware]] — Understanding `express.json()`, `express.urlencoded()`, custom middleware
- [[Express-JS-Course/Routing]] — Route handlers, route parameters, modular routers
- [[Express-JS-Course/Error-Handling]] — Centralized error handling, error middleware
- [[Express-JS-Course/REST-API-Design]] — Deeper dive into REST best practices, versioning, pagination

---

## Next Topics to Explore

- [ ] Middleware (built-in, third-party, custom)
- [ ] Routing & Router modularization
- [ ] Request validation (Zod, Joi, express-validator)
- [ ] Error handling patterns
- [ ] Environment configuration (dotenv)
- [ ] Database integration (MongoDB/Mongoose, PostgreSQL/Prisma)
- [ ] Authentication & Authorization (JWT, sessions)
- [ ] Testing (Jest, Supertest)
