# API-Gateway

This project is an API Gateway built with Java and Spring Cloud Gateway. It acts as a single entry point for routing requests to various microservices, handling authentication, and providing security features.

## Features
- **Routing**: Forwards client requests to appropriate backend microservices.
- **Authentication**: Uses JWT-based authentication to secure endpoints.
- **Security**: Configurable security filters and route validation.
- **Centralized Entry Point**: Simplifies client interaction with multiple microservices.

## Project Structure
```
API-Gateway/
├── src/
│   ├── main/
│   │   ├── java/com/example/api_gateway/
│   │   │   ├── ApiGatewayApplication.java
│   │   │   ├── config/SecurityConfig.java
│   │   │   └── security/
│   │   │       ├── AuthenticationFilter.java
│   │   │       ├── JwtUtil.java
│   │   │       └── RouteValidator.java
│   │   └── resources/
│   │       ├── application.properties
│   │       └── application.yml
│   └── test/
│       └── java/com/example/api_gateway/
├── pom.xml
└── ...
```

## Getting Started

### Prerequisites
- Java 17 or later
- Maven 3.6+

### Build and Run
1. **Clone the repository**
2. **Build the project**:
   ```
   ./mvnw clean install
   ```
3. **Run the application**:
   ```
   ./mvnw spring-boot:run
   ```
   Or run the generated JAR:
   ```
   java -jar target/api-gateway-0.0.1-SNAPSHOT.jar
   ```

### Configuration
- Edit `src/main/resources/application.yml` or `application.properties` to configure routes, authentication, and other gateway settings.

## Security
- JWT tokens are validated for protected routes.
- Security configuration is managed in `SecurityConfig.java` and `AuthenticationFilter.java`.

## Customization
- Add or modify routes in the configuration files.
- Implement additional filters or validators as needed.

## License
This project is licensed under the MIT License.

