# Day-03_AWS_Fundamentals_Part-3_EC2.md

# Amazon EC2 (Elastic Compute Cloud)

## What is EC2?

Amazon EC2 (Elastic Compute Cloud) is an AWS Infrastructure as a Service (IaaS) that provides virtual servers (called EC2 instances) in the cloud. It allows us to run applications without purchasing physical hardware. We only need to install the required operating system and software, such as Docker, Nginx, Jenkins, Java, etc.

AWS follows the **Pay-As-You-Go** pricing model, so we pay only for the resources we use.

---

# Why is it called Elastic Compute Cloud?

### Elastic

Elastic means we can increase or decrease the computing resources according to application demand.

Examples:
- Increase CPU and RAM during high traffic.
- Decrease CPU and RAM when traffic is low.

This helps reduce infrastructure cost.

---

### Compute

Compute refers to a virtual server (virtual machine) where we run our applications.

Examples:
- Ubuntu Server
- Amazon Linux
- Windows Server

---

### Cloud

The server runs in the AWS cloud.

Benefits:
- No need to purchase physical hardware.
- High availability.
- Easy scalability.
- Accessible from anywhere.
- Pay only for what you use.

---

# Advantages of EC2

- No need to purchase physical servers.
- Pay only for the resources used.
- Easy to scale up and scale down.
- Quick deployment of servers.
- Highly available.
- Easy to manage.
- Supports different operating systems.
- Can be integrated with other AWS services.

---

# What is an EC2 Instance?

An EC2 Instance is a virtual server running inside AWS.

Examples:
- Ubuntu EC2 Instance
- Amazon Linux EC2 Instance
- Windows EC2 Instance

---

# What is an AMI (Amazon Machine Image)?

An AMI is a pre-configured template used to launch an EC2 instance.

An AMI contains:
- Operating System
- Root Volume
- Default configuration
- Optional pre-installed software

Think of an AMI as a blueprint for creating EC2 instances.

---

# Why do we use AMIs?

Instead of installing software on every new server:

1. Launch one EC2 instance.
2. Install all required software.
3. Configure the server.
4. Create an AMI.
5. Launch multiple EC2 instances from that AMI.

Benefits:
- Saves time.
- Ensures identical server configuration.
- Reduces manual effort.
- Minimizes human errors.

---

# Important Note about AMIs

Creating or modifying an AMI does NOT update existing EC2 instances.

An AMI is used only when launching new EC2 instances.

Existing EC2 instances remain unchanged.

---

# Who can create an AMI?

- Root User
- IAM User (only if the required permissions are granted)

In real companies, IAM Users create AMIs only if their IAM policies allow it.

---

# Launching Multiple EC2 Instances

AWS allows us to launch multiple EC2 instances simultaneously.

Methods:
- AWS Management Console
- AWS CLI
- Terraform (Infrastructure as Code)

Example:

One configured EC2
        │
Create AMI
        │
Launch 50 EC2 Instances

---

# What is an EC2 Instance Type?

An Instance Type defines the computing capacity of an EC2 instance.

It mainly determines:
- vCPU
- Memory (RAM)
- Network performance

Storage is configured separately using Amazon EBS.

---

# Common Instance Types

| Instance Type | Suitable For |
|---------------|--------------|
| t2.micro | Learning, Free Tier, Small Websites |
| t3.micro | Small Applications |
| t3.small | Small Production Applications |
| m5.large | Medium Applications |
| c5.xlarge | CPU Intensive Applications |

---

# How to Choose an Instance Type?

Choose the instance type based on the application's requirements.

Example:

Small Website
- Low traffic
- Small RAM
- Small CPU
- t2.micro

Large Java Application
- High traffic
- More CPU
- More RAM
- m5.large

Never choose a larger instance unless required because AWS charges based on resource usage.

---

# Interview Questions

## Q1. What is Amazon EC2?

Amazon EC2 (Elastic Compute Cloud) is an AWS IaaS service that provides resizable virtual servers called EC2 instances. It allows us to run applications without purchasing physical hardware and follows the Pay-As-You-Go pricing model.

---

## Q2. Why is EC2 called Elastic Compute Cloud?

Elastic means we can increase or decrease computing resources such as CPU and memory based on application demand.

Compute refers to the virtual server used to run applications.

Cloud means the infrastructure is provided by AWS over the internet, eliminating the need to purchase physical hardware.

---

## Q3. What is an AMI?

An Amazon Machine Image (AMI) is a pre-configured template that contains the operating system, storage configuration, and optional software required to launch an EC2 instance.

---

## Q4. Why do companies create AMIs?

Companies create AMIs to launch multiple identical EC2 instances quickly. This ensures consistency, saves time, reduces manual effort, and minimizes configuration errors.

---

## Q5. Does modifying an AMI update existing EC2 instances?

No.

Existing EC2 instances are independent after they are launched. Updating an AMI affects only new EC2 instances created from that AMI.

---

## Q6. What is an EC2 Instance Type?

An EC2 Instance Type defines the computing capacity of an EC2 instance, including vCPU, memory (RAM), and network performance.

Storage is configured separately using Amazon EBS.

---

# Key Points to Remember

- EC2 is an IaaS service.
- EC2 provides virtual servers.
- Elastic means scalable.
- Pay only for what you use.
- AMI is a template for launching EC2 instances.
- One AMI can be used to launch multiple identical EC2 instances.
- Updating an AMI does not update existing EC2 instances.
- Instance Type defines CPU and RAM.
- Storage is configured separately using EBS.
- Always choose the instance type based on the application's requirements.
