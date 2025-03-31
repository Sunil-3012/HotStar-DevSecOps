# Hotstar DevSecOps CI/CD Pipeline 🚀

This project demonstrates a complete DevSecOps pipeline to deploy a Hotstar clone application on AWS using Jenkins, Docker, Terraform, Kubernetes (EKS), and security tools like SonarQube, OWASP, and Docker Scout.

## 🚧 Project Overview

A CI/CD pipeline was implemented on an EC2 instance with Ubuntu, automating both infrastructure and application deployment. The solution integrates DevSecOps practices to ensure secure, scalable, and efficient delivery.


## 🔁 Pipeline Workflow

1. Provision infrastructure using Terraform (EKS cluster)
2. Perform static code analysis using SonarQube
3. Install app dependencies and scan for vulnerabilities with OWASP
4. Build and push Docker image to Docker Hub
5. Scan Docker image with Docker Scout for CVEs
6. Deploy the application to Kubernetes (EKS) using kubectl

## 🌐 Deployment Architecture

GitHub → Jenkins → SonarQube/OWASP → Docker Build → Docker Scout → EKS (via Terraform & kubectl)


## 🏗️ Infrastructure Setup

- EC2 instance (Ubuntu 24) used as Jenkins master
- EKS cluster provisioned via Terraform
- Kubernetes deployment files (deployment.yaml, service.yaml)
- Jenkins with pre-installed tools: Java, SonarQube, Node.js, Docker, Terraform, kubectl, AWS CLI
- Secure credentials management through Jenkins Secrets

## 🛠️ Tech Stack

- **CI/CD**: Jenkins, GitHub, Maven
- **Infrastructure**: AWS EC2, EKS, IAM, Terraform
- **Security**: SonarQube, OWASP Dependency-Check, Docker Scout
- **Containers & Orchestration**: Docker, Kubernetes
- **Automation**: Ansible (Jenkins → App Server Deployment)
- **Languages**: JavaScript (Node.js), YAML, Bash

## ⚙️ Pipeline Workflow

1. **Code Checkout**: Pulls latest code from GitHub repo
2. **Static Analysis**: SonarQube scan with quality gate enforcement
3. **Security Scan**: OWASP checks for vulnerable dependencies
4. **Dockerization**: Builds and pushes Docker image to Docker Hub
5. **Image Security**: Docker Scout scans for CVEs and recommendations
6. **Deployment**: Jenkins deploys app to EKS using kubectl
7. **Monitoring**: `kubectl get svc -o wide` to verify live service

## 🧪 Security Integration

- **SonarQube**: Code quality analysis with webhook integration and quality gate enforcement.
- **OWASP Dependency-Check**: Identifies vulnerabilities in packages and generates reports.
- **Docker Scout**: Scans for container vulnerabilities and suggests remediations.

## ✅ Key Benefits

- Fully automated and secure CI/CD workflow
- Seamless infrastructure provisioning with Terraform
- Built-in static and dynamic security scanning
- Scalable application deployment using AWS EKS
- End-to-end DevSecOps implementation from code to production

---

## 📌 Next Steps

- Integrate Helm charts for better Kubernetes management
- Add Slack/Webhook notifications for pipeline status
- Use Prometheus and Grafana for application monitoring
- Implement GitOps using ArgoCD or Flux

---

> 👨‍💻 Created by Sunil Gangupamu | AWS Certified Solutions Architect | DevOps Enthusiast

