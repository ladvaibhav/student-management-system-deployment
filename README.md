# Student Management System (Deployment Repository)

This repository contains the **Dockerized deployment configuration** of the Student Management System backend built with Spring Boot.

The core development repository is maintained separately.

https://github.com/ladvaibhav/student-management-system

This repository focuses specifically on **containerization and cloud deployment**.

🔐 Authentication is fully implemented using Spring Security with BCrypt encryption.  
⚠️ For demonstration purposes, security is disabled in the deployed version to allow easy API testing via Swagger.

---

## 📖 Swagger Documentation
https://student-management-temp.onrender.com/swagger-ui/index.html

⚠️ Note: The application is hosted on Render’s free tier.
If the service has been idle, it may take 4-5 minutes to start on the first request.

## 🌍 Live API URL
https://student-management-temp.onrender.com

You can use this base URL to access all endpoints.

Example:
GET https://student-management-temp.onrender.com/v1/students/all


---

## 🛠 Tech Stack

- Java 23+
- Spring Boot 4.0+
- Spring Data JPA
- Hibernate ORM
- PostgreSQL (Managed Database)
- Maven
- Spring Security
- Swagger (Springdoc OpenAPI)
- Docker
- Render (Cloud Hosting)

---

## 🐳 Deployment Architecture

Spring Boot Application  
        ↓  
Docker Container  
        ↓  
Render Web Service  
        ↓  
Managed PostgreSQL (Render)

<img src="docs/images/img_7.png" width="500"/>

---

## 🐳 Deployment Details

- Containerized using Docker
- Environment variables used for database credentials
- CI/CD enabled via GitHub integration
- Internal database networking for secure communication

### 🔐 Environment Variables

- `SPRING_DATASOURCE_URL`
- `SPRING_DATASOURCE_USERNAME`
- `SPRING_DATASOURCE_PASSWORD`
- `PORT`

---

## 🚀 Features

### 📌 Core Functionalities

CRUD Operations for:

- Students
- Departments
- Courses
- Subjects
- Users

### 📄 Pagination & Sorting

- Offset-based Pagination
- Dynamic Sorting (ASC / DESC)

### 🏗 Architecture (Layered Design)

- Entity
- DTO (Data Transfer Object)
- Repository
- Service
- Service Implementation (ServiceImpl)
- Controller

### ⚙ Backend Best Practices

- Global Exception Handling
- Input Validation using Jakarta Validation
- Spring Security (HTTP Basic Authentication)
- Password Encryption using BCrypt
- Swagger API Documentation

---

# 📌 API Endpoints

## 👨‍🎓 Student Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/v1/students` | Create student |
| GET | `/v1/students/all` | Get all students |
| GET | `/v1/students/id/{id}` | Get student by ID |
| GET | `/v1/students/email/{email}` | Get student by email |
| GET | `/v1/students/name/{name}` | Get student by name |
| GET | `/v1/students/paged` | Pagination & sorting |
| PUT | `/v1/students/id/{id}` | Update student |
| DELETE | `/v1/students/id/{id}` | Delete by ID |
| DELETE | `/v1/students/email/{email}` | Delete by Email |

---

## 👤 User Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/v1/users` | Create user |
| GET | `/v1/users/all` | Get all users |
| GET | `/v1/users/id/{userId}` | Get user by ID |
| GET | `/v1/users/name/{username}` | Get user by username |
| PUT | `/v1/users/id/{userId}` | Update user |
| DELETE | `/v1/users/id/{userId}` | Delete user |

---

## 📚 Subject Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/v1/subject` | Create subject |
| GET | `/v1/subject/all` | Get all subjects |
| GET | `/v1/subject/subjectId/{subjectId}` | Get by ID |
| GET | `/v1/subject/subjectName/{subjectName}` | Get by name |
| PUT | `/v1/subject/subjectId/{subjectId}` | Update subject |
| DELETE | `/v1/subject/subjectId/{subjectId}` | Delete subject |

---

## 🏢 Department Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/v1/departments` | Create department |
| GET | `/v1/departments/all` | Get all departments |
| GET | `/v1/departments/deptId/{deptId}` | Get by ID |
| GET | `/v1/departments/deptName/{deptName}` | Get by name |
| PUT | `/v1/departments/deptId/{deptId}` | Update department |
| DELETE | `/v1/departments/deptId/{deptId}` | Delete department |

---

## 🎓 Course Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/v1/courses` | Create course |
| GET | `/v1/courses/all` | Get all courses |
| GET | `/v1/courses/id/{courseId}` | Get by ID |
| GET | `/v1/courses/name/{courseName}` | Get by name |
| GET | `/v1/courses/deptId/{deptId}` | Get by department |
| PUT | `/v1/courses/id/{courseId}` | Update course |
| DELETE | `/v1/courses/id/{courseId}` | Delete course |

---

## 📄 Pagination Example

`GET /v1/students/paged?page=0&size=4&sort=name,asc`

---

## 📸 Swagger UI Preview

<table>
  <tr>
    <td><img src="docs/images/img_1.png" width="800"/></td>
    <td><img src="docs/images/img.png" width="800"/></td>
  </tr>
</table>

---

## 💡 Key Learning Outcomes

- REST API Design
- Clean Layered Architecture
- DTO Pattern Implementation
- Exception Handling Strategy
- Pagination & Sorting Implementation
- Spring Security Integration
- Docker Containerization
- Cloud Deployment on Render

---

## Status

✅ Successfully Deployed  
🚧 Work in Progress

---


## 👨‍💻 Author

**Vaibhav Lad**  
Backend Developer | Spring Boot | PostgreSQL | Docker | Cloud Deployment
