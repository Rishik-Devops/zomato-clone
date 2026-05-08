# Zomato Clone – End-to-End DevSecOps CI/CD Pipeline on AWS EKS


# Project Overview

This project demonstrates an enterprise-style **DevSecOps CI/CD Pipeline** for deploying a **Zomato Clone Application** using modern DevOps tools and cloud-native technologies.

The application is integrated with:

* Continuous Integration using Jenkins
* Static Code Analysis using SonarQube
* Security Scanning using OWASP Dependency Check & Trivy
* Containerization using Docker
* Container Registry using DockerHub
* Kubernetes Deployment on AWS EKS
* GitOps deployment using ArgoCD
* Monitoring using Prometheus & Grafana

The primary objective of this project is to implement a complete production-style DevSecOps workflow from code commit to Kubernetes deployment and monitoring.

---

# Repository

GitHub Repository:

```bash
https://github.com/Rishik-Devops/zomato-clone.git
```

DockerHub Repository:

```bash
https://hub.docker.com/repositories/rishik21
```

---

# Architecture Diagram

> Add architecture diagram inside:

```bash
architecture/devsecops-architecture.png
```

## DevSecOps Workflow

```text
Developer
   ↓
GitHub Repository
   ↓
Jenkins CI/CD Pipeline
   ↓
SonarQube Analysis
OWASP Dependency Check
Trivy Security Scan
Docker Scout Scan
   ↓
Docker Image Build
   ↓
DockerHub Push
   ↓
AWS EKS Cluster
   ↓
ArgoCD GitOps Deployment
   ↓
Kubernetes Deployment
   ↓
Prometheus Monitoring
   ↓
Grafana Dashboards
```

---

# Tech Stack

| Category                | Technologies Used                           |
| ----------------------- | ------------------------------------------- |
| Cloud Platform          | AWS                                         |
| CI/CD                   | Jenkins                                     |
| Source Code Management  | GitHub                                      |
| Code Quality            | SonarQube                                   |
| Security Scanning       | OWASP Dependency Check, Trivy, Docker Scout |
| Containerization        | Docker                                      |
| Container Registry      | DockerHub                                   |
| Container Orchestration | Kubernetes                                  |
| Kubernetes Platform     | AWS EKS                                     |
| GitOps                  | ArgoCD                                      |
| Monitoring              | Prometheus, Grafana                         |
| Application Runtime     | Node.js                                     |

---

# CI/CD Pipeline Stages

The Jenkins pipeline automates the entire DevSecOps workflow.

## Pipeline Stages

1. Clean Workspace
2. Git Checkout
3. SonarQube Analysis
4. Quality Gate Validation
5. Install NPM Dependencies
6. OWASP Dependency Check
7. Trivy File System Scan
8. Docker Image Build
9. Push Docker Image to DockerHub
10. Docker Scout Scan
11. Deploy Application Container

---

# Jenkins Pipeline Screenshot

![Jenkins Pipeline](screenshots/03-jenkins-pipeline.jpeg)

---

# Code Quality & Security

## SonarQube Analysis

SonarQube is integrated with Jenkins to perform:

* Static Code Analysis
* Code Smell Detection
* Vulnerability Detection
* Quality Gate Validation

### SonarQube Dashboard

![SonarQube](screenshots/04-sonarqube-dashboard.jpeg)

---

## Security Scanning

This project implements multiple layers of security scanning:

### OWASP Dependency Check

* Detects vulnerable dependencies
* Identifies CVEs in third-party libraries

### Trivy Scan

* File system vulnerability scanning
* Container vulnerability scanning

### Docker Scout

* Container image recommendations
* Vulnerability insights

---

# Docker & Containerization

The application is containerized using Docker and pushed to DockerHub.

## DockerHub Repository

![DockerHub](screenshots/05-dockerhub-image.jpeg)

---

# AWS Infrastructure

## AWS EC2 Instances

Separate EC2 instances are used for:

* Jenkins Server
* Monitoring Server
* EKS Worker Nodes

### Infrastructure Screenshot

![AWS Infrastructure](screenshots/01-aws-instances.jpeg)

---

# Network & Security Configuration

Security Groups are configured with required ports:

| Service       | Port  |
| ------------- | ----- |
| Jenkins       | 8080  |
| SonarQube     | 9000  |
| Prometheus    | 9090  |
| Grafana       | 3000  |
| Node Exporter | 9100  |
| Application   | 30001 |

### Security Group Configuration

![Security Groups](screenshots/02-security-groups.jpeg)

---

# Kubernetes Deployment on AWS EKS

The application is deployed to AWS EKS using Kubernetes manifests.

## EKS Cluster

![EKS Cluster](screenshots/09-eks-cluster.jpeg)

---

# GitOps Deployment using ArgoCD

ArgoCD continuously monitors the GitHub repository and synchronizes Kubernetes manifests automatically.

## ArgoCD Application Status

![ArgoCD Status](screenshots/10-argocd-status.jpeg)

## ArgoCD Deployment Tree

![ArgoCD Deployment](screenshots/11-argocd-deployment.jpeg)

---

# Monitoring & Observability

## Prometheus Monitoring

Prometheus is configured to monitor:

* Jenkins Metrics
* Node Exporter Metrics
* Kubernetes Metrics
* Application Metrics

### Prometheus Targets

![Prometheus](screenshots/06-prometheus-targets.jpeg)

---

## Grafana Dashboards

Grafana dashboards provide real-time monitoring and visualization.

### Node Exporter Dashboard

![Grafana Node Exporter](screenshots/07-grafana-node-exporter.jpeg)

### Jenkins Monitoring Dashboard

![Grafana Jenkins](screenshots/08-grafana-jenkins.jpeg)

---

# Application Deployment

The final application is successfully deployed and accessible through Kubernetes.

## Application Homepage

![Zomato Homepage](screenshots/12-zomato-homepage.jpeg)

## Application Features

![Zomato Features](screenshots/13-zomato-features.jpeg)

---

# Project Structure

```text
zomato-clone/
│
├── Kubernetes/
├── screenshots/
├── architecture/
├── Jenkinsfile
├── Dockerfile
├── package.json
├── README.md
└── src/
```

---

# How to Run the Project

## Clone Repository

```bash
git clone https://github.com/Rishik-Devops/zomato-clone.git
```

## Build Docker Image

```bash
docker build -t zomato .
```

## Run Container

```bash
docker run -d -p 3000:3000 zomato
```

---

# Future Enhancements

* Implement Terraform for Infrastructure as Code
* Add Helm Charts for Kubernetes deployments
* Configure HTTPS with Ingress Controller
* Integrate Slack Notifications
* Add Automated Backup Strategy
* Implement Horizontal Pod Autoscaling
* Add Blue-Green Deployment Strategy

---

# Key Learning Outcomes

This project helped in gaining hands-on experience with:

* CI/CD Pipeline Automation
* DevSecOps Best Practices
* Kubernetes Deployment Strategies
* GitOps Workflows
* Monitoring & Observability
* AWS EKS Administration
* Container Security Scanning
* Production-style Deployment Architecture

---

# Author

## Rishik Teratiaplli

### DevOps | Cloud | Kubernetes | AWS

GitHub:

```bash
https://github.com/Rishik-Devops
```

DockerHub:

```bash
https://hub.docker.com/u/rishik21
```

---

# Project Status

✅ Completed

This project demonstrates a complete DevSecOps workflow with CI/CD automation, Kubernetes deployment, GitOps, monitoring, and security scanning integrated into a production-style architecture.
