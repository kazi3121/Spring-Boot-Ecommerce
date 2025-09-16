# 🛍️ E-Commerce Backend (Spring Boot)

This project is a **Spring Boot backend service** for an E-Commerce application.  
It manages product information, including images, stock quantity, availability, and search functionality.  

⚠️ **Note:** The **frontend of this project is not developed by me**. This repository only contains the **backend (REST API)**.

---

## 🚀 Features
- CRUD operations for products (Create, Read, Update, Delete).
- Upload and serve product images.
- Search products by name, description, brand, or category.
- PostgreSQL database integration.
- RESTful API endpoints for frontend integration.

---

## 🛠️ Tech Stack
- **Java 17**
- **Spring Boot 3.5.5**
- **Spring Data JPA (Hibernate)**
- **PostgreSQL**
- **Lombok**

## Project Structure
ecom-project/
├── src/main/java/com/example/ecom_project
│ ├── controller/ # REST controllers (API layer)
│ ├── model/ # JPA entities (Product)
│ ├── repository/ # Data access (Spring Data JPA)
│ ├── service/ # Business logic
│ └── EcomProjectApplication.java # Main entry point
├── src/main/resources
│ ├── application.properties # DB configuration
├── pom.xml # Maven dependencies


## Configure Database
- spring.datasource.url=jdbc:postgresql://localhost:6022/Ecom
- spring.datasource.username=postgres
- spring.datasource.password=12345

## Product Image handling
- Images are uploaded as MultipartFile along with product details.
- Images are stored in the database as byte arrays.
- Accessible via /api/product/{id}/image.

## API Endpoints
Method       Endpoint	                           Description
GET	       /api/products	                       Get all products
GET	       /api/product/{id}                     Get product by ID
POST	     /api/product	                         Add a new product (with image)
PUT	       /api/product/{id}                     Update an existing product
DELETE	   /api/product/{id}	                   Delete a product
GET        /api/product/{id}/image	             Get product image by ID
GET	       /api/products/search?keyword=...	     Search products by keyword


## Frontend
The frontend is not part of this repository.

This backend exposes REST APIs that are integrated with React, to have the frontend you can contact with me (kazialaminislam602245@gmail.com).
