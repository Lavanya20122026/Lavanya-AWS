# Amazon EC2 - Notes & Hands-on

## Overview

Amazon EC2 (Elastic Compute Cloud) provides virtual servers in the cloud. It allows users to launch and manage compute resources on demand.

---

##  Key Concepts

### EC2 Instance

* Virtual machine in AWS
* Runs applications like a normal server

### AMI (Amazon Machine Image)

* Pre-configured OS template
* Example: Amazon Linux, Ubuntu

### Instance Types

* General Purpose → balanced
* Compute Optimized → high CPU
* Memory Optimized → high RAM

---

## 💾 Storage

### EBS

* Persistent storage
* Data remains after stop/start

### Instance Store

* Temporary storage
* Data lost when instance stops

---

##  Security Groups

* Acts as a firewall for EC2
* Controls inbound and outbound traffic

### Common Ports

* 22 → SSH
* 80 → HTTP
* 443 → HTTPS

### Key Rule

* Timeout issue → Security Group problem

---

##  EC2 User Data

* Script executed at first launch only
* Used for automation

### Use Cases

* Install software
* Configure server
* Deploy application

---

##  Key Pair

* Used for authentication
* `.pem` → SSH
* `.ppk` → PuTTY

---

##  Networking

* Public IP → internet access
* Private IP → internal communication

### Important

* Public IP changes after restart
* Private IP remains same

---

##  IAM Role

* Provides permissions to EC2
* Avoid storing access keys inside instance

---

##  Pricing Options

* On-Demand → pay per use
* Reserved → long-term discount
* Spot → cheapest, can be interrupted

---

##  Hands-on Summary

### EC2 Instance Creation

1. Choose AMI (Amazon Linux)
2. Select instance type (t2.micro)
3. Create key pair
4. Configure Security Group (SSH, HTTP)
5. Add User Data script
6. Launch instance

---

### Security Groups Hands-on

* Allowed port 22 (SSH) for remote access
* Allowed port 80 (HTTP) for website access
* Verified timeout issue when port was removed

---

### SSH Access

#### Using Windows (PowerShell)

* Used `.pem` file
* Connected using SSH command

#### Using EC2 Instance Connect

* Browser-based SSH
* No key management required

---

## Key Learnings

* EC2 is the foundation of compute in AWS
* Security Groups control access
* User Data automates setup
* IAM Roles are secure way to provide access
* Public IP behavior is important for connectivity

---


