# ☁️ Infrastructure and Web Application Overview

##  Overview
Welcome to the **Amit-Tomar-Cloud** organization — a complete cloud-native solution demonstrating **Infrastructure as Code (IaC)**, **Backend API Development**, and **Serverless Architecture** on AWS.

This organization contains **three main repositories**, each representing a key component of a modern cloud environment:

- **[TF AWS Infra](https://github.com/Amit-Tomar-Cloud/tf-aws-infra)** — Terraform-based AWS infrastructure provisioning.  
- **[WebApp](https://github.com/Amit-Tomar-Cloud/webapp)** — Node.js backend API with PostgreSQL and Express.  
- **[Serverless](https://github.com/Amit-Tomar-Cloud/serverless)** — AWS Lambda-based email verification service using Mailgun.  

Together, these projects form a **scalable, secure, and automated cloud platform** following DevOps and CI/CD best practices.

---

##  Infrastructure Architecture
<img width="1116" height="584" alt="Cloud Infra Diagram" src="https://github.com/user-attachments/assets/3264eab9-0a0b-4321-a600-4e23af457a38" />

**Architecture Highlights:**
- Terraform-managed AWS resources  
- VPC with public/private subnets  
- EC2 for web application hosting  
- RDS for persistent data storage  
- S3 for asset storage  
- Lambda for event-driven automation  
- CloudWatch for monitoring and metrics  

---

##  Repositories Overview

### **1. [TF AWS Infra](https://github.com/Amit-Tomar-Cloud/tf-aws-infra)**
This repository provisions the **AWS networking and compute infrastructure** using **Terraform**.

**Key Features:**
- VPC, subnets, Internet Gateway, and route tables  
- Security Groups, EC2 instances, and Auto Scaling Groups  
- RDS, S3, and CloudWatch monitoring setup  
- SSL certificate import via AWS ACM  
- Fully parameterized configuration via `terraform.tfvars`  

**Tech Stack:** Terraform, AWS CLI, GitHub Actions  

---

### **2. [WebApp](https://github.com/Amit-Tomar-Cloud/webapp)**
A **Node.js + Express backend API** providing a `/healthz` endpoint with PostgreSQL database integration.

**Key Features:**
- Health check API (`/healthz`) for service status  
- PostgreSQL database connection via Sequelize ORM  
- Error handling and input validation  
- Configurable environment variables via `.env`  
- CI/CD pipeline with GitHub Actions  

**Tech Stack:** Node.js, Express.js, PostgreSQL, Sequelize ORM  

---

### **3. [Serverless](https://github.com/Amit-Tomar-Cloud/serverless)**
Implements a **serverless email verification microservice** using **AWS Lambda**, **SNS**, and **Mailgun**.

**Key Features:**
- Triggered by SNS messages from the web app  
- Sends verification emails with secure tokens  
- Integrates with Mailgun API  
- Token expiration and error handling  
- Secure configuration via AWS Secrets Manager  

**Tech Stack:** Node.js, AWS Lambda, SNS, Mailgun  

---

## ⚙️ End-to-End Flow
1. **Infrastructure Setup** — Terraform provisions AWS networking, compute, and storage.  
2. **Application Deployment** — Node.js WebApp runs on EC2, connects to RDS, and exposes `/healthz`.  
3. **Serverless Automation** — Lambda functions handle user verification via SNS + Mailgun.  
4. **Monitoring** — CloudWatch collects metrics and logs for observability.  

---

##  Tech Stack Summary

| Layer | Technology | Purpose |
|-------|-------------|----------|
| **Infrastructure** | Terraform, AWS VPC, EC2, RDS, S3 | Cloud provisioning |
| **Backend** | Node.js, Express, PostgreSQL, Sequelize | REST API |
| **Serverless** | AWS Lambda, SNS, Mailgun | Event-driven email service |
| **CI/CD** | GitHub Actions | Continuous integration & delivery |
| **Monitoring** | CloudWatch | Metrics and log monitoring |

---

##  Project Goal
Demonstrate a **modern DevOps workflow** combining:
- Infrastructure as Code (IaC)  
- Scalable backend APIs  
- Serverless event automation  
- CI/CD-driven deployment  
- Cloud-native observability  

This organization exemplifies how to build, deploy, and manage **production-ready cloud systems** using AWS and open-source technologies.

---

> 💡 *To learn more, explore each repository linked above for setup, deployment, and architecture details.*
