### Spring Boot JWT Authentication API

A simple and secure **JWT (JSON Web Token) Authentication System** built using **Spring Boot**, **Spring Security**, and **MySQL**.

 ### Features

 User Login with username & password
 JWT Token Generation
 Token-based Authentication
 Spring Security Integration
 MySQL Database Support
 REST API (GET & POST endpoints)

### Tech Stack

* Java 21
* Spring Boot
* Spring Security
* Spring Data JPA
* MySQL
* Maven

 ### Project Structure

src/main/java/com/aml3B/DEMO_JWT/
│
├── config        # Security configuration
├── controller    # API endpoints
├── model         # Entity classes
├── repository    # Database access layer
├── security      # JWT utilities
├── service       # Business logic
└── DemoJwtApplication.java

 Setup Instructions

### 1️⃣ Clone the repository

```
git clone https://github.com/Umangdokania/FSDEXP9.git
cd FSDEXP9
```

---

### 2️⃣ Configure Database

Update `application.properties`:

```
spring.datasource.url=jdbc:mysql://localhost:3306/JwtDemo
spring.datasource.username=your_username
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 3️⃣ Run the application

```
mvn spring-boot:run
```

API Endpoints

 1. Login (Generate JWT)

**POST** `/api/login`

Body (x-www-form-urlencoded):

```
username=admin
password=admin
```

 Response:

```
JWT Token (string)
```

 2. Test API

**GET** `/api/hello`

Response:

```
Hello! JWT Authentication Successful
```

 How JWT Works

1. User sends login request
2. Server verifies credentials
3. JWT token is generated
4. Token is used for accessing secured APIs

 Testing (Postman)

* Use **POST** for `/api/login`
* Use **GET** for `/api/hello`
* Pass username & password as form-data

 Sample Output

* Login → Returns JWT Token
* Hello API → Returns success message

 Note

* This project is for **learning/demo purposes**
* Passwords are stored in plain text (can be improved using encryption)
* Security config currently allows all requests (`permitAll()`)



    ### Screenshots

<img width="1440" height="900" alt="Screenshot 2026-03-31 at 4 18 34 PM" src="https://github.com/user-attachments/assets/3632c8df-f977-4556-a9fb-382cf0d9b4f1" />

<img width="1440" height="900" alt="Screenshot 2026-03-31 at 4 18 12 PM" src="https://github.com/user-attachments/assets/7d33625c-c9c8-4150-a568-b9d4d91325b7" />

<img width="1440" height="900" alt="Screenshot 2026-04-06 at 12 22 15 PM" src="https://github.com/user-attachments/assets/c17543af-cd08-4f6d-a502-766cd6d070d2" />

<img width="1440" height="900" alt="Screenshot 2026-04-06 at 12 23 31 PM" src="https://github.com/user-attachments/assets/47f19103-c6b8-43f5-a929-2287f9969afb" />

<img width="1440" height="900" alt="Screenshot 2026-04-06 at 12 24 02 PM" src="https://github.com/user-attachments/assets/b6f6e390-50d5-4bfe-9616-22a69cb0589e" />

