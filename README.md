ECR + ECS (Fargate) + ALB + VPC

Amazon ECR
Amazon ECS (Fargate)
Application Load Balancer
Amazon VPC


Steps
1. Create Docker Image and push in ECE
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin xxx4705.dkr.ecr.us-east-1.amazonaws.com
docker build -t myindiaskilltestproecrrepro .
docker tag myindiaskilltestproecrrepro:latest 56468xxx.dkr.ecr.us-east-1.amazonaws.com/myindiaskilltestproecrrepro:latest
docker push 5646869xxx5.dkr.ecr.us-east-1.amazonaws.com/myindiaskilltestproecrrepro:latest

2. Create VPC and Networking
   VPC(172.16.0.0/16)
   3 public subnets (172.16.0.0/24,172.16.1.0/24,172.16.2.0/24)
   Internetway
   Route Table
3.Create Security Groups
  80 and  5000 allow
4.Create Task Definition   
5.Create ECS Cluster (Fargate)
6Create Application Load Balancer
7.Create ECS Service



