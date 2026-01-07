# Deployment Steps

1. Created a custom VPC.
2. Added public and private subnets in two AZs.
3. Attached Internet Gateway to VPC.
4. Configured route tables for public and private subnets.
5. Created NAT Gateway in public subnet.
6. Launched Bastion Host in public subnet.
7. Deployed application EC2 instances in private subnets.
8. Configured Load Balancer and Target Group.
9. Enabled Auto Scaling Group.