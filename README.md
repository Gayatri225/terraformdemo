# Terraform AWS EC2 + S3 Demo

A very simple **Infrastructure as Code (IaC)** project using **Terraform** to deploy:
- ✅ EC2 instance (Amazon Linux 2023, t2.micro)
- ✅ Security Group allowing SSH (22) & HTTP (80)
- ✅ S3 bucket with random unique name
- ✅ Nginx web server showing a demo page

---

## 🚀 How to Run

### 1. Clone the repo and enter the project folder
```bash
git clone <your-repo-url>
cd tf-ec2-s3-demo
```

### 2. Initialize Terraform
```bash
terraform init
```

### 3. Validate & format (optional but good practice)
```bash
terraform fmt
terraform validate
```

### 4. Plan and Apply
```bash
terraform plan
terraform apply
```
Type `yes` when prompted.

---

## 🌐 Verify the Deployment
- After apply completes, Terraform will output:
  - EC2 Public IP
  - S3 Bucket Name
- Open a browser:
  ```
  http://<ec2_public_ip>
  ```
  You should see a demo webpage: **“Terraform Demo ✅”**

---

## 🛑 Destroy Resources (IMPORTANT)
When finished, destroy everything to avoid charges:
```bash
terraform destroy
```
Type `yes` when prompted.

---

## 📝 Notes
- Region: `ap-south-1` (Mumbai) by default.
- AMI is dynamically fetched (latest Amazon Linux 2023).
- S3 bucket name is auto-randomized to avoid conflicts.
- Instance type: `t2.micro` (free-tier eligible).
