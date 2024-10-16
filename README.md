# 🚀 Deploy a Static Website on AWS with Ansible  

This guide walks through the steps to **deploy a static website on AWS** using **Ansible** to automate infrastructure setup. Below is a structured overview of the entire process, highlighting essential tools, resources, and services used.

---

## 📋 Table of Contents
1. [Prerequisites](#prerequisites)  
2. [Project Overview](#project-overview)  
3. [Step-by-Step Deployment](#step-by-step-deployment)  

---

## 🎯 Prerequisites

Ensure you have the following before starting:  
- **GitHub** account – for code repository management.  
- **VSCode** – a powerful code editor with an integrated terminal.  
- **Git** – to clone and manage your GitHub repository locally.  
- **AWS account** – to deploy infrastructure.  
- Basic knowledge of **Ansible** and **AWS networking** concepts.  

---

## 📖 Project Overview

The project involves:  
1. Setting up a **GitHub repository** to store Ansible playbooks.  
2. Building a **three-tier AWS VPC network** from scratch.  
3. Automating infrastructure deployment with **Ansible**.  
4. Launching **EC2 instances**, including a **Bastion Host**, **Ansible Server**, and **Web Servers**.  
5. Configuring **Security Groups**, **Key Pairs**, and **Route 53 DNS**.  
6. Deploying an **Application Load Balancer** to manage traffic.  
7. Creating an **Amazon Machine Image (AMI)** for future infrastructure reusability.  

---

## 🛠️ Step-by-Step Deployment

### 1️⃣ Sign up for a Free GitHub Account  
- Create an account at [GitHub](https://github.com/).  
- This will host the **Ansible playbooks** and website code.  

### 2️⃣ Create a GitHub Repository  
- Create a new repository in GitHub.  
- Use **VSCode** to connect your repo via **Git** for easy code management.

### 3️⃣ Install Git  
- [Download and install Git](https://git-scm.com/) to manage the repository locally.

### 4️⃣ Install VSCode  
- Download [VSCode](https://code.visualstudio.com/) for writing and managing code.  
- Use its **integrated terminal** to run commands directly.

### 5️⃣ Build a Three-Tier AWS VPC  
- Set up the **VPC** with **public and private subnets** across multiple availability zones.  
- This ensures high availability and isolation of resources.

### 6️⃣ Create NAT Gateway and Security Group  
- **NAT Gateway**: Allows outbound internet access for private instances.  
- **Security Groups**: Control inbound and outbound traffic to ensure secure hosting.

### 7️⃣ Create a Key Pair  
- Generate a **Key Pair** (public/private key) to connect to your EC2 instances via SSH.  

### 8️⃣ Import Public Key to AWS  
- Import your **public key** to **AWS** for SSH access via **Ansible**.

### 9️⃣ Launch Bastion Host, Ansible Server, and Web Servers  
- **Bastion Host**: Acts as a jump server for accessing private instances.  
- **Ansible Server**: Hosts playbooks to automate configuration.  
- **Web Servers**: Serve the static website to users.

### 🔑 10️⃣ Add the Private Key to Ansible Server  
- Copy the **private key** into the Ansible server to allow secure SSH access to web servers.

### 11️⃣ Create an Application Load Balancer  
- **ALB** distributes incoming traffic among the web servers, ensuring optimal performance.

### 12️⃣ Set up A Record in Route 53  
- Create an **A Record** in **Route 53** to map the website's domain name to the load balancer.

### 13️⃣ Create an AMI of the Ansible Server  
- Take an **AMI snapshot** of the Ansible server for easy future deployment.  
- This image can be reused to quickly launch identical instances.

---


