# Production Setup (Docker)

This folder contains the **production-ready Docker setup** for the Security Microservice.

The application is designed to run **only inside Docker** in production to ensure:
- Environment consistency
- Isolated dependencies
- Secure configuration handling

---

## 🛠 Tech Stack (Prod)

- Python (Docker image)
- FastAPI
- Cryptography (Fernet)
- Loguru
- Docker
- Docker Compose

---

## 📁 Structure

crypto-microservice/
│
├── app/ # Application source code
├── requirements.txt # Production dependencies
├── Dockerfile # Application image definition
├── docker-compose.yml # Service orchestration
├── .env.prod # Production environment variables
├── README.md
└── INSTRUCTIONS.txt


---

## 🔐 Security Notes

- Secrets are injected via `.env.prod`
- No secrets are committed into source code
- Production configuration is environment-driven

---

## 🚀 Deployment Philosophy

This setup reflects how backend microservices are commonly deployed:
- Immutable Docker images
- Externalized configuration
- Single-command startup using Docker Compose