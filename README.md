# ecom-project
Spring Boot(Java) based e-commerce backend providing REST APIs for products and orders.

# E-Commerce Backend (Spring Boot)

A clean and modular **Spring Boot–based backend** for an e-commerce application. This project exposes RESTful APIs for managing products and is designed to integrate seamlessly with a modern frontend (React/Angular).

The goal of this project is to demonstrate **real-world backend development practices**, including layered architecture, database integration, and clean API design.

---

## 🚀 Features

* Product management (CRUD operations)
* RESTful API design using Spring MVC
* Layered architecture (Controller → Service → Repository)
* JPA/Hibernate for database interaction
* Externalized configuration using `application.properties`
* Ready to integrate with any frontend application

---

## 🧱 Project Structure

```
ecom-project
├── src/main/java/com/hunter/ecom_project
│   ├── controller        # REST controllers (API layer)
│   ├── service           # Business logic
│   ├── repository        # Data access layer (JPA repositories)
│   ├── model             # Entity classes
│   └── EcomProjectApplication.java
│
├── src/main/resources
│   ├── application.properties   # App configuration
│   ├── data1.sql                # Sample seed data
│   ├── static/                  # Static resources
│   └── templates/               # View templates (if needed)
│
└── pom.xml
```

---

## 🛠️ Tech Stack

* **Java 17+**
* **Spring Boot**
* **Spring Web (REST APIs)**
* **Spring Data JPA**
* **Hibernate**
* **H2 / MySQL (configurable)**
* **Maven**

---

## ⚙️ Configuration

Update database and server configuration in:

```properties
src/main/resources/application.properties
```

Example:

```properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driver-class-name=org.h2.Driver
spring.jpa.hibernate.ddl-auto=update
spring.h2.console.enabled=true
```

---

## ▶️ Running the Application

### Using Maven

```bash
mvn spring-boot:run
```

### Or using JAR

```bash
mvn clean package
java -jar target/ecom-project-0.0.1-SNAPSHOT.jar
```

Application will start at:

```
http://localhost:8080
```

---

## 📡 API Overview

### Product APIs

| Method | Endpoint                           | Description                |
| ------ | ---------------------------------- | -------------------------- |
| Method | Endpoint                           | Description                |
| ------ | ---------                          | -------------              |
| GET    | `/products`                        | Fetch all products         |
| GET    | `/products/{id}`                   | Fetch product by ID        |
| GET    | `/products/search?keyword={value}` | Search products by keyword |
| POST   | `/products`                        | Create a new product       |
| PUT    | `/products/{id}`                   | Update product             |
| DELETE | `/products/{id}`                   | Delete product             |

(Exact endpoints may vary based on controller implementation.)

---

## 🔗 Frontend Integration

This backend is designed to be consumed by a separate frontend application:

* React
* Angular
* Any REST-capable client

CORS and API URLs can be configured as needed.

---

## 🧪 Sample Data

Initial sample data is provided via:

```
src/main/resources/data1.sql
```

This helps bootstrap the database during development.

---

## 📌 Future Enhancements

* User authentication & authorization (JWT)
* Order and cart management
* Role-based access control
* Pagination and filtering
* API documentation using Swagger/OpenAPI

---

## 👨‍💻 Author

**Himanshu Patil**
Software/Backend Engineer
GitHub: [https://github.com/himanshupatil208](https://github.com/himanshupatil208)

---

## 📄 License

This project is open for learning and demonstration purposes.

