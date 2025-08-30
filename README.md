# Terraform AWS EC2 + S3 Demo

Pls check the "tf demo" folder for the screenshots

A very simple **Infrastructure as Code (IaC)** project using **Terraform** to deploy:
- ✅ EC2 instance (Amazon Linux 2023, t3.micro)
- ✅ Security Group allowing SSH (22) & HTTP (80)
- ✅ S3 bucket with random unique name
- ✅ Nginx web server showing a demo page


## 📝 Notes
- Region: `ap-south-1` (Mumbai) by default.
- AMI is dynamically fetched (latest Amazon Linux 2023).
- S3 bucket name is auto-randomized to avoid conflicts.
- Instance type: `t3.micro` (free-tier eligible).
