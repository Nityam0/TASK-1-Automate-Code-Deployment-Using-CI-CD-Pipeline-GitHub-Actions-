# Task 1 – Automate Code Deployment Using CI/CD Pipeline (GitHub Actions)

##  Project Overview

This project demonstrates an automated CI/CD pipeline using:

- Node.js
- Docker
- GitHub Actions
- DockerHub

The pipeline automatically builds and pushes a Docker image to DockerHub whenever code is pushed to the `main` branch.

---

## 🛠️ Tech Stack

- Node.js (Express App)
- Docker
- GitHub
- GitHub Actions
- DockerHub

---

## 📂 Project Structure
                                                   ** steps to create project**

### Step 1 – Create Node.js Application
- Create a ec2 in aws.
- add sg on 3000. (Application runs on port 3000.)
- then create folder nodejs-demo-app
- '''bash''''
        cd nodejs-demo-app
        npm init -y
        npm install express
- create index.js
- update the package.json
- Tested the app locally using `node index.js`.

---

### Step 2 – Create Dockerfile
- Created a Dockerfile for the Node.js app.
- Built Docker image using:
  docker build -t nodejs-cicd-demo .
- Ran container locally to verify it works.

---

### Step 3 – Push Code to GitHub
- Initialized Git repository.
- Added project files.
- Pushed code to GitHub main branch.

---

### Step 4 – Create GitHub Actions Workflow
- Created folder: .github/workflows/
- Added main.yml file.
- Defined CI/CD pipeline that triggers on push to main branch.

---

### Step 5 – Configure GitHub Secrets
- Added DOCKER_USERNAME.
- Added DOCKER_PASSWORD.
- Used secrets to securely login to DockerHub.

---

### Step 6 – Create DockerHub Repository
- Created repository named: nodejs-cicd-demo.
- Made it public.

---

### Step 7 – Automatic CI/CD Execution
- Pushed new code to GitHub.
- GitHub Actions automatically:
  - Installed dependencies
  - Built Docker image
  - Logged into DockerHub
  - Pushed Docker image

---

## ✅ Final Result
- CI/CD pipeline working successfully.
- Docker image automatically pushed on every code change.
- Full automation implemented.
