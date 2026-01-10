# End-To-End CI/CD Pipeline with Jenkins, Docker, Kubernetes, ArgoCD, and Terraform

This project demonstrates an end-to-end CI/CD pipeline for deploying a containerized application using DevOps best practices.  
It follows a monorepo approach where application code, CI/CD configuration, Kubernetes manifests, and infrastructure automation are managed together.

## Tech Stack
- Jenkins
- Docker
- Kubernetes
- ArgoCD
- Terraform
- GitHub

## Project Overview
- Application source code is managed in GitHub.
- Jenkins pipeline builds and tests the application.
- Docker image is built and pushed to the container registry.
- Kubernetes manifests are used to deploy the application.
- ArgoCD is used for GitOps-based continuous deployment.
- Terraform is used to provision Kubernetes infrastructure components and deploy the monitoring stack.
- Application is scaled to multiple replicas for high availability.

## Infrastructure & Monitoring (Terraform)
- Terraform is used with Kubernetes and Helm providers.
- A dedicated Kubernetes namespace for monitoring is created.
- The kube-prometheus-stack is deployed using Helm.
- Prometheus and Grafana are used for cluster monitoring and observability.
- Terraform code is maintained inside the `terraform-project/` directory.

## Repository Structure
