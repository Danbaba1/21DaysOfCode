# 21 Days of Code Challenge

Welcome to the 21 Days of Code Challenge! This repository contains my daily coding tasks for the challenge.

## Day 1: Getting Started with Express.js

### Task:
- Install Express.js using npm.
- Create a simple Express app with routes and middleware.
- Understand the basic structure of an Express application.

### Steps:
1. **Install Express.js**:
   - Run `npm install express` in your project directory to install Express.js.

2. **Create a Simple Express App**:
   - Create a new JavaScript file (e.g., `app.js`) in your project directory.
   - Import Express module and create an instance of Express.
   - Define routes and middleware functions.
   - Start the server to listen for incoming requests.

3. **Understand the Basic Structure**:
   - Express follows a middleware-based architecture.
   - Middleware functions are executed sequentially for each incoming request.
   - Routes are defined using HTTP methods and URL patterns.
   - Express applications have a modular structure, with routes, middleware, and other configurations separated into different files.

### Example Code:
```javascript
// app.js
const express = require('express');
const app = express();

// Middleware function
app.use((req, res, next) => {
  console.log('Middleware function');
  next();
});

// Route
app.get('/', (req, res) => {
  res.send('Hello, World!');
});

// Start server
const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
  console.log(`Server is running on port ${PORT}`);
});
