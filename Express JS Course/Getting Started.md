---
title: Getting Started with Express.js
tags: []
created: '2026-09-19'
source: VaultAgent
---
# Getting Started with Express.js

## Importing Express

```javascript
// CommonJS (require)
const express = require('express');
const app = express();

// ES Modules (import)
import express from 'express';
const app = express();
```

## Starting the Server

```javascript
const PORT = 3000;

app.listen(PORT, () => {
  console.log(`Server running on http://localhost:${PORT}`);
});
```

## Defining Routes with `app.get()`

```javascript
// Basic route
app.get('/', (req, res) => {
  res.send('Hello World!');
});

// Route with parameters
app.get('/user/:id', (req, res) => {
  res.send(`User ID: ${req.params.id}`);
});
```

## Sending Responses with `res.send()`

```javascript
app.get('/', (req, res) => {
  // Sends a string (sets Content-Type to text/html)
  res.send('Hello World!');
  
  // Sends JSON (sets Content-Type to application/json)
  res.send({ message: 'Hello World!' });
  
  // Sends a Buffer
  res.send(Buffer.from('Hello World!'));
});
```

## Complete Minimal Example

```javascript
const express = require('express');
const app = express();
const PORT = 3000;

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.listen(PORT, () => {
  console.log(`Server running on http://localhost:${PORT}`);
});
```

## Key Points

- **`require('express')`** / **`import express`** — loads the Express module
- **`express()`** — creates an Express application instance
- **`app.get(path, callback)`** — defines a route handler for HTTP GET requests
- **`res.send(data)`** — sends HTTP response (auto-sets Content-Type)
- **`app.listen(port, callback)`** — starts the server on specified port

---

*Related: [[Express JS Course/Index]]*
