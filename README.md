# Student Management System - Backend (Spring Boot)

This is the **backend REST API** for a Student Management System built using **Spring Boot** and **MySQL**. It provides full CRUD operations and integrates with a frontend built using Angular.

---

## 🚀 Features

- ✅ Create, Read, Update, Delete (CRUD) operations for student records
- 📦 RESTful API
- 🌐 CORS configuration for frontend communication
- 🗃️ MySQL Database integration
- 

---

## 🔧 Tech Stack

- Java 17+
- Spring Boot 3.x
- Spring Web
- Spring Data JPA
- MySQL
- Lombok (for boilerplate reduction)

---

## 📁 Project Structure

```
src/
├── main/
│   ├── java/com/example/studentapi/
│   │   ├── controller/
│   │   │   └── StudentController.java
│   │   ├── model/
│   │   │   └── Student.java
│   │   ├── repository/
│   │   │   └── StudentRepository.java
│   │   ├── service/
│   │   │   └── StudentService.java
│   │   └── StudentApiApplication.java
│   └── resources/
│       ├── application.properties
```

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/ShwejanShashank/sms.git
cd sms
```

### 2. Configure MySQL

Make sure MySQL is installed and running. Create a database named `studentdb`.

Update your `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/studentdb
spring.datasource.username=your_mysql_username
spring.datasource.password=your_mysql_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect

server.port=8081
```

### 3. Build the project

If using Maven:

```bash
./mvnw clean install
```

Or with Gradle:

```bash
./gradlew build
```

### 4. Run the application

```bash
./mvnw spring-boot:run
```

App will start at: [http://localhost:8081](http://localhost:8081)

---

## 🌐 API Endpoints

| Method | Endpoint              | Description             |
|--------|-----------------------|-------------------------|
| GET    | `/api/students`       | Get all students        |
| GET    | `/api/students/{id}`  | Get student by ID       |
| POST   | `/api/students`       | Create new student      |
| PUT    | `/api/students/{id}`  | Update student by ID    |
| DELETE | `/api/students/{id}`  | Delete student by ID    |

---

## 🔐 CORS Configuration

CORS is enabled in the controller like this:

```java
@CrossOrigin(origins = "http://localhost:4200")
```

Change the origin to match your Angular frontend if needed.

---

## 🧪 Testing

Run unit tests using:

```bash
./mvnw test
```

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

## ✨ Acknowledgments

- Spring Boot documentation
- MySQL JDBC integration
- Angular frontend available [here](https://github.com/ShwejanShashank/student-app)
