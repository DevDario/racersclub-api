# 🏎️ RacersClub API

![Language](https://img.shields.io/badge/language-Kotlin-7F52FF?style=for-the-badge&logo=kotlin)
![Framework](https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Database](https://img.shields.io/badge/PostgreSQL-Neon-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Hosting](https://img.shields.io/badge/Hosted_on-Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)
![License](https://img.shields.io/github/license/DevDario/racersclub-api?style=for-the-badge)

---

## 📌 Overview

**RacersClub API** is a clean, modular backend service that manages a fictional racing club.  
It provides **CRUD operations for Racers, Cars, and Races**, built with **Spring Boot + Kotlin** and following **Domain-Driven Design (DDD)** principles.

This project is designed as a practical study of clean backend architecture using modern Java/Kotlin technologies, while applying industry best practices.

---

## 🧩 Architecture

This project follows the **Domain-Driven Design (DDD)** layered architecture:
```yml
src
└── main
├── domain # Entities, Value Objects, Domain Services
├── application # Use Cases (Services, DTOs)
├── infrastructure
│ ├── repository (JPA implementations)
│ ├── config (Spring configurations)
│ └── persistence (Postgres entities/mappings)
└── interfaces # Controllers (REST endpoints)
```

> ✅ Domain logic is isolated from framework & infrastructure  
> ✅ Clear separation of concerns for scalability and testability

---

## ⚙️ Tech Stack

- **Language**: [Kotlin](https://kotlinlang.org/)
- **Framework**: [Spring Boot](https://spring.io/projects/spring-boot)
- **ORM & Persistence**: Spring Data JPA + Hibernate
- **Database**: [PostgreSQL](https://www.postgresql.org/) (hosted on [Neon](https://neon.tech/))
- **Hosting**: [Render](https://render.com/)
- **Other dependencies**:
  - Lombok
  - Spring Web (REST)
  - Spring Security
  - Spring Boot DevTools (optional)
  - Validation (Jakarta)
  - Java Mail Sender (email validation)

---

## 🚀 Features

- 🔐 User **Authentication** with **JWT** and **Email validation**
- 📇 Manage **Racers** (create, read, update, delete)
- 🚗 Manage **Cars** assigned to Racers
- 🏁 Manage **Races** (scheduling, participants)
- 📦 RESTful API endpoints with JSON payloads
- 🛡️ Validation and error handling

---

## 💻 Local Development Setup

### 1. Prerequisites
- JDK 17+ (Temurin or OpenJDK)
- Gradle (or use the Gradle wrapper)
- PostgreSQL (local or Neon instance)
- VS Code / IntelliJ IDEA (with Kotlin & Spring plugins)

### 2. Clone and Configure

```bash
git clone https://github.com/DevDario/racersclub-api.git
```
```powershell
cd racersclub-api
```

- Create .env (or application-dev.yml) with your DB credentials:

```yml
SPRING_DATASOURCE_URL=jdbc:postgresql://localhost:5432/racersclub
SPRING_DATASOURCE_USERNAME=postgres
SPRING_DATASOURCE_PASSWORD=yourpassword
```
### 3. Run the API

```yml
./gradlew bootRun
```

### 4. Test

- Open:

```h
http://localhost:8080/api/auth
http://localhost:8080/api/racers
http://localhost:8080/api/cars
http://localhost:8080/api/races
```

## ☁️ Deployment

- Database is deployed on Neon
 (serverless PostgreSQL) 🌍

- Backend is deployed on Render 🌍

- Use Render’s Dockerfile or Build & Deploy from GitHub.
Remember to add environment variables for **DB URL**, **username**, and **password**.


## 📂 Project Structure

```yml
racersclub-api
 ├── build.gradle.kts
 ├── settings.gradle.kts
 ├── src
 │   ├── main
 │   │   ├── domain
 │   │   ├── application
 │   │   ├── infrastructure
 │   │   └── interfaces
 │   └── test
 └── README.md
```

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
Feel free to open an issue or submit a pull request.

## ⚖️ License

This project is licensed under the [MIT License](https://github.com/DevDario/racersclub-api/LICENSE.md)

## 📧 Contact

**Author**: Dário Silva <br>
**GitHub**: @DevDario 😉
