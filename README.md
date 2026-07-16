<div align="center">

# 🚀 Spring Boot User CRUD REST API

### Persistent Storage with MySQL | Spring Data JPA | Hibernate | Flyway

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=springboot)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate-ORM-59666C?style=for-the-badge&logo=hibernate)
![Flyway](https://img.shields.io/badge/Flyway-Migrations-CC0200?style=for-the-badge)
![Maven](https://img.shields.io/badge/Maven-Build-C71A36?style=for-the-badge&logo=apachemaven)

**A production-style RESTful CRUD API built with Spring Boot featuring persistent storage using MySQL, Spring Data JPA (Hibernate), and Flyway database migrations.**

</div>

---

# 📌 Project Overview

This project was developed as part of the **Prodigy InfoTech Internship – Task 2: Persistent Storage with Database Integration**.

The application extends a basic REST API by integrating **MySQL** for permanent data storage. It follows a clean layered architecture using **Controller → Service → Repository**, with **Spring Data JPA** and **Hibernate ORM** handling database interactions.

Database schema creation and versioning are managed automatically using **Flyway Migrations**, making the project scalable and production-ready.

---

# ✨ Features

- ✅ Create User
- ✅ Retrieve All Users
- ✅ Retrieve User by ID
- ✅ Update Existing User
- ✅ Delete User
- ✅ Persistent Data Storage using MySQL
- ✅ Spring Data JPA Repository
- ✅ Hibernate ORM
- ✅ Flyway Database Migration
- ✅ UUID-based User IDs
- ✅ DTO Validation
- ✅ Global Exception Handling
- ✅ Environment Variable Configuration (.env)
- ✅ HikariCP Connection Pooling
- ✅ Tested using Postman

---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| Java 21 | Programming Language |
| Spring Boot | Backend Framework |
| Spring Web | REST API Development |
| Spring Data JPA | Database Access Layer |
| Hibernate | ORM Framework |
| MySQL | Relational Database |
| Flyway | Database Migration |
| Maven | Dependency Management |
| Postman | API Testing |
| IntelliJ IDEA | Development Environment |

---

# 🏗 Project Architecture

```text
                 Client (Postman)

                        │
                        ▼

             ┌─────────────────────┐
             │  UserController      │
             └─────────────────────┘
                        │
                        ▼

             ┌─────────────────────┐
             │    UserService       │
             └─────────────────────┘
                        │
                        ▼

             ┌─────────────────────┐
             │ UserRepository (JPA) │
             └─────────────────────┘
                        │
                        ▼

             ┌─────────────────────┐
             │   Hibernate ORM      │
             └─────────────────────┘
                        │
                        ▼

             ┌─────────────────────┐
             │   MySQL Database     │
             └─────────────────────┘
```

---

# 📂 Project Structure

```text
basic-rest-api
│
├── docs
│   └── screenshots
│
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.example.basic_rest_api
│   │   │       ├── controller
│   │   │       ├── dto
│   │   │       ├── exception
│   │   │       ├── model
│   │   │       ├── repository
│   │   │       ├── service
│   │   │       └── BasicRestApiApplication
│   │   │
│   │   └── resources
│   │       ├── application.properties
│   │       └── db
│   │           └── migration
│   │               └── V1__create_users_table.sql
│
├── pom.xml
├── .gitignore
├── README.md
└── .env (ignored)
```

---

# 🗄 Database Details

**Database:** MySQL

**Schema:** `prodigy_task2_db`

**Migration Tool:** Flyway

**ORM:** Hibernate (Spring Data JPA)

### Users Table

| Column | Type |
|---------|------|
| id | UUID |
| name | VARCHAR |
| email | VARCHAR |
| age | INTEGER |

---

# 🔗 REST API Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | `/api/users` | Create User |
| GET | `/api/users` | Retrieve All Users |
| GET | `/api/users/{id}` | Retrieve User by ID |
| PUT | `/api/users/{id}` | Update Existing User |
| DELETE | `/api/users/{id}` | Delete User |

---

# ⚙️ How to Run the Project

## Clone Repository

```bash
git clone https://github.com/uddishasinghh31/springboot-user-crud-api.git
```

---

## Configure MySQL

Create a database named:

```sql
CREATE DATABASE prodigy_task2_db;
```

---

## Configure Environment Variables

Create a `.env` file in the project root.

```properties
DB_URL=jdbc:mysql://localhost:3306/prodigy_task2_db
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

> **Note:** The `.env` file is intentionally excluded from GitHub using `.gitignore` to keep credentials secure.

---

## Run the Application

Using Maven:

```bash
mvn spring-boot:run
```

Or simply run:

```
BasicRestApiApplication.java
```

Flyway will automatically create the required database tables on application startup.

---

# 📸 Project Screenshots

## 🏗 Project Structure

Shows the layered package structure used in the application.

<p align="center">
<img src="docs/screenshots/git_structure.png" width="900"/>
</p>

---

## 📂 Complete Project Directory

Displays the complete Maven project structure including documentation, resources, and migration scripts.

<p align="center">
<img src="docs/screenshots/complete-project-structure.png" width="900"/>
</p>

---

## 🌐 API Testing using Postman

Successful retrieval of users through the REST API.

<p align="center">
<img src="docs/screenshots/get_fromDatabase.png" width="900"/>
</p>

---

## 🗄 MySQL Database

Persistent records stored inside the MySQL database after API requests.

<p align="center">
<img src="docs/screenshots/mysql_database.png" width="900"/>
</p>

---

# 🧪 Sample JSON Response

```json
[
  {
    "id": "81acc614-cae5-44a2-881e-d85156fa6efb",
    "name": "Riya",
    "email": "riya@gmail.com",
    "age": 34
  },
  {
    "id": "aa1cb954-f377-4f53-aa4b-643ba9924ad3",
    "name": "Maya",
    "email": "maya@gmail.com",
    "age": 5
  }
]
```

---

# 🚀 Future Improvements

- Swagger / OpenAPI Documentation
- Spring Security Authentication
- JWT Authentication
- Pagination & Sorting
- Search APIs
- Docker Support
- Unit Testing with JUnit
- Logging using SLF4J
- CI/CD Pipeline
- Cloud Deployment (AWS / Railway / Render)

---

# 👩‍💻 Author

**Udisha Singh**

GitHub: https://github.com/uddishasinghh31

---

# 📄 Internship Details

**Organization:** Prodigy InfoTech

**Task 1:** Build a REST API for CRUD Operations

**Task 2:** Extend the REST API with Persistent Storage using MySQL, Hibernate, Spring Data JPA, and Flyway Database Migrations.

---

<div align="center">

### ⭐ If you found this project useful, please consider giving it a Star!

</div>
