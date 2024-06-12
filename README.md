Sure! Here is a brief README for your `springboot-security-JWT-authentication` repository:

---

# Spring Boot JWT Authentication with Spring Security

## Description

This project demonstrates a secure authentication system using Spring Boot and Spring Security with JWT (JSON Web Token). It includes features for user creation, token generation, and validation. Additionally, it displays messages based on user roles.

## Features

- **User Creation**: Register new users with specific roles.
- **Token Generation**: Generate JWT tokens upon successful authentication.
- **User and Token Validation**: Validate users and tokens to ensure secure access.
- **Role-Based Messaging**: Display custom messages based on the user's role.

## Technologies Used

- Spring Boot
- Spring Security
- JWT (JSON Web Token)
- H2 Database (for development)

## Getting Started

### Prerequisites

- Java 11 or higher
- Maven

### Installation

1. **Clone the repository**:

```sh
git clone https://github.com/RavinduTJAY97/springboot-security-JWT-authentication.git
cd springboot-security-JWT-authentication
```

2. **Build the project**:

```sh
mvn clean install
```

3. **Run the application**:

```sh
mvn spring-boot:run
```

The application will start on `http://localhost:8080`.

## Usage

### Register a New User

To create a new user, send a POST request to `/api/auth/register` with the user details:

```json
{
    "name": "newuser",
    "password": "newUser@1234",
    "email": "newuser@gmail.com",
    "roles": "ROLE_ADMIN"
}
```

### Authenticate a User

To authenticate a user and receive a JWT token, send a POST request to `/api/auth/login` with the user credentials:

```json
{
  "username": "newuser",
  "password": "password"
}
```

You will receive a JWT token in the response, which can be used to access protected endpoints.

### Access Protected Endpoints

Include the JWT token in the Authorization header for accessing protected endpoints:

```sh
Authorization: Bearer <your_token>
```

### Role-Based Messaging

Access a protected endpoint and receive a message based on your role:

- `/api/user`: Accessible by users with the `ROLE_USER` role.
- `/api/admin`: Accessible by users with the `ROLE_ADMIN` role.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss improvements or features.

## License

This project is licensed under the MIT License.

---

Feel free to customize this README further to fit your project's specifics.
