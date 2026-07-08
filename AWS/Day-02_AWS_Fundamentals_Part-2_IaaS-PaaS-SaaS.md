# Day 2 – AWS Fundamentals (Part 2)

> **Roadmap:** 21-Day DevOps Preparation
>
> **Topic:** IaaS, PaaS & SaaS
>
> **Status:** ✅ Completed

---

# Cloud Service Models

Cloud service models define **who is responsible for managing different parts of the infrastructure and application.**

There are three major cloud service models:

1. Infrastructure as a Service (IaaS)
2. Platform as a Service (PaaS)
3. Software as a Service (SaaS)

---

# 1. IaaS (Infrastructure as a Service)

## Definition

Infrastructure as a Service (IaaS) provides virtual infrastructure such as servers, storage, and networking over the Internet.

The cloud provider manages the infrastructure, while the customer is responsible for installing and managing the operating system, software, and applications.

---

## Cloud Provider Responsibilities

- Physical Servers
- Virtual Machines
- Storage
- Networking
- Data Center
- Power
- Cooling
- Physical Security

---

## Customer Responsibilities

- Operating System
- Software Installation
- Security Patches
- Middleware
- Applications
- Data
- User Management

---

## AWS Example

- Amazon EC2

Other Examples

- Azure Virtual Machines
- Google Compute Engine

---

## Real DevOps Example

Launch an EC2 instance.

Connect using SSH.

```bash
ssh -i key.pem ubuntu@public-ip
```

Install required software.

```bash
sudo apt update
sudo apt install nginx
sudo apt install docker.io
sudo apt install jenkins
```

AWS provides the server.

You install and manage everything else.

---

# Real-Life Analogy

Imagine purchasing an empty plot.

Someone provides the land.

You build the house.

You decide:

- Design
- Furniture
- Paint
- Security

Maximum responsibility is yours.

---

# Advantages of IaaS

- Full control over the server
- Flexible
- Highly scalable
- Suitable for DevOps workloads
- Easy to deploy applications

---

# Disadvantages

- User manages Operating System
- User performs updates
- User manages security patches
- More administrative responsibility

---

# 2. PaaS (Platform as a Service)

## Definition

Platform as a Service (PaaS) provides infrastructure along with the operating system and runtime environment.

The customer only deploys and manages the application.

---

## Cloud Provider Responsibilities

- Infrastructure
- Storage
- Networking
- Operating System
- Runtime Environment
- Security Updates

---

## Customer Responsibilities

- Application
- Application Configuration
- Application Data

---

## Examples

- AWS Elastic Beanstalk
- Google App Engine
- Heroku

---

## Real DevOps Example

Instead of creating an EC2 instance and installing Java manually, upload the application to Elastic Beanstalk.

AWS manages:

- Server
- Operating System
- Runtime

You only deploy the application.

---

# Real-Life Analogy

Renting a fully furnished apartment.

The owner provides:

- Furniture
- Electricity
- Water
- Maintenance

You simply move in and live there.

---

# Advantages

- Faster application deployment
- No Operating System management
- Automatic updates
- Reduced administration

---

# Disadvantages

- Less control
- Limited customization
- Platform dependency

---

# 3. SaaS (Software as a Service)

## Definition

Software as a Service (SaaS) provides complete software over the Internet.

The cloud provider manages everything.

Users simply use the software.

---

## Cloud Provider Responsibilities

- Infrastructure
- Storage
- Networking
- Operating System
- Runtime
- Applications
- Security
- Updates
- Maintenance

---

## User Responsibilities

- Create an account
- Configure settings
- Use the software

---

## Examples

- Gmail
- Google Drive
- Microsoft 365
- Dropbox
- Zoom

---

## Real DevOps Example

Using Gmail.

You simply:

- Create an account
- Login
- Send emails

Google manages:

- Mail Servers
- Storage
- Operating System
- Security
- Backup
- Updates

---

# Real-Life Analogy

Staying in a hotel.

Everything is already available.

You simply use the room.

No maintenance.

No cleaning.

No repairs.

---

# Advantages

- Easy to use
- No installation
- Automatic updates
- Accessible from anywhere
- No maintenance

---

# Disadvantages

- Very limited control
- Depends on Internet connectivity
- Customization may be limited

---

# Responsibility Comparison

| Component | IaaS | PaaS | SaaS |
|-----------|------|------|------|
| Physical Server | Cloud Provider | Cloud Provider | Cloud Provider |
| Storage | Cloud Provider | Cloud Provider | Cloud Provider |
| Networking | Cloud Provider | Cloud Provider | Cloud Provider |
| Operating System | Customer | Cloud Provider | Cloud Provider |
| Runtime | Customer | Cloud Provider | Cloud Provider |
| Middleware | Customer | Cloud Provider | Cloud Provider |
| Application | Customer | Customer | Cloud Provider |
| Data | Customer | Customer | Cloud Provider (Application Data Management) |

---

# AWS Examples

| AWS Service | Service Model |
|-------------|---------------|
| Amazon EC2 | IaaS |
| AWS Elastic Beanstalk | PaaS |

Examples outside AWS

| Service | Service Model |
|----------|---------------|
| Gmail | SaaS |
| Google Drive | SaaS |
| Microsoft 365 | SaaS |
| Zoom | SaaS |

---

# Interview Questions

## What is IaaS?

Infrastructure as a Service provides virtual infrastructure such as servers, storage, and networking. The user manages the operating system, applications, and software.

---

## What is PaaS?

Platform as a Service provides infrastructure, operating system, and runtime. The user only develops and deploys the application.

---

## What is SaaS?

Software as a Service provides complete software over the Internet. Users simply access and use the software without managing the underlying infrastructure.

---

## Why is EC2 considered IaaS?

Because AWS provides the infrastructure, while the customer installs and manages the operating system, applications, and software.

---

## Why is Gmail considered SaaS?

Because Google manages the servers, operating system, storage, updates, and security. Users only access and use the email service.

---

## Which service model gives the most control?

IaaS

---

## Which service model gives the least responsibility?

SaaS

---

## Which service model is most commonly used by DevOps Engineers?

IaaS

Reason:

DevOps engineers require control over:

- Linux
- Docker
- Jenkins
- Kubernetes
- Networking
- Security
- Application Deployment

---

# Memory Trick

## IaaS

"I Manage the Server"

Examples

- Install Linux
- Install Docker
- Install Jenkins
- Deploy Application

---

## PaaS

"I Deploy My Application"

Cloud provider manages:

- Server
- OS
- Runtime

You manage:

- Application

---

## SaaS

"I Just Use the Software"

Examples

- Gmail
- Google Drive
- Microsoft 365

---

# Real-Life Analogy

| Service Model | Analogy |
|---------------|---------|
| IaaS | Empty Plot – You build the house |
| PaaS | Fully Furnished Apartment – You only move in |
| SaaS | Hotel Room – Everything is ready to use |

---

# Key Points to Remember

✅ IaaS = Infrastructure as a Service

✅ PaaS = Platform as a Service

✅ SaaS = Software as a Service

✅ EC2 is an example of IaaS

✅ Elastic Beanstalk is an example of PaaS

✅ Gmail is an example of SaaS

✅ IaaS gives maximum control

✅ SaaS gives minimum responsibility

✅ DevOps Engineers mainly work with IaaS

---

# Topics Completed

- ✅ IaaS
- ✅ PaaS
- ✅ SaaS
- ✅ Responsibility Model
- ✅ AWS Examples
- ✅ Interview Questions
- ✅ Real-World Analogies

---

# Next Topic

➡️ AWS Global Infrastructure

- Regions
- Availability Zones (AZs)
- Edge Locations
