# 🏗️ Terraform AWS Modular Infrastructure

This project provisions an AWS infrastructure using Terraform with modular design. It includes:

- ✅ VPC (Virtual Private Cloud)
- ✅ Subnet (public)
- ✅ EC2 Instance
- ✅ Modular file structure
- ✅ GitHub Actions CI/CD workflow
- ✅ Optional Terraform Cloud remote backend

---

## 📁 Project Structure
terraform-infra/
├── main.tf # Root config calling modules
├── variables.tf # Input variables for root
├── outputs.tf # Outputs from root
├── terraform.tfvars # Optional variable overrides
├── .github/
│ └── workflows/
│ └── terraform.yml # GitHub Actions CI
└── modules/
├── vpc/ # VPC module
├── subnet/ # Subnet module
└── ec2/ # EC2 module


---

## 🧱 Modules Overview

### VPC Module
- Creates a VPC with CIDR block and name

### Subnet Module
- Public subnet inside the above VPC

### EC2 Module
- EC2 instance in the subnet
- Public IP auto-assigned
- AMI and type configurable

---

## 🚀 Getting Started

### 🔧 Prerequisites
- [Terraform](https://developer.hashicorp.com/terraform/downloads)
- AWS account with access/secret keys
- Optionally: [Terraform Cloud](https://app.terraform.io)

---

### 🛠️ Setup

```bash
git clone https://github.com/your-user/terraform-infra.git
cd terraform-infra

terraform init
terraform plan
terraform apply

