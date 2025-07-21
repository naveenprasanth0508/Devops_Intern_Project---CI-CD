# 🚀 yugixx-cicd-pipeline

> **DevOps CI/CD Pipeline Project – *YUGIXX React App Deployment on AWS***

---

## 📌 Overview

This project demonstrates how I built and automated a **CI/CD pipeline** using **Jenkins** to deploy a **React web application** to an **AWS EC2 instance** running **Nginx**.  
By integrating GitHub, Jenkins, and AWS, the goal was to reduce manual deployment steps, ensure faster and more reliable delivery, and gain practical DevOps experience.

> ⚠️ Even though the app is no longer running online, this repository **documents the process, pipeline steps, and architecture** — making it useful for learning, reference, or reuse.

---

## 🛠 Tech Stack & Tools Used:

- **React.js** – Frontend single-page application
- **Git & GitHub** – Source code management & webhook triggering
- **Jenkins** – Automation server for build & deploy
- **AWS EC2** – Virtual server to host the app
- **Nginx** – Web server to serve React static files
- **Node.js & npm** – Build tools
- *(Future scope)* Docker & Kubernetes – for advanced containerization & scaling

---

🔧 Pipeline Stages:

✅ Stage 1 – Clone code
Clone the latest code from GitHub whenever changes are pushed.

✅ Stage 2 – Install dependencies
npm install

✅ Stage 3 – Build React app
npm run build

✅ Stage 4 – Deploy to EC2
Copy the contents of the build/ folder to /var/www/html on the EC2 instance using SCP/SSH.

✅ Achievements & Learning:
- Automated deployment reduced manual work & errors
- Understood practical CI/CD with Jenkins & GitHub
- Configured Nginx to serve a React SPA
- Learned to use SSH keys securely for remote deployment

---

✏️ Future Scope:
- Use Docker to containerize the React app
- Deploy with Kubernetes for scalability
- Integrate Slack or Email notifications
- Add SonarQube for static code analysis

---

## 🧰 Project Workflow

```mermaid
graph TD
  A[Developer pushes code] --> B[GitHub Repository]
  B --> C[GitHub Webhook]
  C --> D[Jenkins Pipeline Trigger]
  D --> E[npm install & npm run build]
  E --> F[Deploy build to EC2 /var/www/html]
  F --> G[Nginx serves app to users]



