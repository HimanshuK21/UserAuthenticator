User Authentication API

**Overview**
- **Project**: Backend API for user authentication (registration, login, token issuance).
- **Purpose**: Provide secure authentication endpoints and issue JWTs to the UI.

**Tech Stack**
- **Framework**: Spring Boot (Java)
- **Build**: Maven

**Prerequisites**
- **Java JDK**: 17+ installed
- **Maven**: bundled wrapper available (`mvnw` / `mvnw.cmd`)

**Configuration**
- Use `src/main/resources/application.properties` or environment variables to configure:
  - **JWT secret** (e.g., `JWT_SECRET`)
  - **Database connection** (`spring.datasource.*` or other DB-specific settings)
  - **Server port** (`server.port`)

**Run Locally**
- Using the Maven wrapper (Linux/macOS): `./mvnw spring-boot:run`
- On Windows PowerShell / CMD: `mvnw.cmd spring-boot:run`
- Build artifact: `./mvnw package` then `java -jar target/<artifact>.jar`

**Docker / Compose**
- A `compose.yaml` is provided for containerized runs; use `docker compose up --build`.

**Typical Endpoints**
Note: Confirm exact paths in the code; these are common defaults and may differ.
- `POST /api/auth/register` — register a new user
- `POST /api/auth/login` — authenticate and return a JWT
- `POST /api/auth/refresh` — refresh tokens (if implemented)
- `GET /api/auth/me` — get current authenticated user info

**Testing**
- Run unit and integration tests: `./mvnw test`

**Troubleshooting**
- If startup fails due to DB connectivity, verify the connection string and credentials.
- For JWT issues, ensure the `JWT_SECRET` used by the UI and backend match the expected format.

If you'd like, I can add example `application.properties`, Postman collection, or update the README with exact endpoints after scanning the controller classes.
