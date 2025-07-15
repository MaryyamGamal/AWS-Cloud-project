# AWS Web Application Deployment

This project showcases the deployment of a secure, highly available web application using AWS cloud infrastructure. It follows industry best practices for architecture, automation, and observability, leveraging native AWS services and Infrastructure as Code (IaC) via CloudFormation.

---

## 📌 Project Objectives

- Deploy a multi-tier web application architecture
- Automate resource provisioning using CloudFormation
- Ensure high availability and scalability
- Enforce strong security and compliance
- Enable continuous monitoring and deployment

---

## 🧱 Architecture Overview

The project includes the following key AWS components:

- **VPC** with public and private subnets (multi-AZ)
- **EC2** instances in Auto Scaling Groups behind an **Application Load Balancer**
- **RDS** (MySQL) database in Multi-AZ configuration
- **S3** bucket for static assets or backups
- **CloudFront** for content delivery (optional)
- **IAM**, **Security Groups**, and **VPC Isolation** for secure access
- **CodePipeline**, **CodeBuild**, and **CodeDeploy** for CI/CD
- **CloudWatch**, **SNS**, and **CloudTrail** for logging, monitoring, and alerts

---

## 🧩 Infrastructure Modules

| Resource              | Technology      |
|----------------------|-----------------|
| Networking           | VPC, Subnets, IGW, NAT, Route Tables |
| Compute              | EC2, Auto Scaling Group, ALB |
| Storage              | S3, RDS (MySQL) |
| Deployment Automation| CloudFormation |
| CI/CD                | CodePipeline, CodeBuild, CodeDeploy |
| Monitoring           | CloudWatch, SNS, CloudTrail |
| Security             | IAM, SGs, SSL/TLS |

---

## 📁 Repository Structure

```
aws-webapp-deployment/
├── templates/
│   └── vpc-network.yml        # CloudFormation template for network resources
├── diagrams/
│   └── architecture.png       # Architecture diagram (optional)
├── scripts/
│   └── deployment.sh          # Script for deploying the stack (optional)
└── README.md
```

---

## 🚀 Deployment

1. Clone the repo:
   ```bash
   git clone https://github.com/MaryyamGamal/AWS-Cloud-project.git
   cd aws-webapp-deployment
   ```

2. Deploy using AWS CLI:
   ```bash
   aws cloudformation create-stack      --stack-name my-vpc-stack      --template-body file://templates/vpc-network.yml      --capabilities CAPABILITY_NAMED_IAM
   ```

3. Monitor the stack creation via AWS Console or CLI.

---

## 🔐 Security Highlights

- IAM roles with least-privilege access
- Public/private subnet isolation
- Encrypted RDS and S3
- HTTPS with SSL/TLS via ALB
- Audit logging via CloudTrail

---

## 📊 Monitoring and Observability

- Real-time metrics and alarms in **CloudWatch**
- Notifications via **SNS**
- Event and API logging through **CloudTrail**

---

## 🛠️ Tech Stack

- **AWS Services:** EC2, RDS, S3, ALB, VPC, CloudFormation, IAM, CloudWatch, CloudTrail, SNS, CodePipeline, CodeDeploy, CodeBuild
- **Database:** MySQL
- **OS:** Amazon Linux 2
- **IaC:** YAML-based CloudFormation templates

---

## 📎 Author

**Mariam Gamal Ahmed Abodaif**  
Cloud Engineer | AWS & Azure Certified  
[LinkedIn](https://www.linkedin.com/in/mariamabodaif) • [GitHub](https://github.com/MaryyamGamal)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
