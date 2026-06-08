# terraform-aws-infrastructure-automation
Automated AWS infrastructure provisioning using Terraform by creating VPCs, Security Groups, and EC2 Key Pairs through Infrastructure as Code (IaC).
AWS Infrastructure Automation using Terraform

-- Project Overview --

This project demonstrates Infrastructure as Code (IaC) principles using Terraform to automate AWS resource provisioning.

The project consists of three real-world DevOps tasks completed on KodeKloud Engineer Platform:

AWS Key Pair Creation
AWS Security Group Creation
AWS VPC Creation

The objective was to provision AWS infrastructure using Terraform instead of manually creating resources through the AWS Console.

-- Technologies Used --
Terraform
AWS
Infrastructure as Code (IaC)
AWS VPC
AWS Security Groups
AWS Key Pairs
VS Code
Linux

Task 1: AWS Key Pair Creation
Objective

Create an RSA private key and upload its public key to AWS as an EC2 Key Pair.

Requirements
Key Pair Name: xfusion-kp
Key Type: RSA
Save private key locally

-- Terraform Resources Used --

tls_private_key
aws_key_pair
local_file

-- What I Implemented --

Generated a 4096-bit RSA key pair using Terraform.

Created an AWS Key Pair resource using the generated public key.

Stored the private key locally in PEM format for future SSH access.

-- Commands Used --

terraform init

terraform validate

terraform plan

terraform apply -auto-approve

-- Result--

Successfully created:

RSA Key
AWS Key Pair
PEM File
Task 2: AWS Security Group Creation
Objective

Create a Security Group inside the default VPC.

Requirements

Security Group Name:
xfusion-sg
Description:
Security group for Nautilus App Servers
Inbound Rules:
HTTP
Port: 80
Source: 0.0.0.0/0
SSH
Port: 22
Source: 0.0.0.0/0

-- Terraform Resources Used --

data "aws_vpc"
aws_security_group

-- What I Implemented --

Retrieved the default VPC.

Created a Security Group.

Configured inbound HTTP and SSH access.

Attached Security Group to the default VPC.

-- Commands Used --

terraform init

terraform validate

terraform plan

terraform apply -auto-approve

Result

Successfully created a Security Group with HTTP and SSH access.

Task 3: AWS VPC Creation
Objective

Create a custom VPC using Terraform.

Requirements

Name:
nautilus-vpc
Region:
us-east-1
CIDR:
10.0.0.0/16

-- Terraform Resource Used --
 aws_vpc

 -- What I Implemented --

Created a custom VPC.

Assigned a CIDR block.

Added tags for resource identification.

Managed infrastructure through Terraform code.

-- Commands Used --

terraform init

terraform validate

terraform plan

terraform apply -auto-approve

Result

Successfully provisioned a VPC in AWS.

-- Terraform Workflow Followed --

1. Write Terraform Code

Infrastructure defined in main.tf.

2. Initialize Terraform
   terraform init
   Downloads provider plugins.

3. Validate Configuration
   terraform validate
   Checks syntax errors.

4. Review Execution Plan
   terraform plan
   Displays resources that will be created.

5. Provision Infrastructure
   terraform apply -auto-approve
   Creates AWS resources.

-- Skills Demonstrated --

Infrastructure as Code
Terraform Fundamentals
AWS Networking
AWS Security
Key Pair Management
VPC Configuration
Security Group Configuration
Linux Command Line
DevOps Automation
Key Learnings

-- Through this project I learned --

How Terraform automates cloud infrastructure.
Difference between manual provisioning and IaC.
How to create AWS networking resources.
How Terraform state management works.
How to manage cloud resources using reusable code.
      
 
