# End-To-End CI/CD Pipeline with Jenkins, Docker, Kubernetes, and ArgoCD

This project demonstrates an end-to-end CI/CD pipeline for deploying a containerized application using DevOps best practices.

## Tech Stack
- Jenkins
- Docker
- Kubernetes
- ArgoCD
- GitHub
- Terraform

## Project Overview
- Application source code is managed in GitHub.
- Jenkins pipeline builds and tests the application.
- Docker image is built and pushed to the container registry.
- Kubernetes manifests are used to deploy the application.
- ArgoCD is used for GitOps-based continuous deployment.
- Application is scaled to multiple replicas for high availability.

## Repository Structure
├── app.py
├── requirements.txt
├── Dockerfile
├── Jenkinsfile
├── k8s/
│ ├── deployment.yaml
│ └── service.yaml
└── extras/
├── terraform-project/
│   ├── main.tf
│   ├── README.md 
│   └── .gitignore
└── README.md

## CI/CD Flow
GitHub → Jenkins → Docker → Kubernetes → ArgoCD

## How to Run
1. Build Docker image using Jenkins pipeline.
2. Push image to container registry.
3. Apply Kubernetes manifests.
4. Monitor deployment using kubectl and ArgoCD.

## Outcome
- Automated build and deployment pipeline
- GitOps-based deployment
- Scalable Kubernetes application

