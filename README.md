# Learner Report MERN Application - Kubernetes Deployment

This repository contains Kubernetes deployment files and Helm charts for the Learner Report MERN application.

## Project Structure
learner-report-k8s/
├── backend-deployment.yaml
├── backend-service.yaml
├── frontend-deployment.yaml
├── frontend-service.yaml
├── mongodb-deployment.yaml
├── configmaps.yaml
├── helm-chart/
│ ├── Chart.yaml
│ ├── values.yaml
│ └── templates/
│ ├── backend-deployment.yaml
│ └── backend-service.yaml
└── Jenkinsfile

## Application Repositories
- Frontend: https://github.com/nikhilmathur1957/learnerReportCS_frontend
- Backend: https://github.com/nikhilmathur1957/learnerReportCS_backend

## Deployment

### Using Kubernetes Manifests
```bash
kubectl apply -f .
USING HELM
helm install learner-report-app helm-chart/
Jenkins Pipeline
The Jenkinsfile provides a complete CI/CD pipeline for automated deployment.
