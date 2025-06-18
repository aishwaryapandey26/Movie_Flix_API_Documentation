# 🎬 MovieFlix API

Welcome to **MovieFlix API**, a powerful and developer-friendly RESTful API designed for a movie review platform. With MovieFlix, users can discover movies, submit reviews, and interact with a catalog of top-rated films.

> 📘 This project is built as a backend demonstration for REST API design, secure authentication using JWT, and clean documentation practices.

---

## 📁 Table of Contents

- [🚀 Features](#-features)
- [🛠️ Tech Stack](#️-tech-stack)
- [📦 Installation & Setup](#-installation--setup)
- [🔐 Authentication](#-authentication)
- [📡 API Endpoints Overview](#-api-endpoints-overview)
- [📄 Full API Documentation](#-full-api-documentation)
- [🧠 Project Purpose](#-project-purpose)
- [🧪 Testing the API](#-testing-the-api)
- [📎 License](#-license)

---

## 🚀 Features

✅ Browse Movies  
✅ Submit Movie Reviews  
✅ Like/Dislike Reviews  
✅ View Top Rated Content  
✅ JWT-based User Authentication  
✅ Filter/Search Movies  

---

## 🛠️ Tech Stack

- **Backend**: Node.js / Spring Boot (choose one as per your actual setup)  
- **Database**: MongoDB / PostgreSQL  
- **Authentication**: JWT (JSON Web Token)  
- **Hosting**: Render / Heroku / AWS  
- **Tools**: Postman for testing, GitHub for version control

---

## 📦 Installation & Setup

Follow these steps to run the project locally:

### Prerequisites
- Node.js / Java (depending on backend)
- npm / Maven
- MongoDB / PostgreSQL setup (or use a mock server)
- Postman (optional for testing)

### Steps
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/movieflix-api.git
   cd movieflix-api

2. **Install dependencies**
   - For Node.js:
     ```bash
     npm install
     ```
   - For Spring Boot:
     ```bash
     mvn install
     ```

3. **Run the project**
   - For Node.js:
     ```bash
     npm start
     ```
   - For Spring Boot:
     ```bash
     ./mvnw spring-boot:run
     ```

4. **Access the API**
   - Open your browser or use Postman to access the API:
     ```bash
     http://localhost:8080/api/v1/
     ```
   - Use JWT for authorization:
     ```bash
     Authorization: Bearer <your_token_here>
     ```

5. **Test the endpoint**
   - You can use `curl` to test the `/movies` endpoint:
     ```bash
     curl -X GET http://localhost:8080/api/v1/movies
     ```

---

## 🔐 Authentication

This API uses **JWT (JSON Web Token)** for user authentication. You will need to register a user and then log in to receive a JWT token.

### Steps for Authentication:

1. **Register a new user:**
   - Endpoint: `POST /api/v1/auth/register`
   - Request body:
     ```json
     {
       "username": "yourUsername",
       "email": "yourEmail@example.com",
       "password": "yourPassword"
     }
     ```

2. **Login to get the token:**
   - Endpoint: `POST /api/v1/auth/login`
   - Request body:
     ```json
     {
       "username": "yourUsername",
       "password": "yourPassword"
     }
     ```
   - Response (JWT Token):
     ```json
     {
       "token": "yourJWTtokenHere"
     }
     ```

3. **Use the token for authorization:**
   - Add the token to the `Authorization` header for subsequent API requests:
     ```bash
     Authorization: Bearer <your_token_here>
     ```

---

## 📡 API Endpoints Overview

Below is a summary of the main API endpoints available:

| HTTP Method | Endpoint                            | Description                                       |
|-------------|-------------------------------------|---------------------------------------------------|
| GET         | `/api/v1/movies`                    | Retrieve a list of movies                        |
| GET         | `/api/v1/movies/{id}`               | Retrieve detailed information about a specific movie |
| POST        | `/api/v1/reviews`                   | Submit a movie review                            |
| GET         | `/api/v1/reviews/{movieId}`         | View reviews for a specific movie                |
| POST        | `/api/v1/likes`                     | Like a review                                    |
| POST        | `/api/v1/dislikes`                  | Dislike a review                                 |

---

## 📄 Full API Documentation

For a detailed breakdown of each endpoint, including request and response formats, error codes, and example responses, please refer to the full API documentation at: 

**[Full API Documentation](http://localhost:8080/api-docs)**

---

## 🧠 Project Purpose

MovieFlix API is designed to demonstrate how to build a RESTful API using JWT authentication and clean code practices. It serves as a useful platform for learning how to implement CRUD operations, secure authentication, and interactive features like liking/disliking content.

---

## 🧪 Testing the API

You can test the API using tools like **Postman** or **curl**. Below are some examples:

1. **List movies:**
   ```bash
   curl -X GET http://localhost:8080/api/v1/movies

2.**Submit a movie review:** 
   ```bash
curl -X POST http://localhost:8080/api/v1/reviews -H "Authorization: Bearer <your_token_here>" -d '{"movieId": 1, "review": "Amazing movie!"}'
```

3.**Like a review:**
```bash
curl -X POST http://localhost:8080/api/v1/likes -H "Authorization: Bearer <your_token_here>" -d '{"reviewId": 123}'
```

## 📎 License

### Breakdown of Changes:
- **Authentication Section**: Explained the registration and login process, including token retrieval and usage.
- **API Endpoints Overview**: Provided a table with the HTTP methods and descriptions of endpoints.
- **Full API Documentation Link**: Added a placeholder for the full API documentation link.
- **Testing the API**: Added examples for how to test endpoints using `curl`.

This completes your README in a continuous and structured way, providing all the necessary details.
