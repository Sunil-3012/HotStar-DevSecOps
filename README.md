# Hotstar DevSecOps CI/CD Pipeline 🚀

This project demonstrates a complete DevSecOps pipeline to deploy a Hotstar clone application on AWS using Jenkins, Docker, Terraform, Kubernetes (EKS), and security tools like SonarQube, OWASP, and Docker Scout.

## 🚧 Project Overview

A CI/CD pipeline was implemented on an EC2 instance with Ubuntu, automating both infrastructure and application deployment. The solution integrates DevSecOps practices to ensure secure, scalable, and efficient delivery.

## 🔧 Tools & Technologies

- **CI/CD**: Jenkins, GitHub, Maven
- **Infrastructure**: Terraform, AWS EKS, EC2, IAM
- **Security**: SonarQube, OWASP Dependency-Check, Docker Scout
- **Containers & Orchestration**: Docker, Kubernetes (kubectl)
- **Automation**: Ansible
- **Languages**: JavaScript (Node.js), YAML, Bash

## 📦 Jenkins Pipeline Features

- **Terraform**: Provisions EKS cluster with backend S3 and remote state locking.
- **SonarQube**: Performs static code analysis and enforces quality gates.
- **OWASP**: Scans for known vulnerabilities in dependencies.
- **Docker Build & Push**: Builds container image and pushes it to Docker Hub.
- **Docker Scout**: Analyzes image CVEs and security risks.
- **Kubernetes Deployment**: Applies deployment and service manifests to EKS.
- **Environments**: Dev and Prod environment switching using Jenkins parameters.

## 🧪 Security Integration

- **SonarQube**: Code quality analysis with webhook integration and quality gate enforcement.
- **OWASP Dependency-Check**: Identifies vulnerabilities in packages and generates reports.
- **Docker Scout**: Scans for container vulnerabilities and suggests remediations.

## 🌐 Deployment Architecture

GitHub → Jenkins → SonarQube/OWASP → Docker Build → Docker Scout → EKS (via Terraform & kubectl)


## 🛠️ How It Works

1. Jenkins pulls code from GitHub and performs SonarQube analysis.
2. Terraform provisions the Kubernetes cluster (EKS).
3. Docker image is built, scanned, and pushed to Docker Hub.
4. Kubernetes deployment is triggered with `kubectl` using credentials stored in Jenkins.
5. Final service is exposed on EKS with LoadBalancer IP.

## ✅ Outcome

- Full CI/CD automation with security gates
- Infrastructure as Code with Terraform
- Secure, scalable Hotstar clone deployed on AWS

---

> 👨‍💻 Created by Sunil Gangupamu | AWS Certified Solutions Architect | DevOps Enthusiast

