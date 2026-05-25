# LinkxChop - Enterprise URL Shortener Platform

LinkxChop is a secure, high-performance URL shortener platform built using a robust, multi-layered Microservices architecture. Designed for minimal latency and high scalability, the system handles 1,000+ requests per day and features real-time click tracking, JWT authentication, and fully containerized deployments.

## 🌐 Live Demo & Deployment Notes

The application is fully deployed and accessible here: **[LinkxChop Live Application](https://linkxchop.netlify.app/)**

> ⚠️ **Important Note on Performance:** > Because this portfolio project is currently hosted on a **free-tier hosting platform**, the underlying database goes into a "cold sleep" after periods of inactivity.
> * **Initial Load Delay:** If you are the first person to visit the site in a while, the initial database request may take **30–50 seconds** to wake up the server.
> * **Subsequent Performance:** Once the database instance is awake, all subsequent URL shortening, routing, and authentication requests will process with optimal, sub-millisecond latency.


## 🚀 Key Features
* **Secure URL Shortening:** Generates highly optimized, shortened aliases for complex URLs.
* **JWT Authentication:** Implements secure user onboarding, authentication, and state management using Spring Security and JSON Web Tokens (JWT).
* **Real-time Analytics:** Tracks click metrics and user interactions with minimal latency.
* **Multi-Layered Architecture:** Follows enterprise design patterns separating Controller, Service, DTO, and Repository layers.
* **Production-Ready Environment:** Securely handles configuration using externalized environment variables (`.env`).
* **Containerized Deployment:** Fully Dockerized for seamless multi-environment consistency and scalability.

---

## 🛠️ Tech Stack

### Backend
* **Language:** Java
* **Framework:** Spring Boot (Spring MVC, Spring Data JPA, Spring Security)
* **Security:** JWT (JSON Web Tokens), Role-Based Access Control (RBAC)
* **Database:** PostgreSQL / MySQL

### Frontend
* **Framework:** React.js
* **Styling:** Tailwind CSS

### DevOps
* **Containerization:** Docker

---

## 🏗️ Architecture & Project Structure

The backend follows a strict multi-layered architecture to maximize decoupling and maintainability:

```text
├── src/main/java/org/url/shortener/
│   ├── controller/      # REST Endpoints (Handles HTTP Requests/Responses)
│   ├── service/         # Core Business Logic & Shortening Algorithms
│   ├── repository/      # Database Access Layer (Spring Data JPA)
│   ├── dtos/             # Data Transfer Objects for Secure Payload Delivery
│   ├── model/           # Database Entities
│   └── security/        # JWT & Spring Security Configurations