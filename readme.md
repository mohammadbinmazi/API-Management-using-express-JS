# Tea Management API using express js

## Overview

This is a simple REST API for managing a collection of teas. It allows users to:

- Add new teas
- Retrieve all teas
- Retrieve a specific tea by ID
- Update tea details
- Delete a tea

This project is built using Node.js and Express.

---

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory:

   ```bash
   cd tea-management-api
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Start the server:
   ```bash
   node index.js
   ```
   The server will start on `http://localhost:3000`.

---

## Endpoints

### 1. Add a New Tea

**POST** `/teas`

- **Request Body:**
  ```json
  {
    "name": "Green Tea",
    "price": 2.99
  }
  ```
- **Response:**
  ```json
  {
    "id": 1,
    "name": "Green Tea",
    "price": 2.99
  }
  ```

### 2. Get All Teas

**GET** `/teas`

- **Response:**
  ```json
  [
    {
      "id": 1,
      "name": "Green Tea",
      "price": 2.99
    },
    {
      "id": 2,
      "name": "Black Tea",
      "price": 3.99
    }
  ]
  ```

### 3. Get a Tea by ID

**GET** `/teas/:id`

- **Response:**
  ```json
  {
    "id": 1,
    "name": "Green Tea",
    "price": 2.99
  }
  ```
- **Error:**
  ```json
  "Tea not found"
  ```

### 4. Update a Tea

**PUT** `/teas/:id`

- **Request Body:**
  ```json
  {
    "name": "Updated Tea",
    "price": 4.99
  }
  ```
- **Response:**
  ```json
  {
    "id": 1,
    "name": "Updated Tea",
    "price": 4.99
  }
  ```
- **Error:**
  ```json
  "Tea not found"
  ```

### 5. Delete a Tea

**DELETE** `/teas/:id`

- **Response:**
  Status Code: `204 No Content`
- **Error:**
  ```json
  "Tea not found"
  ```

---

## Features

- Full CRUD operations for managing tea data.
- Express JSON middleware for handling request bodies.
- In-memory storage for tea data.

---

## Technologies Used

- **Node.js**: JavaScript runtime.
- **Express**: Web framework for Node.js.

---

## Future Improvements

- Add a database (e.g., MongoDB or MySQL) for persistent data storage.
- Implement authentication and authorization.
- Add unit tests for better reliability.

---

## Author

Developed by [mohammad bin mazi ].
guided by Hitesh chaudhary
