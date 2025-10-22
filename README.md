# AWS-Launch-VM
Launch a Virtual Machine (EC2 Instance) on AWS and connect to it via SSH using a key pair.

# AWS-EC2-VM-launch
This repository contains my practice task for launching an **AWS EC2 virtual machine**, connecting to it via SSH, and exploring basic Linux commands.

## Objective
The main goal of this task was to get **hands-on experience with cloud virtual machines**.  
I wanted to understand how to **create, configure, and connect** to an AWS EC2 instance, and get a feel for **Infrastructure-as-a-Service (IaaS)** — the foundation of cloud computing.

## Tools I Used
- AWS Free Tier account  
- AWS EC2 (Elastic Compute Cloud)  
- SSH client (or browser-based terminal)  

## Steps I Followed

### 1. Logged in to AWS
I started by logging into my AWS Management Console and opening the **EC2 Dashboard**.  
I confirmed that my **Free Tier** was active so I could practice without worrying about costs.

### 2. Created a New EC2 Instance
I clicked **Launch Instance** and filled in the details:  
- **Instance Name:** `cloud-vm`  
- **Operating System:** Ubuntu Server 22.04 LTS (Free Tier Eligible)  
- **Instance Type:** `t2.micro` (1 vCPU, 1 GB RAM)  
- **Key Pair:** `cloudvmkey.pem` (needed for SSH access)  
- **Network Settings:** Enabled HTTP (80) and HTTPS (443)  
- **Region:** North Virginia (us-east-1)  

After reviewing the settings, I launched the instance and waited for it to pass the **2/2 status checks**.

### 3. Connected to the VM via SSH
Once the instance was ready, I connected to it using:

```bash
ssh -i "cloudvmkey.pem" ubuntu@<Public-IP-Address>
To verify everything was working, I ran a few basic Linux commands:

bash
Copy code
uname -a     # Check system info
ls           # List files in the current directory
whoami       # Confirm logged-in user
Seeing the terminal respond instantly made me realize just how powerful cloud computing is — I was literally controlling a remote server from my laptop!

4. Stopped the EC2 Instance
After testing, I stopped the instance to avoid unnecessary charges.
It was a small but important step in managing cloud resources responsibly.

VM Configuration at a Glance
Parameter	Value
Instance Name	cloud-vm
Operating System	Ubuntu 22.04 LTS
Region	North Virginia (us-east-1)
Instance Type	t2.micro (Free Tier Eligible)
Key Pair	cloudvmkey.pem
Firewall Rules	HTTP (80), HTTPS (443), SSH (22)
Connection Method	SSH (Client or Browser Terminal)

Screenshots
Here are the screenshots showing my progress:





What I Learned
How to create, configure, and connect to an AWS EC2 instance.

Basics of SSH connection and remote Linux server management.

Fundamentals of Infrastructure-as-a-Service (IaaS).

The importance of stopping instances to save costs and manage cloud resources effectively.

Conclusion
This task was a great hands-on experience with AWS EC2.
It helped me understand how cloud virtual machines work, how to access them remotely, and how to manage resources efficiently.
I feel much more confident navigating the cloud now and look forward to exploring more advanced cloud services in the future.

Author: Aishwarya Kopulwar
Role: Cloud Computing Intern — Elevate Labs
Date: October 2025
