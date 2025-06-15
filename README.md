# Terraform-AWS-EC2-Infrastructure-as-Code

## Description

This project provisions AWS EC2 infrastructure using Terraform. It creates an EC2 instance, configures security groups, installs NGINX, and hosts a static website.

## Technologies Used

- Terraform
- AWS EC2
- AWS Security Groups
- NGINX (installed on EC2 via user data)

## Folder Structure

terraform-aws-ec2/
├── main.tf
├── variables.tf
├── outputs.tf
├── provider.tf
├── terraform.tfvars
├── user_data.sh
└── README.md

## Setup Instructions

### Prerequisites

- AWS Account
- AWS Access Key and Secret Key
- AWS CLI configured locally
- Terraform installed

### AWS Credentials

Either configure using AWS CLI:

```bash
aws configure
Or export environment variables:


export AWS_ACCESS_KEY_ID="your_access_key"
export AWS_SECRET_ACCESS_KEY="your_secret_key"
export AWS_DEFAULT_REGION="your_region"
Initialize Terraform
Inside the project directory, run:

terraform init
Plan Infrastructure Changes

terraform plan
Apply Infrastructure Changes

terraform apply
Confirm with yes when prompted.

Destroy Infrastructure
To remove all resources created:


terraform destroy
Confirm with yes when prompted.

What This Creates
EC2 instance (Amazon Linux 2)

Security Group allowing HTTP (80), SSH (22)

NGINX installed automatically

Static HTML page hosted at /var/www/html/index.html

Notes
Ensure the provided AWS credentials have necessary permissions to create EC2 and related resources.

Use only in non-production environments while testing.

Author
Supriya S P
