# cloudformation-project

## Fully Automated VPC and EC2 Setup with VPC Peering using CloudFormation templates

### 1. Provision two isolated VPCs (Internal & Client)
### 2. Launch public and private EC2 instances in each
### 3. enable secure cross-VPC communication between private instances via VPC Peering

## Architecture Diagram
<img width="1466" height="864" alt="image" src="https://github.com/user-attachments/assets/fa80a660-2a33-4687-b642-a546a6634834" />

### With Infrastructure as Code (IaC) using AWS CloudFormation, we'll build a complete, production-like network setup without any manual steps
#### 1. Create Two VPCs – Each with custom CIDR blocks for logical separation (e.g., 10.0.0.0/16 and 172.168.0.0/16).
#### 2. Deploy Public and Private Subnets – In each VPC, spread across different Availability Zones.
#### 3. Launch EC2 Instances – One public and one private instance in each VPC.
#### 4. Establish VPC Peering – To enable communication between private subnets in both VPCs.
#### 5. Configure Route Tables – Modify route tables to allow secure, cross-VPC traffic flow.

### Let’s Build
#### ✅ First Stage: Write CloudFormation Templates in VS Code (YAML Format)
#### CloudFormation supports both JSON and YAML, but YAML is much simpler to write and read. It is also easier
#### compared to Terraform, which uses its own custom language (HCL).

### Start by creating the following templates:

 
