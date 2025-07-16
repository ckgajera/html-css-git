# 📘 Blog Application - Full Stack (Spring Boot + React)

A full-stack blog application built using **Spring Boot**, **React.js**, **MySQL**, **JWT Authentication**, and **Tailwind CSS**.

---

## 📁 Tech Stack

| Layer        | Technology                     |
|--------------|--------------------------------|
| Frontend     | React.js, Axios, Tailwind CSS  |
| Backend      | Java, Spring Boot (3.5.3), Spring Security |
| Database     | MySQL                          |
| Auth         | JWT (JSON Web Token)           |
| API Docs     | Swagger (Springdoc OpenAPI)    |
| Validation   | Hibernate Validator             |

---

## 🔧 Features

- ✅ User Registration & Login
- ✅ Role-based Authorization (`USER` / `ADMIN`)
- ✅ CRUD Operations for Posts
- ✅ Comment on Posts
- ✅ Delete User and Cascade Delete Posts + Comments
- ✅ Responsive UI using Tailwind CSS
- ✅ Swagger API Documentation

---

## 🗂️ Project Structure

### Backend (Spring Boot)
```
/src/main/java/com/backend/blogapp
├── config
│   └── SecurityConfig.java, SwaggerConfig.java
├── controller
│   └── AuthController.java, PostController.java, CommentController.java
├── dto
├── entity
├── repository
├── service
│   ├── impl
│   └── interfaces
└── exception
```

### Frontend (React)
```
/src
├── components
│   ├── Navbar.jsx
│   ├── PostList.jsx
│   ├── PostDetail.jsx
│   └── CommentSection.jsx
├── pages
│   ├── Login.jsx
│   ├── Register.jsx
│   └── Home.jsx
├── App.js
├── index.js
└── index.css (Tailwind)
```

---

## 🚀 Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/blog-application.git
cd blog-application
```

---

## ⚙️ Backend Setup

### 📌 Prerequisites
- Java 17+
- Maven
- MySQL Server

### 📦 Install & Run
```bash
cd backend
mvn clean install
```

### ▶️ Run Spring Boot
```bash
./mvnw spring-boot:run
```

### 🌐 Swagger UI
```
http://localhost:8080/swagger-ui/index.html
```

### 📁 MySQL Setup
Update `application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/blogdb
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

---

## 🌐 Frontend Setup

### 📌 Prerequisites
- Node.js (v18+)
- npm or yarn

### 📦 Install & Run
```bash
cd frontend
npm install
npm start
```

---

## 🔐 Authentication

- **JWT Token** used for securing APIs.
- Token is stored in localStorage on login.
- Axios sends token as `Authorization: Bearer <token>` header.

---

## 🔗 API Endpoints (Spring Boot)

| Method | Endpoint                      | Description              |
|--------|-------------------------------|--------------------------|
| POST   | `/api/auth/register`          | Register user            |
| POST   | `/api/auth/login`             | Login                    |
| GET    | `/api/posts`                  | List all posts           |
| GET    | `/api/posts/{id}`             | Get post by ID           |
| POST   | `/api/posts`                  | Create post (admin)      |
| DELETE | `/api/posts/{id}`             | Delete post + comments   |
| POST   | `/api/comments`               | Add comment              |
| GET    | `/api/comments/posts/{id}`    | Get comments by post     |

---

## 🧪 Testing

- Backend APIs tested using **Postman**
- Frontend interactions tested manually
- Exception handling included for 400, 403, 404, 500

---

## 🛠️ To-Do

- [ ] Unit & Integration Testing
- [ ] Like/Dislike Comments
- [ ] Add Profile Page
- [ ] Pagination for posts

---

## 🤝 Contributing

Contributions are welcome! Open an issue first to discuss your ideas.

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).
