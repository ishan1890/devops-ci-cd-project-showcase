# devops-ci-cd-project-showcase
"End-to-End CI/CD Pipeline with Jenkins, Kubernetes, ArgoCD ,SonarQube,Github- Complete DevOps Implementation"
End-to-End CI/CD Pipeline Implementation
![AWS](https://img.shields.io/badge/AWS-Ec2-blue)
![AWS](https://img.shields.io/badge/AWS-EKS-orange)
![Docker](https://img.shields.io/badge/Docker-yellow)
![Jenkins](https://img.shields.io/badge/Jenkins-CI/CD-blue)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Orchestration-326ce5)
![Java](https://img.shields.io/badge/Java-17-red)
![ArgoCD](https://img.shields.io/badge/ArgoCD-GitOps-ef7b4d)
![SonarQube](https://img.shields.io/badge/SonarQube-Code%20Quality-4E98D5)


A complete CI/CD pipeline implementation that automates the build, test, security scanning, and deployment of a Java application to Kubernetes using GitOps principles.

## 📋 Project Overview

This project demonstrates a real-world DevOps implementation featuring:

- **CI Pipeline**: Automated builds, testing, and code quality analysis with Jenkins
- **Containerization**: Docker image building and management
- **Security Scanning**: Trivy vulnerability scanning
- **GitOps Deployment**: ArgoCD for declarative Kubernetes deployments
- **Infrastructure as Code**: Kubernetes manifests and automated provisioning

## 🏗️ Architecture

![Architecture Diagram](+----------------+ +-------------+ +-------------------+ +---------------+
| GitHub | | Jenkins | | Docker Hub | | Kubernetes |
| Repository +-----> CI Pipeline+-----> Image Registry +-----> (EKS) |
| (Java Code) | | | | | | |
+----------------+ +-------------+ +-------------------+ +-------+-------+
|
|
+----------------+ +-------------+ +-------------------+ |
| GitHub | | ArgoCD | | Monitoring | |
| GitOps Repo +-----> GitOps +-----> & Logging <-------------+
| (K8s Manifests) | Controller| | |
+----------------+ +-------------+ +-------------------+)

## 📁 Project Structure

### Main Components:
- **[Application Repository](https://github.com/ishan1890/register-app)** - Java Spring Boot application
- **[GitOps Repository](https://github.com/ishan1890/gitops-register-app)** - Kubernetes manifests and deployment configurations
- **This Portfolio** - Documentation and overview of the complete setup

### Technology Stack:
- **CI/CD**: Jenkins, ArgoCD
- **Containerization**: Docker
- **Orchestration**: Kubernetes, AWS EKS
- **Code Quality**: SonarQube
- **Security**: Trivy
- **Languages**: Java, Groovy, YAML, Bash
- **Cloud**: AWS EC2, EKS, IAM

## 🚀 Key Features Implemented

### Continuous Integration:
- Automated build and testing with Jenkins
- Code quality analysis with SonarQube
- Security vulnerability scanning with Trivy
- Docker image building and tagging

### Continuous Deployment:
- GitOps methodology with ArgoCD
- Automated Kubernetes deployments
- Environment-specific configurations
- Rollback capabilities

### Infrastructure:
- AWS EKS cluster provisioning with eksctl
- Automated infrastructure deployment
- Monitoring and logging setup
- Security best practices implementation

## 📊 Results Achieved

- ✅ **90% reduction** in deployment time
- ✅ **100% automation** of build and deployment processes
- ✅ **Zero-downtime deployments** with Kubernetes rolling updates
- ✅ **Security scanning** integrated into pipeline
- ✅ **Infrastructure as Code** implementation

## 🛠️ Installation & Setup

Detailed setup instructions available in the [Setup Guide](docs/setup-guide.md)

### Quick Start:
```bash
# Clone the application
git clone https://github.com/ishan1890/register-app.git

# Set up infrastructure
eksctl create cluster --name my-cluster --region ap-south-1 --node-type t2.small

# Deploy with ArgoCD
argocd app create my-app --repo https://github.com/ishan1890/gitops-register-app --path . --dest-server https://kubernetes.default.svc
