# 🚀CI-CD-for-Node.js-Application
This project implements a **complete CI/CD pipeline** for a Node.js application using **Jenkins, AWS EC2, and GitHub integration**.  
The pipeline automates **build, test, and deployment** whenever code changes are pushed to the repository.

---

## 🏗️ Architecture Diagram
![](./img/Screenshot%202025-11-07%20171608.png)

---

## ⚙️ Pipeline Components

### 1. 🧠 Source Control (GitHub)
- **Repository:** `CI-CD-for-Node.js-Application`
- **Branches:** `main`
- **Webhooks:** Configured for automatic Jenkins build triggers
- **Files:**
  - `app.js` → Node.js application code  
  - `Jenkinsfile` → Pipeline configuration  
  - `package.json` → Dependencies and scripts  

### 2. 🧩 CI/CD Server (Jenkins)
- **Pipeline Name:** `node-app-deployment`
- **Configuration:** GitHub SCM integration with webhook triggers  
- **Pipeline Script:** Pulled from SCM (`Jenkinsfile`)  
- **Build Status:** Successful deployments tracked via Jenkins dashboard  

### 3. ☁️ Deployment Target (AWS EC2)
- **Instance:** `node-app-deployment (i-027870cd570812ea6)`  
- **Region:** `us-east-1`
- **Network:**  
  - Public IPv4: `3.95.174.55`  
  - Private IPv4: `172.31.30.197`  

---


### 2️⃣ AWS EC2 Dashboard
![](./img/Screenshot%202025-11-05%20231406.png)

### 3️⃣ GitHub Repository & Webhook
![](./img/Screenshot%202025-11-07%20172201.png)
![](./img/Screenshot%202025-11-05%20232418.png)

### 4️⃣ Jenkins Pipeline Dashboard
![](./img/Screenshot%202025-11-07%20173502.png)

### 5️⃣ Jenkins Job Configuration
![](./img/Screenshot%202025-11-05%20233631.png)

### 6️⃣ Successful Deployment Output
![](./img/Screenshot%202025-11-05%20231501.png)

---

## 🔁 Pipeline Workflow Overview

| Stage | Description |
|--------|-------------|
| **1. Code Commit** | Developer pushes changes to GitHub repository |
| **2. Webhook Trigger** | GitHub triggers Jenkins pipeline via webhook |
| **3. Build Execution** | Jenkins pulls latest code and installs dependencies |
| **4. Deployment** | Application deployed to AWS EC2 instances |
| **5. Verification** | Health checks and status monitoring performed |

---
## 🌟 Features

✅ Automated builds on every code change

✅ Zero-downtime deployments

✅ Multi-environment support(Production Staging)

✅ Rollback capabilities

✅ Build status notifications

✅ Comprehensive monitoring

---

## 🧰 Technologies Used


| Component       | Technology       |
| --------------- | ---------------- |
| Version Control | GitHub           |
| CI/CD Server    | Jenkins          |
| Cloud Provider  | AWS EC2          |
| Application     | Node.js          |
| Orchestration   | Jenkins Pipeline |
| Integration     | GitHub Webhooks  |

---

## 🛠️ Getting Started
### Prerequisites

* Jenkins server with necessary plugins

* AWS EC2 instances configured

* GitHub repository with webhooks

* Node.js application code

### Setup Instructions

* Configure Jenkins pipeline with GitHub repository URL

* Set up AWS EC2 instances in target regions

* Configure GitHub webhooks for Jenkins integration

* Define deployment scripts in Jenkinsfile

* Test the pipeline with sample deployments

---

## 📊 Monitoring and Logs

* Jenkins build history and console output

* AWS EC2 instance status checks

* GitHub webhook delivery status

* Application health endpoints

---     