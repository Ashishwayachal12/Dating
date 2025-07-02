# 💘 MyDating - Spring Boot Dating Application

A simple Spring Boot-based dating platform that allows users to register their details, filter users by gender, and find best matches based on age and interests.

---

## 📦 Features

- User registration with basic details and interests
- Filter users by gender (MALE / FEMALE)
- Match users based on:
  - Age difference
  - Common interests
- RESTful API using Spring Boot + JPA + MySQL
- Enum support for gender
- Clean architecture with DAO, Service, Controller layers

---

## 🛠️ Tech Stack

- Java 17+
- Spring Boot
- Spring Data JPA
- MySQL
- Lombok
- Jackson (for JSON mapping)
- Maven

---

## 📁 Project Structure

com.mydating.dating
│
├── controller # REST Controllers
├── service # Business Logic
├── dao # Data Access Object
├── entity # JPA Entities
├── repository # Spring Data Repositories
├── dto # Data Transfer Objects (like MatchingUser)
├── util # Enum & Utility classes



---

## 🧪 API Endpoints

| Method | Endpoint                    | Description                      |
|--------|-----------------------------|----------------------------------|
| POST   | `/users`                    | Register a new user              |
| GET    | `/users/gender/male`        | Get all male users               |
| GET    | `/users/gender/female`      | Get all female users             |
| GET    | `/users/match?id=1&top=3`   | Get top 3 best matches for user with ID 1 |

---

## 📝 JSON Request Sample

```json
POST /users
Content-Type: application/json

{
  "name": "Ashish",
  "email": "ashish@gmail.com",
  "phone": 9876543210,
  "age": 25,
  "gender": "MALE",
  "intrests": ["Music", "Travel", "Cricket"]
}

