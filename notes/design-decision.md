 # Design Decisions

## VPC Design
- Created a custom VPC with CIDR block 10.0.0.0/16.
- Used multiple Availability Zones (ap-south-1a and ap-south-1b) to achieve high availability.
- Designed the architecture so that if one Availability Zone goes down, the application continues to run from the other zone ensuring fault tolerance and backup.

## Subnets
- Public subnets for Load Balancer and Bastion Host.
- Private subnets for application EC2 instances.

## NAT Gateway
- Used NAT Gateway to allow private instances to access the internet securely.
- No public IP assigned to private instances.

## No VPC Endpoints
  - VPC endpoints were not used because:
  - This project focuses on basic high-availability architecture.
  - Internet access via NAT Gateway was sufficient.

