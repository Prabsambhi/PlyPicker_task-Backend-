# Express JWT Authentication API

This is a simple Express.js API for user registration, authentication using JWT (JSON Web Tokens), and accessing protected routes with token verification.

## Features

- User registration
- User authentication (login)
- Token-based authentication using JWT
- Protected routes accessible only with a valid token

## Dependencies

- [express](https://www.npmjs.com/package/express): Fast, unopinionated, minimalist web framework for Node.js.
- [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken): An implementation of JSON Web Tokens.
- [body-parser](https://www.npmjs.com/package/body-parser): Node.js body parsing middleware.

# Express JWT Authentication API

This is a simple Express.js API for user registration, authentication using JWT (JSON Web Tokens), and accessing protected routes with token verification.

## Endpoints

### 1. User Registration

- **URL:** `POST /register`
- **Description:** Register a new user with a unique username and password.
- **Request Body:**
  ```json
  {
    "username": "example",
    "password": "password"
  }
- **Response:**
- **201** Created - User registered successfully.
- **400** Bad Request - Username already exists.

### 2. User Authentication (Login)

- **URL:** `POST /login`
- **Description:** Authenticate a user by providing their username and password.
- **Request Body:**
  ```json
  {
    "username": "example",
    "password": "password"
  }
- **Response:**
- **200** OK - Authentication successful. Returns a JWT token.
- **401** Unauthorized - Invalid username or password.

### 3. Get Dummy Data (Protected Route)

- **URL:** `GET /data`
- **Description:** Get dummy data. Accessible only with a valid JWT token.
- **Headers:** Authorization: Bearer <token>
- **Response:**
- **200** OK - Returns dummy data.
- **403** Forbidden - Token is required or invalid token.
