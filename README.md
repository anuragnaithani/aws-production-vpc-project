# AWS Production VPC Architecture Project

This project demonstrates a production-style AWS architecture using VPC, public subnet, private subnet, Bastion Host, NAT Gateway, Auto Scaling Group, Target Group, and Application Load Balancer.

## Architecture

User traffic flows through the Application Load Balancer and reaches EC2 instances running inside private subnets.

```text
User
 ↓
Internet Gateway
 ↓
Application Load Balancer
 ↓
Target Group
 ↓
Private EC2 Instances
Admin access flow:

Laptop
 ↓
Bastion Host
 ↓
Private EC2 Instance

Private EC2 internet access flow:

Private EC2
 ↓
NAT Gateway
 ↓
Internet
AWS Services Used
Amazon VPC
Public Subnet
Private Subnet
Internet Gateway
NAT Gateway
EC2
Bastion Host
Auto Scaling Group
Launch Template
Target Group
Application Load Balancer
Security Groups
Project Steps
Created a custom VPC.
Created public and private subnets across two Availability Zones.
Created NAT Gateway for private EC2 internet access.
Created Auto Scaling Group for EC2 instances.
Launched application servers in private subnets.
Created Bastion Host in public subnet for SSH access.
Hosted a simple HTML website using Python HTTP server.
Created Target Group for EC2 instances.
Created Application Load Balancer to route traffic.
Accessed the website using Load Balancer DNS.
Website

The website was hosted using:

python3 -m http.server 8000
Screenshots
Website Output

VPC

Subnets

Auto Scaling Group

EC2 and Bastion Host

Target Group

Load Balancer

Important Security Note

PEM files, AWS access keys, and secret credentials should never be uploaded to GitHub.

Learning Outcome

Through this project, I learned how production applications are deployed securely in AWS using private subnets, Bastion Host, NAT Gateway, Auto Scaling Group, and Load Balancer.

Created By

Anurag Naithani
