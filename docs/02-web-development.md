# Web Development Fundamentals

## Frontend Stack

### HTML5
- **Semantic Elements**: `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>`
- **Forms**: `<input>`, `<textarea>`, `<select>`, `<button>`
- **Accessibility**: ARIA labels, semantic HTML, alt text for images
- **Meta Tags**: Viewport, charset, description

### CSS3
- **Selectors**: Element, Class, ID, Attribute, Pseudo-classes, Pseudo-elements
- **Box Model**: Content → Padding → Border → Margin
- **Display**:
  - Block: Full width
  - Inline: Only needed width
  - Inline-block: Hybrid
  - Flexbox: One-dimensional layout
  - Grid: Two-dimensional layout
- **Responsive Design**: Media queries, Mobile-first approach
- **Modern Features**: CSS Variables, Animations, Transitions, Gradients

### JavaScript Fundamentals
- **Variables**: var (avoid), let, const
- **Data Types**: string, number, boolean, object, array, null, undefined
- **Functions**: Declaration, Expression, Arrow functions
- **Scope**: Global, Function, Block scope (let/const)
- **Closures**: Function with access to outer scope
- **Async**: Callbacks, Promises, async/await
- **DOM Manipulation**: Query selectors, Event listeners, CRUD operations

## Backend Fundamentals

### HTTP Protocol
- **Methods**: GET, POST, PUT, DELETE, PATCH
- **Status Codes**:
  - 2xx: Success (200, 201, 204)
  - 3xx: Redirection (301, 302, 304)
  - 4xx: Client Error (400, 401, 403, 404)
  - 5xx: Server Error (500, 502, 503)
- **Headers**: Content-Type, Authorization, CORS headers

### REST API Design
- **Principles**:
  - Resource-oriented: Think in nouns, not verbs
  - Stateless: Each request contains all needed info
  - Client-Server: Separation of concerns
  - Cacheable: Responses should define cacheability
- **Naming Conventions**:
  - Use nouns for endpoints: `/users`, `/posts`
  - Use verbs in methods: GET, POST, PUT, DELETE
  - Avoid: `/getUsers`, `/createUser`
- **Status Codes**:
  - POST (Create): 201 Created
  - GET (Read): 200 OK
  - PUT (Update): 200 OK or 204 No Content
  - DELETE (Delete): 204 No Content

### Databases

#### SQL (Relational)
- **ACID Properties**: Atomicity, Consistency, Isolation, Durability
- **Normalization**: 1NF, 2NF, 3NF (reduce redundancy)
- **Common Databases**: PostgreSQL, MySQL, SQLite

#### NoSQL (Non-relational)
- **Document**: MongoDB, CouchDB
- **Key-Value**: Redis, Memcached
- **Column-family**: HBase, Cassandra
- **Search**: Elasticsearch
- **Advantages**: Flexible schema, horizontal scalability

## Authentication & Security

### Authentication Methods
- **Session-based**: Server stores session, browser sends cookie
- **Token-based (JWT)**: Server generates token, client sends in header
- **OAuth2**: Third-party authentication

### Security Best Practices
- **HTTPS**: Always encrypt data in transit
- **Password**: Hash with bcrypt/Argon2, never plain text
- **CORS**: Control cross-origin requests
- **SQL Injection**: Use parameterized queries
- **XSS**: Sanitize user input
- **CSRF**: Use tokens to verify requests

## Popular Tech Stack Options

### MERN Stack
- **M**ongo: NoSQL database
- **E**xpress: Node.js framework
- **R**eact: Frontend library
- **N**ode.js: JavaScript runtime

### LAMP Stack
- **L**inux: Operating system
- **A**pache: Web server
- **M**ySQL: Database
- **P**HP: Programming language

### MEAN Stack
- **M**ongo: NoSQL database
- **E**xpress: Node.js framework
- **A**ngular: Frontend framework
- **N**ode.js: JavaScript runtime

---
**Last Updated**: 2026-04-05
