# Web Application: Fitness Training NEOGYM

## Description:
Launched "Fitness Training NeoGym," an innovative web application that prioritizes a seamless user experience, even during scheduled or unexpected downtime, thanks to the robust integration of AWS services.Utilized AWS services to enhance the availability and resilience of the Fitness Training NeoGym web application, ensuring an uninterrupted user experience in the face of potential disruptions.

---

## Overview
This project demonstrates the deployment of a highly available and scalable web application on AWS using services like EC2,Deployed across multiple Availability Zones, Application Load Balancer (ALB), and Auto Scaling Group (ASG).

The architecture ensures high availability, fault tolerance, and automatic scaling based on application demand.

---

## Services
* S3
* IAM Role
* EC2
* Application Load Balancer(ALB)
* Auto Scaling Group(ASG)
* Cloudwatch
* Simple Notification Service(SNS)

---

## Architecture Flow

1. Application files stored in S3  
2. EC2 instances fetch application data from S3  
3. ALB distributes incoming traffic across instances  
4. Auto Scaling Group adjusts instance count based on load  
5. CloudWatch monitors performance metrics  
6. SNS sends notifications for scaling events

---
  
![Project 05](https://github.com/sumathi-rajan/project5/assets/150107821/34851d04-5ceb-4c09-8063-02bd5eea2f8a)

##  Implementation Summary

### S3 Setup
- Stored application deployment files in S3  
- Enabled secure access using IAM role  

---

### IAM Role
- Created IAM role for EC2 instance  
- Granted permissions to access S3 securely  

---

### EC2 Deployment
- Launched EC2 instances with required configurations  
- Used user data to install dependencies during startup  
- Associated IAM role for S3 access  

---

### Application Load Balancer (ALB)
- Configured internet-facing ALB  
- Created target group for EC2 instances  
- Distributed traffic across multiple Availability Zones  

---

### Security Groups
- ALB: Allowed inbound traffic from internet  
- EC2: Allowed traffic only from ALB  

---

### Auto Scaling Group (ASG)
- Configured:
  - Min: 1  
  - Desired: 2  
  - Max: 3  
- Automatically adjusts instances based on demand  

---

### Scaling Policy
- Scale out when CPU > 50%  
- Scale in when CPU < 35%  
- Ensures performance and cost optimization  

---

### CloudWatch Monitoring
- Monitored CPU utilization and system metrics  
- Integrated with ASG for automated scaling  

---

### SNS Notifications
- Configured email alerts for scaling events  
- Notifies when instances are added or removed  

---

##  Key Features

- High availability across multiple Availability Zones  
- Automatic scaling based on demand  
- Secure architecture using IAM and Security Groups  
- Load-balanced traffic distribution  
- Real-time monitoring and alerting  

---

##  Use Case

This architecture is ideal for web applications that require high availability, scalability, and cost-efficient resource management under varying workloads.

---

## ⚠️ Challenges & Learnings

### Challenges
- Configuring ALB target groups and health checks correctly  
- Setting up Auto Scaling policies for optimal performance  
- Managing secure communication between ALB and EC2 instances  

### Learnings
- Gained hands-on experience with scalable AWS architecture  
- Learned how to configure Auto Scaling and load balancing  
- Improved understanding of monitoring and alerting using CloudWatch and SNS  

---

##  Outcome

Successfully deployed a scalable and highly available web application on AWS that can handle variable traffic loads while maintaining performance and minimizing costs.








