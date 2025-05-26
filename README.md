# Athlete Inventory Management API (AIM API)

A lightweight, scalable backend REST API built using **Java**, **Spring Boot**, and **AWS**, designed to manage athlete gear inventory data for retail and internal Nike applications.

## 📌 Project Overview

This API provides CRUD operations for managing athlete inventory items such as shoes, apparel, and equipment. It follows RESTful best practices and is designed for deployment on AWS infrastructure.

## 🚀 Tech Stack

- **Java 17**
- **Spring Boot 3.x**
- **DynamoDB** / **MySQL** (as primary datastore)
- **AWS EC2** (for deployment)
- **Docker**
- **JUnit 5** & **Mockito** (for unit testing)
- **GitHub Actions** / **AWS CodePipeline** (for CI/CD)

## 📝 Features

- Create, Read, Update, Delete (CRUD) operations for inventory items
- RESTful API design following best practices
- API documentation with **Swagger**
- Test-Driven Development with **JUnit** and **Mockito**
- CI/CD pipeline integration
- Dockerized for containerized deployment
- Cloud deployment using **AWS EC2**

## 📚 API Endpoints

| Method | Endpoint             | Description                     |
|:--------|:---------------------|:--------------------------------|
| `POST`  | `/api/inventory`      | Add a new inventory item         |
| `GET`   | `/api/inventory`      | Retrieve all inventory items     |
| `GET`   | `/api/inventory/{id}` | Retrieve a specific item by ID   |
| `PUT`   | `/api/inventory/{id}` | Update an existing item          |
| `DELETE`| `/api/inventory/{id}` | Delete an item                   |

## 📂 Project Structure
```
athlete-inventory-api/
├── src/
│ ├── main/
│ │ ├── java/com/aim/api/
│ │ │ ├── controller/
│ │ │ ├── service/
│ │ │ ├── model/
│ │ │ └── repository/
│ │ └── resources/
│ │ └── application.properties
│ └── test/
│ └── java/com/aim/api/
│ └── service/
├── Dockerfile
├── pom.xml
└── README.md
```


## 🛠️ Getting Started

### Prerequisites:
- Java 17
- Maven
- Docker (optional)
- AWS EC2 instance (for deployment)

### Run Locally:
```bash
mvn clean install
mvn spring-boot:run
API will be accessible at: http://localhost:{port}/api/inventory

🐳 Docker Deployment (Optional)
bash
Copy
Edit
docker build -t athlete-inventory-api .
docker run -p 8080:8080 athlete-inventory-api
✅ Testing
Run tests with:

bash
Copy
Edit
mvn test
Unit tests written using JUnit 5 and Mockito.

📦 CI/CD
Setup either:

GitHub Actions for automated build, test, and deploy

AWS CodePipeline for cloud-native CI/CD workflows

