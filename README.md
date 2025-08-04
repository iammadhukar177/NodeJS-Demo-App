# 📦 nodejs-demo-app

A simple **Node.js** application deployed using a **CI/CD pipeline** powered by **GitHub Actions** and **DockerHub**. Every push to the `main` branch automatically builds and pushes a Docker image to DockerHub.

---

## 🚀 Features

- Node.js + Express app
- Dockerized setup
- GitHub Actions CI/CD
- Automated DockerHub deployment
- Trigger on push to `main` branch

---

## 🧾 Prerequisites

- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/)
- [GitHub account](https://github.com/)
- [DockerHub account](https://hub.docker.com/)

---

## 📁 Project Structure

```
nodejs-demo-app/
│
├── index.js                # Main Node.js application
├── package.json            # App metadata and dependencies
├── Dockerfile              # Docker image definition
└── .github/
    └── workflows/
        └── main.yml        # CI/CD pipeline definition
```

---

## 🛠️ Setup Instructions

### 1. Clone this repository

```bash
git clone https://github.com/<your-username>/nodejs-demo-app.git
cd nodejs-demo-app
```

### 2. Install dependencies (for local testing)

```bash
npm install
npm start
```

---

## 🐳 Docker Setup

### Build Docker Image

```bash
docker build -t nodejs-demo-app .
```

### Run Docker Container

```bash
docker run -p 3000:3000 nodejs-demo-app
```

Open browser at: [http://localhost:3000](http://localhost:3000)

---

## 🔄 CI/CD Pipeline Workflow

The CI/CD pipeline is defined in:  
`.github/workflows/main.yml`

### What it does:

- ✅ On push to `main`:
  - Checkout code
  - Log in to DockerHub
  - Build Docker image
  - Push image to DockerHub

---

## 🔐 GitHub Secrets

Set the following repository secrets in **GitHub → Settings → Secrets → Actions**:

| Secret Name         | Description                         |
|---------------------|-------------------------------------|
| `DOCKER_USERNAME`   | Your DockerHub username             |
| `DOCKER_PASSWORD`   | Your DockerHub access token/password|

---

## 📦 DockerHub Deployment

The final Docker image will be available at:

```
https://hub.docker.com/r/<your-dockerhub-username>/nodejs-demo-app
```

---

## 🧪 Example Output

Once the container is running, visit:

```
http://localhost:3000
```

You should see:

```
Hello from Node.js Demo App!
```

---

## 🙌 Acknowledgements

- [GitHub Actions](https://github.com/features/actions)
- [DockerHub](https://hub.docker.com/)
- [Node.js](https://nodejs.org/)
