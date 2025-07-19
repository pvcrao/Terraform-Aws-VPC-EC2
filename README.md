# 🚀 Terraform AWS VPC + EC2 Project

This project demonstrates how to provision a **secure**, **scalable**, and **production-grade AWS environment** using **Terraform** from scratch.  
It is designed for those who want to move beyond tutorials and build **real-world Infrastructure as Code (IaC)** with **modular**, **clean**, and **automated provisioning**.

---

## 🧠 What You'll Learn

- Custom VPC creation (no default VPC)
- Public + Private Subnets across multiple AZs
- NAT Gateway and Internet Gateway setup
- Route Tables and associations
- EC2 instance provisioning in public subnet
- Sample `user-data.sh` for EC2 bootstrap
- Modular Terraform code structure
- AWS provider setup and Terraform CLI usage

---

## 🧰 Tech Stack

| Tool       | Purpose                              |
|------------|--------------------------------------|
| Terraform  | Infrastructure as Code (IaC)         |
| AWS EC2    | Virtual Server                       |
| AWS VPC    | Isolated Network                     |
| AWS IGW    | Internet access for public subnet    |
| AWS NAT    | Internet access for private subnet   |
| Amazon Linux | Lightweight base OS                |

---

## 📁 File Structure

```text
terraform-aws-vpc-ec2/
├── main.tf                  # Root module combining all resources
├── variables.tf             # Input variables
├── outputs.tf               # Exported output values
├── terraform.tfvars         # Variable values
├── nat.tf                   # NAT Gateway setup
├── private-subnet.tf        # Private subnets and route table
├── user-data.sh             # EC2 initialization script
└── README.md                # Project documentation

--

⚙️ How to Deploy
✅ Prerequisites
Terraform v1.3+

AWS account and CLI configured (aws configure)

IAM user with programmatic access + VPC/EC2 full permissions

Create a terraform.tfvars file with values:


aws_region = "ap-south-1"
vpc_cidr   = "10.0.0.0/16"

--

🚀 **Steps to Deploy**

# 1. Clone the repo
git clone https://github.com/ARIFULLALAB01/Terraform-Aws-VPC-EC2.git
cd terraform-aws-vpc-ec2

# 2. Initialize Terraform
terraform init

# 3. Validate code
terraform validate

# 4. Preview execution plan
terraform plan -out=tfplan

# 5. Apply infrastructure changes
terraform apply tfplan

--

🧹 Destroy Infrastructure

terraform destroy

--


🔮 Next Steps 

These are ideas to further enhance and productionize this Terraform setup:

🔐 Bastion Host in public subnet for SSH access to private EC2

☁️ Remote S3 backend + DynamoDB for state locking

📦 EC2 + Jenkins pipeline to trigger provisioning

🐳 Deploy Dockerized app with EBS volume mount

🕸️ Add Load Balancer (ALB/NLB) with EC2 Auto Scaling Group

🧪 Connect GitLab CI/CD for IaC deployments

🔐 Refactor and tighten Security Groups & IAM roles

👨‍💻 **Author**

Shaik Arifulla
🚀 DevOps | Terraform | AWS | Kubernetes | CI/CD | Cloud Automation
🔗 LinkedIn → https://www.linkedin.com/in/arifullashaikofficial/
📁 GitHub → https://github.com/ARIFULLALAB01/

⭐ If you find this project helpful, feel free to fork, star, or connect with me on LinkedIn!

---
