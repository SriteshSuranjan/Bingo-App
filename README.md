# 🎯 Bingo App – DevSecOps Project

Welcome to the **Bingo App Deployment** project!  
This project demonstrates how to deploy a multiplayer Bingo application using modern **DevOps** and **DevSecOps** practices.

---

## 🛠️ Tools & Technologies Used

| Category            | Tools                                                                                                                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Version Control** | ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)                                                                                                            |
| **CI/CD**           | ![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)                                                                                                         |
| **Code Quality**    | ![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?style=flat-square&logo=sonarqube&logoColor=white)                                                                                                   |
| **Security**        | ![OWASP](https://img.shields.io/badge/OWASP-000000?style=flat-square&logo=owasp&logoColor=white) ![Trivy](https://img.shields.io/badge/Trivy-00979D?style=flat-square&logo=trivy&logoColor=white)              |
| **Containerization**| ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)                                                                                                            |
| **Orchestration**   | ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)                                                                                                |
| **Monitoring**      | ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white) |

---

## 🚦 Project Pipeline Stages

### ✅ Phase 1: Local Docker Deployment
- Containerize the Next.js Bingo App.
- Build Docker image and run locally.
- Use Trivy & OWASP Dependency Check for vulnerability scanning.

### 🚀 Phase 2: CI/CD Pipeline via Jenkins
- Linting, SonarQube quality analysis & security checks.
- CI with Jenkinsfile for clean, build, push and deploy.

### ☁️ Phase 3: Kubernetes (EKS) Deployment
- Deploy the app to AWS EKS using `manifest.yml`.
- Monitor with Prometheus + Grafana.

---

## 📂 Project Structure

```
Bingo-App/
├── components/
├── pages/
├── public/
├── styles/
├── utils/
├── Dockerfile
├── docker-compose.yml
├── jenkinsfile
├── manifest.yml
├── next.config.js
├── package.json
├── package-lock.json
```

---

## 🚀 Getting Started (Dev Mode)

> Node.js v16.20.2 and npm v8.19.4 are required

```bash
# Clone the repo and navigate into it
git clone https://github.com/your-username/Bingo-App.git
cd Bingo-App

# Install dependencies
npm install

# Run the app
npm run dev

# Run in background
nohup npm run dev &
```

---

## 🐳 Docker Deployment

```bash
# Build Docker Image
docker build -t bingo .

# Run Container
docker run -p 3000:3000 -d --name bingoapp bingo

# OR using Docker Compose
docker-compose up -d

# Stop containers
docker-compose down
```

---

## 🔐 Permissions Fix (Docker Group)

```bash
sudo usermod -aG docker ubuntu
sudo usermod -aG jenkins $USER
sudo systemctl restart docker
```

---

## 🎮 Gameplay Demo

Create a room where multiplayers can join and play:  
![Game Demo](https://github.com/andres0ares/bingo/blob/main/public/bingo_prev1.gif)

Live updates are synced across all players in the room:  
![Live Sync](https://github.com/andres0ares/bingo/blob/main/public/bingo_prev2.gif)

---

## 🎯 Objective

This project was built to:
- Learn **WebSockets**
- Implement multiplayer game logic
- Practice DevSecOps CI/CD deployment

The Bingo game logic is inside:
```
utils/bingo.js
```

---

## 🤝 Connect with Me

Feel free to connect and discuss DevOps or collaborations:

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sriteshsuranjan)
