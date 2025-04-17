# 🎬 MovieFlix API

Welcome to the **MovieFlix API** — a RESTful API for a movie review platform, allowing users to explore movies, submit reviews, and discover top-rated content.
## 📌 Base URL

https://api.movieflix.com/v1
> Note: This is a placeholder. Replace with your own mock server or deployed endpoint if needed.

## 🔐 Authentication

Most endpoints are public, but **creating reviews, liking reviews, and submitting movies** require **JWT authentication**.

### 🛂 How to Authenticate

Send the JWT token in the `Authorization` header:

Authorization: Bearer <your_token_here>
## 🧭 Endpoints

### 1. 🎥 Get All Movies

**Endpoint:** `GET /movies`  
**Description:** Retrieve a list of all movies.

#### ✅ Response:

[ 
  { 
    "id": 101, 
    "title": "Inception", 
    "genre": "Sci-Fi", 
    "releaseYear": 2010, 
    "rating": 4.8 
  }, 
  { 
    "id": 102, 
    "title": "The Matrix", 
    "genre": "Sci-Fi", 
    "releaseYear": 1999, 
    "rating": 4.9 
  } 
]

## ⚠️ Error Handling

All failed requests will return standard error formats:

#### Sample Error Response:

{ 
  "error": "Invalid token or expired session" 
}

| Code | Meaning              |
|------|----------------------|
| 400  | Bad Request          |
| 401  | Unauthorized         |
| 404  | Not Found            |
| 500  | Internal Server Error |

## 📦 Tech Stack (Assumed Backend)
- **Backend:** Node.js / Spring Boot
- **Database:** MongoDB / PostgreSQL
- **Authentication:** JWT
- **Hosting:** Render / Heroku / AWS

## 🚀 Sample Usage

### Get Movies (cURL)

curl -X GET https://api.movieflix.com/v1/movies

### Submit Review (cURL)

curl -X POST https://api.movieflix.com/v1/reviews \
  -H "Authorization: Bearer <token>" \
  -H "Content-Type: application/json" \
  -d '{"movieId": 101, "rating": 5, "comment": "Amazing!"}'

## 📚 Summary

| Feature        | Supported |
|----------------|-----------|
| Browse Movies  | ✅        |
| Submit Reviews | ✅        |
| Get Top Rated  | ✅        |
| User Auth      | ✅        |
| Search & Filters | ✅      |

## 🧠 About the Project

MovieFlix API is part of a personal side project to demonstrate API design and documentation skills. This fictional API is designed to mimic real-world platforms like IMDb or Letterboxd and showcases best practices in RESTful API design and developer experience.

##📎 License

This project is licensed for educational and personal portfolio use only.
Not affiliated with or endorsed by IMDb, Letterboxd, or any real movie service.

## 📎 License

This project is licensed for educational and personal portfolio use only.
Not affiliated with or endorsed by IMDb, Letterboxd, or any real movie service.

