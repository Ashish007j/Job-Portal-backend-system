# Job Portal Backend System

A **Job Portal Backend System** built using **Java and Spring Boot**, designed to handle core backend functionalities of a modern job portal platform. This project focuses on scalable REST APIs, clean layered architecture, and real‑world backend features commonly asked in **top MNC interviews**.

---

## 🚀 Project Overview

This backend system provides APIs for managing **users, jobs, and job applications**. It is designed to serve as the backend for a job portal where **recruiters can post jobs** and **candidates can search and apply for jobs**.

The project follows **industry‑standard backend practices** such as:

* Layered architecture (Controller → Service → Repository)
* RESTful API design
* Database integration
* Clean and modular code structure

---

## 🛠 Tech Stack

* **Language:** Java
* **Framework:** Spring Boot
* **Build Tool:** Maven
* **Database:** MongoDB
* **ORM / Data Access:** Spring Data
* **API Type:** REST APIs
* **IDE Support:** IntelliJ IDEA, VS Code

---

## ✨ Key Features

### 👤 User Management

* User registration
* User login / authentication
* Role‑based users (Job Seeker / Recruiter)
* Profile management

### 💼 Job Management

* Create job postings (Recruiter)
* Update and delete job listings
* View all available jobs
* Search jobs by keyword / criteria

### 📄 Job Application Management

* Apply for jobs (Job Seeker)
* Track applied jobs
* View applicants for a job (Recruiter)

### ⚙️ Backend Capabilities

* RESTful API design
* Proper request/response handling
* Exception handling
* Modular and scalable codebase

---

## 📁 Project Structure

```
Job-Portal-backend-system
│
├── Main-Project
│   ├── controller     # REST Controllers
│   ├── service        # Business logic
│   ├── repository     # Database access layer
│   ├── model / entity # Data models
│   └── config         # Configuration files
│
├── pom.xml            # Maven dependencies
└── application.properties / yml
```

---

## 🔌 API Endpoints (Sample)

| Method | Endpoint              | Description         |
| ------ | --------------------- | ------------------- |
| POST   | `/api/users/register` | Register a new user |
| POST   | `/api/users/login`    | User login          |
| POST   | `/api/jobs`           | Create job posting  |
| GET    | `/api/jobs`           | Get all jobs        |
| POST   | `/api/applications`   | Apply for a job     |

---

## 🧪 API Testing (Terminal & Postman)

Below are sample **cURL commands** and **Postman test details** to test the APIs locally.

---

### 🔹 1. User Registration

**cURL (Terminal):**

```bash
curl -X POST http://localhost:8080/api/users/register \
-H "Content-Type: application/json" \
-d '{
  "name": "Ashish",
  "email": "ashish@gmail.com",
  "password": "123456",
  "role": "JOB_SEEKER"
}'
```

**Postman:**

* Method: `POST`
* URL: `http://localhost:8080/api/users/register`
* Body → raw → JSON

---

### 🔹 2. User Login

**cURL (Terminal):**

```bash
curl -X POST http://localhost:8080/api/users/login \
-H "Content-Type: application/json" \
-d '{
  "email": "ashish@gmail.com",
  "password": "123456"
}'
```

---

### 🔹 3. Create Job (Recruiter)

**cURL (Terminal):**

```bash
curl -X POST http://localhost:8080/api/jobs \
-H "Content-Type: application/json" \
-d '{
  "title": "Java Backend Developer",
  "company": "ABC Tech",
  "location": "Bangalore",
  "salary": "8-12 LPA",
  "description": "Spring Boot, REST APIs, MongoDB"
}'
```

---

### 🔹 4. Get All Jobs

**cURL (Terminal):**

```bash
curl -X GET http://localhost:8080/api/jobs
```

---

### 🔹 5. Apply for Job

**cURL (Terminal):**

```bash
curl -X POST http://localhost:8080/api/applications \
-H "Content-Type: application/json" \
-d '{
  "jobId": "JOB_ID_HERE",
  "userId": "USER_ID_HERE"
}'
```

---

## 📬 Postman Collection (Recommended)

* Create a **Postman Collection** named: `Job Portal Backend`
* Add folders:

  * User APIs
  * Job APIs
  * Application APIs
* Use environment variable:

  * `baseUrl = http://localhost:8080`

Example URL in Postman:

```
{{baseUrl}}/api/jobs
```

---

## ▶️ How to Run the Project

1. **Clone the repository**

   ```bash
   git clone https://github.com/Ashish007j/Job-Portal-backend-system.git
   ```

2. **Open the project in IDE** (IntelliJ / VS Code)

3. **Configure Database**

   * Update `application.properties` with database URL, username, and password

4. **Build the project**

   ```bash
   mvn clean install
   ```

5. **Run the application**

   ```bash
   mvn spring-boot:run
   ```

6. Backend will start at:

   ```
   http://localhost:8080
   ```
---

## 🔮 Future Enhancements

* JWT‑based authentication
* Role‑based authorization
* Resume upload feature
* Advanced job search & filters
* Admin dashboard
* Microservices architecture

---

## 👨‍💻 Author

**Ashish Kumar Jha**
Backend Developer

---

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub.

---

> This project is created for learning, practice, and interview preparation purposes.
