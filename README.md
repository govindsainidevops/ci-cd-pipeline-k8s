# CI/CD Pipeline with Jenkins, Docker, Kubernetes 🚀

## 📌 Overview
This project demonstrates an end-to-end CI/CD pipeline:
GitHub
   ↓
Jenkins
   ↓
Docker Build
   ↓
Docker Hub
   ↓
Kubernetes (docker Desktop - Kubenetes)
   ↓
Prometheus + Grafana


## ⚙️ Tech Stack
- Python (Flask)
- Docker
- Jenkins
- Kubernetes

## 🔄 Workflow
1. Developer pushes code to GitHub
2. Jenkins pipeline triggers
3. Docker image is built and pushed
4. Kubernetes deployment updated manually in my local

## 🚀 Run Locally

docker build -t devops-app .
docker run -p 5000:5000 devops-app

## ☸️ Deploy to Kubernetes locally in Docker Desktop - kubernetes

kubectl apply -f k8s-deployment.yaml
kubectl apply -f prometheus-deployment.yaml
kubectl apply -f grafana-deployment.yaml

## 📊 Monitoring Dashboard

### Grafana Dashboard
![Grafana](docs/grafana-dashboard.png)

### Prometheus Targets
![Prometheus](docs/prometheus-targets.png)


Additional Commands which can be used depending on setup 


kubectl port-forward svc/prometheus-service 9090:9090
kubectl port-forward svc/devops-service 8081:80
kubectl port-forward svc/grafana-service 3000:3000

Command to manually invoke incoming request in browser. 

while ($true) { Invoke-WebRequest http://localhost:8081 }

✅ Flask app
✅ Dockerized app
✅ Kubernetes deployment
✅ Jenkins CI/CD
✅ Prometheus monitoring
✅ Grafana dashboards
✅ Kubernetes networking
✅ Real observability stack