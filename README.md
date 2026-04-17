# CI/CD Pipeline with Jenkins, Docker, Kubernetes 🚀

## 📌 Overview
This project demonstrates an end-to-end CI/CD pipeline:
GitHub → Jenkins → Docker → Kubernetes

## ⚙️ Tech Stack
- Python (Flask)
- Docker
- Jenkins
- Kubernetes

## 🔄 Workflow
1. Developer pushes code to GitHub
2. Jenkins pipeline triggers
3. Docker image is built and pushed
4. Kubernetes deployment updated

## 🚀 Run Locally

docker build -t devops-app .
docker run -p 5000:5000 devops-app

## ☸️ Deploy to Kubernetes

kubectl apply -f k8s-deployment.yaml
