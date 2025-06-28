# User Management API

A Spring Boot REST API for user management with authentication and role-based access control.

## Requirements

- Java 17+
- Maven 3.8+
- PostgreSQL 13+

## Setup

1. Clone the repository
```bash
git clone https://github.com/username/user-management-api.git
cd user-management-api
```

2. Configure database in `application.properties`
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/userdb
spring.datasource.username=your_username
spring.datasource.password=your_password
```

3. Run the application
```bash
mvn spring-boot:run
```

The API will be available at `http://localhost:8080`

## API Endpoints

```
POST   /api/auth/login          - User login
POST   /api/auth/register       - User registration
GET    /api/users               - Get all users (Admin only)
GET    /api/users/{id}          - Get user by ID
PUT    /api/users/{id}          - Update user
DELETE /api/users/{id}          - Delete user (Admin only)
```

## Testing

```bash
mvn test
```

## License

MIT License