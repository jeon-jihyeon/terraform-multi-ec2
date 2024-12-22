# Terraform Multiple EC2 Instances
The terraform-multi-ec2 repository provides Terraform configurations for provisioning multiple AWS EC2 instances along with associated networking components.
- Terraform v0.12.23
    + provider registry.terraform.io/providers/hashicorp/aws v3.66.0

## Prerequsite
Before deploying this infrastructure, ensure you have:
- aws cli v2
- S3 bucket for storing Terraform state files.
- IAM User with necessary permissions for resource creation.
- SSL Certificate For securing communications.
- domain for application access.

## Overview
![aws-architecture-v100](https://user-images.githubusercontent.com/63345897/147190524-0bb95fad-852f-4e4f-8542-7427b8515a68.jpg)
The network architecture is designed to ensure high availability and security:
- VPC: Provides an isolated network environment.
- Subnets: Distributed across multiple Availability Zones for redundancy.
- Routing: Configured to manage traffic flow efficiently.
- Security Groups: Defined to allow necessary traffic while restricting unauthorized access.

This project utilizes Terraform to automate the creation of AWS infrastructure, including:
- VPC 
- AZ subnets
- Routing tables
- Internet Gateway
- NAT instance
- EC2 instance
- Security groups
- ALB
- RDS
- S3
- CodeDeploy
- .yml files for gitaction
- scripts files for codedeploy

## Source Structure
- [Standard Module Structure](https://www.terraform.io/language/modules/develop/structure)
    + separated by environment
