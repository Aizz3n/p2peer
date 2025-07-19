# P2Peer

![P2Peer Logo](docs/assets/logo.png)

**100% Bitcoin decentralized marketplace, no KYC, powered by Lightning Network.**

## 📖 Overview

P2Peer is a peer-to-peer platform for buying and selling physical products, using exclusively Bitcoin as the payment method. Our goal is to offer an experience **without intermediaries**, **without identity verification (KYC)**, focusing on **privacy**, **financial sovereignty**, and the **circular economy**.

## 🚀 Features

- **Anonymous Login** via LNURL-auth (future Nostr support)  
- **Product CRUD**: create, edit, list, and delete listings  
- **Lightning Payments**: invoice generation and instant confirmation  
- **Transaction History**: track your sales and purchases  
- **P2P Chat**: direct negotiation between buyer and seller  
- **Reputation System**: star ratings and comments  

## 🛠 Tech Stack

- **Backend**: Java 17+, Spring Boot 3, Spring Security  
- **Database**: PostgreSQL + Hibernate (JPA)  
- **Frontend**: React.js + Tailwind CSS (MVP)  
- **Payments**: LNbits API / BTCPay Server (fallback)  
- **Image Storage**: IPFS or MinIO  
- **Authentication**: LNURL-auth (JWT)  
- **Infrastructure**: Docker, Nginx, VPS (Hetzner/Fly.io)  
- **Monitoring**: Prometheus + Grafana / Sentry  
- **CI/CD**: GitHub Actions  

## 📂 Project Structure

```bash
p2peer/
├── backend/             # Spring Boot application
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/p2peer
│   │   │   │   ├── config/        # Security, CORS configurations
│   │   │   │   ├── controller/    # REST endpoints
│   │   │   │   ├── model/         # JPA entities
│   │   │   │   ├── repository/    # Persistence interfaces
│   │   │   │   ├── service/       # Business logic
│   │   │   │   └── P2PeerApplication.java
│   │   │   └── resources/
│   │   │       ├── application.yml
│   │   │       └── db/migration  # Flyway scripts
│   │   └── test/                # JUnit + Mockito tests
│   └── Dockerfile
├── frontend/            # React SPA (separate folder or monorepo)
├── docs/                # Additional docs (Wireframes, API)
│   └── assets/          # Images, logos
├── .github/             # CI/CD workflows
└── README.md
```

## ⚙️ Installation and Local Setup

1. **Prerequisites**: Java 17+, Maven, Node.js, Docker  
2. Clone the repository:
   ```bash
   git clone https://github.com/your-username/p2peer.git
   cd p2peer
   ```
3. Configure `application.yml` in `backend/src/main/resources` with your PostgreSQL connection and LNbits keys.  
4. Start the backend:
   ```bash
   cd backend
   mvn clean spring-boot:run
   ```
5. Start the frontend:
   ```bash
   cd frontend
   npm install
   npm start
   ```
6. Access the app at `http://localhost:3000`.

## 📑 API Documentation

Automatically generated with **Swagger UI**:  
`http://localhost:8080/swagger-ui/index.html`

## 🧪 Tests

Run all tests:
```bash
cd backend
mvn test
```

## 🚚 Deployment

Pipelines configured in `.github/workflows` for Docker build and deploy:  
- Image build  
- Push to Docker Hub or private registry  
- Deploy to server via SSH or Kubernetes  

## 🤝 Contribution

1. Fork this repository  
2. Create a feature branch: `git checkout -b feature/new-feature`  
3. Commit your changes: `git commit -m 'Add new feature'`  
4. Push the branch: `git push origin feature/new-feature`  
5. Open a Pull Request  

See `CONTRIBUTING.md` for details.

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

*P2Peer — Buy, sell, and trade freely. No banks. No KYC. Only Bitcoin.*

---
