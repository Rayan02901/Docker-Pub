\# Production Setup (Docker)



This folder contains the production-ready Docker setup for the \*\*Auth Microservice\*\*.



The application is designed to run \*\*only inside Docker in production\*\* to ensure:



\- Environment consistency

\- Isolated runtime dependencies

\- Secure authentication configuration

\- Real-world deployment parity





\## 🛠 Tech Stack (Prod)



\- ASP.NET Core (.NET)

\- JWT Authentication

\- Swagger (OpenAPI)

\- Docker

\- Docker Compose





\## 📁 Structure



auth-microservice/

│

├── build/ # Published .NET build output

├── Dockerfile # Runtime image definition

├── docker-compose.yml # Service orchestration

├── appsettings.json # Base configuration

├── README.md

└── INSTRUCTIONS.txt







\## 🔐 Security Notes



\- JWT secrets are NOT hardcoded

\- Sensitive configuration is injected at runtime

\- Published binaries are used (no SDK in container)

\- Authentication tokens are issued and validated securely

\- Docker isolates the runtime environment





\## 🚀 Deployment Philosophy



This setup reflects how authentication microservices are deployed in

real-world backend systems:



\- Pre-published, immutable application binaries

\- Minimal runtime Docker images

\- Environment-driven configuration

\- Stateless JWT-based authentication

\- Single-command startup using Docker Compose





\## ▶️ How This Service Is Used



The Auth Microservice provides:



\- User login

\- JWT generation

\- Token verification

\- Token refresh

\- Health check endpoint



It is intended to be consumed by other backend services

(e.g., Crypto Security Microservice) via internal APIs.





\## ⚠️ Important Notes



\- The `build/` folder MUST exist before running Docker

\- This service is not meant to be run via `dotnet run` in production

\- Swagger is enabled for validation and testing

\- Unit tests are not executed inside the production container

\- This setup simulates enterprise-grade deployment patterns

