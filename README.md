
# Movie Theater Booking System 🎥

## Description
This project is a backend application for managing a movie theater. It allows users to:
- Browse a **catalog of movies**.
- View **available showtimes** and book seats for specific screenings.
- **Administrators** can manage movies, showtimes, and reservations.
- Supports **authentication** with role-based access (Admin and Customer).

This project is developed using **Java** and **Spring Boot**, with **MySQL** as the database.

---

## Features

### Core Features
1. **Movie Management**:
   - View available movies.
   - Add, edit, and delete movies (admin only).

2. **Showtime Management**:
   - Create and manage showtimes and assign movies to theaters.
   - View available showtimes.

3. **Seat Booking**:
   - Reserve specific seats for a showtime.
   - Cancel bookings.

4. **Authentication**:
   - Secure login and registration.
   - Role-based access control using **JWT** tokens.

---

## Technologies Used

### Core Technologies
- **Java 17**: Programming language.
- **Spring Boot**: Framework for backend development.
- **MySQL**: Relational database for data storage.

### Dependencies
- **Spring Boot Starter Web**: For building REST APIs.
- **Spring Boot Starter Data JPA**: For database interactions.
- **Spring Security**: For securing the application.
- **JWT**: For authentication and authorization.
- **MySQL Driver**: For MySQL database connection.
- **Lombok**: To reduce boilerplate code.
- **Spring Boot DevTools**: For hot reloading during development.
- **Swagger/OpenAPI**: For API documentation.

### Additional Tools
- **Docker**: For containerization of the backend and database.
- **Postman**: For API testing.
- **DBeaver/MySQL Workbench**: For database management.

---

## Project Setup

### Prerequisites
Make sure you have the following installed:
1. **Java 17** or higher.
2. **Maven** or **Gradle** for dependency management.
3. **MySQL** (or Docker for containerized MySQL).
4. **Postman** (or Insomnia) for testing APIs.

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/movie-theater-backend.git
   cd movie-theater-backend
   ```

2. Install dependencies using Maven:
   ```bash
   mvn clean install
   ```

3. Configure the database in `src/main/resources/application.yml`:
   ```yaml
   spring:
     datasource:
       url: jdbc:mysql://localhost:3306/movie_theater
       username: your_username
       password: your_password
     jpa:
       hibernate:
         ddl-auto: update
       show-sql: true
   ```

4. Start the application:
   ```bash
   mvn spring-boot:run
   ```
---

## API Endpoints

### Authentication
- `POST /auth/login`: Authenticate and receive a JWT token.
- `POST /auth/register`: Register a new user.

### Movies
- `GET /movies`: Get a list of all movies.
- `POST /movies`: Add a new movie (admin only).
- `PUT /movies/{id}`: Update movie details (admin only).
- `DELETE /movies/{id}`: Delete a movie (admin only).

### Showtimes
- `GET /showtimes`: View available showtimes.
- `POST /showtimes`: Create a new showtime (admin only).

### Reservations
- `POST /reservations`: Create a reservation for a specific showtime.
- `DELETE /reservations/{id}`: Cancel a reservation.

---

## Project Structure

```plaintext
src
├── main
│   ├── java
│   │   ├── com.example.movietheater
│   │   │   ├── controller    # REST Controllers
│   │   │   ├── service       # Business Logic
│   │   │   ├── repository    # Database Access
│   │   │   ├── model         # Entities
│   │   │   ├── dto           # Data Transfer Objects
│   │   │   └── config        # Configuration (Security, etc.)
│   └── resources
│       ├── application.yml   # App Configuration
│       └── static            # Static resources (if any)
```

---

## Future Enhancements
1. **Notifications** for reservation confirmation or changes.
2. **Admin dashboard** with metrics and reports.
3. **Support for multiple languages**.
4. Integration with **external payment gateways** for ticket purchases.


---



