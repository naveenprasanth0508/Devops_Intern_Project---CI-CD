# 🚀 yugixx-cicd-pipeline

> **DevOps CI/CD Pipeline Project – *YUGIXX React App Deployment on AWS***

---

## 📌 Overview

This project demonstrates how I built and automated a **CI/CD pipeline** using **Jenkins** to deploy a **React web application** to an **AWS EC2 instance** running **Nginx**.  
By integrating GitHub, Jenkins, and AWS, the goal was to reduce manual deployment steps, ensure faster and more reliable delivery, and gain practical DevOps experience.

> ⚠️ Even though the app is no longer running online, this repository **documents the process, pipeline steps, and architecture** — useful for learning, reference, or reuse.

---

## 🛠 Tech Stack & Tools Used

- **React.js** – Frontend single-page application
- **Git & GitHub** – Source code management & webhook triggering
- **Jenkins** – Automation server for build & deploy
- **AWS EC2** – Virtual server to host the app
- **Nginx** – Web server to serve React static files
- **Node.js & npm** – Build tools
- *(Future scope)* Docker & Kubernetes – for advanced containerization & scaling

---

## 🧰 Project Workflow

```mermaid
Steps: 
  A[Developer pushes code] --> B[GitHub Repository]
  B --> C[GitHub Webhook]
  C --> D[Jenkins Pipeline Trigger]
  D --> E[npm install & npm run build]
  E --> F[Deploy build to EC2 /var/www/html]
  F --> G[Nginx serves app to users]

🔧 Pipeline Stages:

✅ Stage 1 – Clone code
Clone the latest code from GitHub whenever changes are pushed.

✅ Stage 2 – Install dependencies
npm install

✅ Stage 3 – Build React app
npm run build

✅ Stage 4 – Deploy to EC2
Copy the contents of the build/ folder to /var/www/html on the EC2 instance using SCP/SSH.

📦 Implementation Steps
1️⃣ Create a React app & push to GitHub
2️⃣ Install Jenkins on local Ubuntu machine
3️⃣ Install Jenkins plugins: Git, NodeJS, Pipeline
4️⃣ Configure GitHub webhook to auto-trigger builds
5️⃣ Write Jenkinsfile with pipeline steps:
npm install
npm run build
scp build files to EC2

6️⃣ Start Nginx on EC2 to serve the app

✅ Achievements & Learning
Automated deployment reduced manual work & errors

Understood practical CI/CD with Jenkins & GitHub

Configured Nginx to serve a React SPA

Learned to use SSH keys securely for remote deployment

✏️ Future Scope
Use Docker to containerize the React app

Deploy with Kubernetes for scalability

Integrate Slack or Email notifications

Add SonarQube for static code analysis

📍 Why this repo is useful (even without code)
✅ Shows DevOps workflow & thinking
✅ Acts as a portfolio / case study
✅ Helps others learn to build a CI/CD pipeline with Jenkins & EC2
✅ Can be reused or extended in future projects

🙌 Conclusion
This project shows that with open-source tools like Jenkins, GitHub, and AWS, it’s possible to set up a robust, automated deployment workflow — even for small side projects.

"Automate what you can, so you can innovate what matters." 🚀

✅ Feel free to copy-paste directly into your repo!  
If you'd like, I can also:
* Create a sample `Jenkinsfile`
* Add badges or a project cover image

Just say **yes!** 🌱
