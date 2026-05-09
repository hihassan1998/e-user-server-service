# e-user-server-service

## Table of Contents
- [User Server Service – Earnsome MVP](#user-server-service--earnsome-mvp)
- [Responsibilities](#responsibilities)
- [Tech Stack](#tech-stack)
- [Gateway Integration](#gateway-integration)
- [Get Started](#get-started)
- [Contributions](#contributions)

---

# User Server Service – Earnsome MVP

The **User Server Service** is responsible for handling all user-related data and profile management functionality within the Earnsome fintech platform. It acts as the dedicated user data layer in the microservice architecture and works together with the Auth Service, Business Service, and API Gateway.

This service manages user profile information, account settings, user roles, and protected user operations. Authentication itself is handled externally by the Auth Server Service, while this service focuses on storing and managing application-specific user data.

The User Service communicates securely through JWT-based authentication validated by the API Gateway. Requests forwarded from the gateway can include verified user identity information used to personalize and secure user-specific operations.

The service is designed with scalability and separation of concerns in mind, allowing authentication, business logic, and user management to evolve independently across the Earnsome platform.

---

## Responsibilities

- Store and manage user profile data
- Handle authenticated user operations
- Manage user roles and permissions
- Support protected user routes
- Integrate with API Gateway authentication flow
- Provide user-related APIs to frontend applications

---

## Tech Stack

- Node.js
- Express.js
- MongoDB
- Mongoose
- JSON Web Token (JWT)
- CORS
- Swagger/OpenAPI Documentation
- dotenv

---

## Gateway Integration

The User Server Service is intended to run behind the Earnsome API Gateway.

Example local routing:

| Gateway Route | Target Service |
|---|---|
| `/users/*` | `http://localhost:3002` |

Example:
```
GET http://localhost:3000/users/me
```
Forwarded internally to:
```
GET http://localhost:3002/users/me
```

## Get Started
1. Clone the repo:
```bash
 git clone https://github.com/hihassan1998/e-user-server-service.git
```
2. Move to the project:
```bash
 cd e-user-server-service
```
3. Intall all dependencies:
```bash
 npm install
```
4. Configure environment variables
Create a .env file:
```
PORT=3002
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_shared_secret
```
5. Development server
```
mpm start
```
6. Go to the web-browser and run 
```bash
 https://localhost:3001
```


## Contributions
This repository and its microservices are being developed as part of the research and development of the Earnsome fintech application, a real estate investment MVP platform.

The system is designed and implemented by Hassan Ishfaq Hussain, acting as the lead developer, with a focus on building a scalable microservice architecture for authentication, user management, business logic, and frontend integration.

Ibrahim Sohail Dar contributes as the accountant and business domain specialist, primarily responsible for defining and supporting the financial models, investment logic, and business rules that shape the core functionality of the platform.

![alt text](earnLogo-RMbG.png)