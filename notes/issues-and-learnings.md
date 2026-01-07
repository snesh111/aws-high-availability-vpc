## Issue: Private EC2 had no internet access

- Cause:-  Private subnet route table initially had no default route to a NAT Gateway.
- Fix:-Added 0.0.0.0/0 route pointing to the NAT Gateway.
- Learning:- EC2 instances inherit internet access from subnet route tables, not by default.

## Issue: SSH access denied
- Cause: Wrong key permissions.
- Fix: Used chmod 600 on PEM file.

## Learning
- Public subnets need IGW.
- Private subnets should never have public IPs.