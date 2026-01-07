# Highly Available AWS Infrastructure (Multi-AZ)

## Project Overview
This project demonstrates the design and implementation of a highly available and secure AWS infrastructure using core AWS networking services. The architecture follows AWS best practices with public and private subnets across multiple Availability Zones.

---

## Architecture Diagram
![Architecture](architecture/architecture%20diagram.png)

---

## AWS Services Used
- Amazon VPC
- Public & Private Subnets (Multi-AZ)
- Internet Gateway
- Regional NAT Gateway
- Application Load Balancer (ALB)
- EC2 Auto Scaling Group
- Security Groups
- Amazon EC2 (Ubuntu)

---

## Architecture Details
- Designed a custom VPC in the ap-south-1 (Mumbai) region
- Created public and private subnets across two Availability Zones (ap-south-1a, ap-south-1b)
- Deployed an Application Load Balancer in public subnets
- Launched EC2 instances in private subnets using an Auto Scaling Group
- Configured a Regional NAT Gateway to allow outbound internet access for private instances
- Implemented Security Groups following the principle of least privilege

---

## Security Design
- EC2 instances do not have public IP addresses
- Internet traffic is allowed only through the Application Load Balancer
- Private subnets are isolated from direct internet access
- Outbound internet access is controlled via NAT Gateway

---

## Bastion Host
- A Bastion Host is deployed in a public subnet to securely access EC2 instances in private subnets without exposing them directly to the internet

---

## Cost Management
- Used free-tier eligible EC2 instance types
- Deleted NAT Gateway, ALB, and EC2 instances after testing to avoid unnecessary charges

---

## Screenshots
AWS Console screenshots are available in the `/screenshots` folder.

---

## Future Improvements
- Add VPC Endpoints to access AWS services privately without using a NAT Gateway
- Implement Infrastructure as Code (IaC) using Terraform
- Add monitoring and logging using Amazon CloudWatch

---

## Author
**Snesh Subbiah Raj**  
Aspiring DevOps / Cloud Engineer
