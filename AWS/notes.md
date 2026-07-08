# Day 2 – AWS Fundamentals (Part 1)

> **Roadmap:** 21-Day DevOps Preparation
>
> **Topic:** Introduction to Cloud Computing & Types of Cloud
>
> **Status:** ✅ Completed

---

# What is Cloud Computing?

Cloud Computing is the **on-demand delivery of computing services** such as servers, storage, networking, databases, and applications over the Internet.

Instead of purchasing and maintaining physical servers, organizations rent resources from a cloud provider and pay only for what they use.

## Interview Definition

> Cloud Computing is the on-demand delivery of IT resources such as servers, storage, networking, and databases over the Internet with pay-as-you-go pricing.

---

# Traditional Data Center vs Cloud

## Traditional Data Center

Company purchases and maintains:

- Physical Servers
- Storage
- Networking Devices
- Electricity
- Cooling
- Security
- Backup Infrastructure

### Disadvantages

- High initial investment
- Hardware maintenance
- Limited scalability
- Time-consuming setup
- Need dedicated infrastructure team

---

## Cloud Computing

Cloud Provider (AWS) manages:

- Physical Servers
- Networking Hardware
- Storage Hardware
- Power
- Cooling
- Physical Security

Customer manages:

- Operating System (EC2)
- Applications
- Users
- Data
- Application Security

---

# Why Companies Prefer Cloud?

- No hardware purchase
- No infrastructure maintenance
- Faster deployment
- High availability
- Scalability
- Backup facilities
- Pay only for what you use
- Global accessibility

---

# Pay-As-You-Go Model

Cloud follows the Pay-As-You-Go pricing model.

Example:

Need one server for 3 days?

Launch one EC2 instance.

After work is completed:

Terminate the instance.

Billing stops.

No long-term hardware investment.

---

# Real Life Example

Hotel Analogy

Buying a Hotel

- Huge investment
- Maintenance cost
- Security
- Staff

Renting a Hotel Room

- Pay only while staying
- No maintenance
- Easy and economical

Cloud Computing works similarly.

---

# Real DevOps Example

Without Cloud

Developer
↓
Purchase Server
↓
Install Hardware
↓
Configure Network
↓
Install OS
↓
Deploy Application

Time Required:
Days or Weeks

---

With AWS

Developer
↓
Launch EC2
↓
SSH into Server
↓
Deploy Application

Time Required:
Few Minutes

---

# Advantages of Cloud Computing

- No hardware purchase
- Reduced infrastructure cost
- Pay only for used resources
- High Availability
- Scalability
- Backup & Disaster Recovery
- Easy Deployment
- Global Access
- Better Resource Utilization

---

# Scalability

Scalability means increasing or decreasing resources based on application demand.

Example

Normally:

2 Servers

During Festival Sale:

10 Servers

More users → Add more servers.

---

# Elasticity

Elasticity means automatically increasing or decreasing resources based on demand.

Example

Normal Traffic

2 Servers

↓

Heavy Traffic

10 Servers

↓

Traffic Reduced

Automatically Back to 2 Servers

AWS supports Elastic Scaling.

---

# Interview Question

## Why do companies prefer Cloud Computing?

Answer:

Cloud Computing reduces infrastructure management, provides scalability, high availability, backup facilities, faster deployment, and follows the Pay-As-You-Go pricing model, allowing organizations to focus on application development instead of hardware management.

---

# Scenario Based Question

Question

A company requires 50 servers only for 3 days.

What would you recommend?

- Buy 50 Physical Servers
- Launch 50 EC2 Instances

Answer

Launch 50 EC2 Instances because they can be created within minutes, cost less for short-term usage, and can be terminated after the event. This saves both time and infrastructure cost.

---

# Types of Cloud

There are three major deployment models.

1. Public Cloud
2. Private Cloud
3. Hybrid Cloud

---

# 1. Public Cloud

Definition

Infrastructure is owned and managed by a cloud provider.

Multiple customers share the provider's infrastructure.

Examples

- AWS
- Microsoft Azure
- Google Cloud Platform (GCP)

Advantages

- Low Cost
- Highly Scalable
- No Infrastructure Maintenance
- Pay-As-You-Go

Real Example

Launching an EC2 instance in AWS.

---

# 2. Private Cloud

Definition

Infrastructure is owned and used by a single organization.

Examples

- Banks
- Government Organizations
- Military
- Hospitals

Advantages

- More Control
- Better Security
- Better Compliance

Disadvantages

- Expensive
- Requires Maintenance

---

# 3. Hybrid Cloud

Definition

Combination of Public Cloud and Private Cloud.

Some applications run on Private Cloud while others run on Public Cloud.

Example

Private Cloud

- Student Database
- Financial Records

Public Cloud (AWS)

- College Website
- Online Portal

Advantages

- Flexibility
- Better Security
- Cost Optimization

---

# Public vs Private vs Hybrid

| Public Cloud | Private Cloud | Hybrid Cloud |
|--------------|---------------|--------------|
| Owned by Cloud Provider | Owned by Organization | Combination of Both |
| Shared Resources | Dedicated Resources | Mixed Environment |
| Low Cost | High Cost | Medium Cost |
| Highly Scalable | More Control | Flexible |

---

# Interview Questions

## What is Cloud Computing?

Cloud Computing is the on-demand delivery of IT resources over the Internet with Pay-As-You-Go pricing.

---

## What are the advantages of Cloud Computing?

- Scalability
- High Availability
- Cost Saving
- Faster Deployment
- Backup
- Disaster Recovery
- Global Accessibility

---

## What is Public Cloud?

Public Cloud is cloud infrastructure owned and managed by a cloud provider such as AWS, Azure, or GCP, where resources are shared among multiple customers.

---

## What is Private Cloud?

Private Cloud is cloud infrastructure dedicated to a single organization and managed either internally or by a third party.

---

## What is Hybrid Cloud?

Hybrid Cloud is a combination of Public Cloud and Private Cloud where workloads are distributed between both environments.

---

## Which cloud type does AWS belong to?

Public Cloud

---

# Key Points to Remember

✅ Cloud = Rent Infrastructure

✅ Traditional Data Center = Own Infrastructure

✅ AWS is a Public Cloud

✅ Public Cloud = Low Cost

✅ Private Cloud = More Control

✅ Hybrid Cloud = Best of Both

✅ Scalability = Increase/Decrease Resources

✅ Elasticity = Automatic Scaling

✅ Pay-As-You-Go = Pay Only for What You Use

---

# DevOps Perspective

As a DevOps Engineer, you will mainly work on Public Cloud platforms like AWS.

Typical Workflow

Developer
↓
GitHub
↓
Jenkins
↓
Docker
↓
AWS EC2
↓
Load Balancer
↓
Users

Understanding Cloud Computing is the foundation for all upcoming AWS services.

---

# Topics Completed

- ✅ Cloud Computing
- ✅ Traditional Data Center vs Cloud
- ✅ Advantages of Cloud
- ✅ Pay-As-You-Go
- ✅ Scalability
- ✅ Elasticity
- ✅ Public Cloud
- ✅ Private Cloud
- ✅ Hybrid Cloud

---

# Next Topic

➡️ Cloud Service Models

- IaaS
- PaaS
- SaaS
