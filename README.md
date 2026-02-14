# Product Service Microservice - DevOps Lab 2

**Module:** Current Trends in Software Engineering (SE4010)  
**Lab:** DevOps Lab – 3  
**Title:** Building a Spring Boot Microservice with In-Memory Database & Swagger  

**Student Details**  
- **Name:** Dilshan S.C  
- **IT Number:** IT22118318  
- **Group:** Y4S2.WE.SE.01.01  
- **Module:** SE4010 – Current Trends in Software Engineering  
- **Semester:** Semester 2, 2026 

## Objective

The goal of this lab is to create a simple **RESTful Product microservice** using **Spring Boot** with the following features:

- CRUD operations (Create, Read, Update, Delete)
- Data persistence using **H2 in-memory database**
- Interactive API documentation using **Swagger OpenAPI**

## Technologies Used

- **Java** (17 or later recommended)
- **Spring Boot** (latest stable version)
- **Maven** (build tool)
- **Spring Web** – for building REST APIs
- **Spring Data JPA** – for database access
- **H2 Database** – in-memory database
- **Springdoc OpenAPI UI** (Swagger) – for API documentation

## Project Setup

The project was generated using **Spring Initializr** with the following configuration:

- **Project**     : Maven  
- **Language**    : Java  
- **Packaging**   : Jar  
- **Group**       : com.sliit  
- **Artifact**    : product-service  
- **Dependencies**:
  - Spring Web
  - Spring Data JPA
  - H2 Database
  - Springdoc OpenAPI UI

## Features Implemented

### Part 1 – Creating the Spring Boot Microservice
- Project generated via https://start.spring.io
- Imported and configured in IDE (IntelliJ / Eclipse / VS Code)

### Part 2 – Implementing REST APIs
Created full **CRUD** operations for the **Product** resource:

| HTTP Method | Endpoint                  | Description                  |
|-------------|---------------------------|------------------------------|
| POST        | `/api/products`           | Create a new product         |
| GET         | `/api/products`           | Get all products             |
| GET         | `/api/products/{id}`      | Get product by ID            |
| DELETE      | `/api/products/{id}`      | Delete product by ID         |

(Note: PUT/update endpoint can be added as extension if required)

**Entity:** `Product`  
Fields: `id` (Long, auto-generated), `name` (String), `price` (Double/BigDecimal)

### Part 3 – Using In-Memory Database (H2)

- Configured H2 in `application.properties`
- Enabled H2 web console
- JDBC URL: `jdbc:h2:mem:testdb` (or similar)
- Access H2 console at: **http://localhost:8080/h2-console**

### Part 4 – Enabling Swagger (OpenAPI)

- Added `springdoc-openapi-starter-webmvc-ui` dependency
- Swagger UI available at: **http://localhost:8080/swagger-ui.html**  
- OpenAPI JSON available at: **http://localhost:8080/v3/api-docs**

## How to Run the Application

1. Clone or download the project
2. Open in your preferred IDE
3. Run the main class:  
   `ProductServiceApplication.java` (or use Maven command)
   
   ```bash
   mvn spring-boot:run
