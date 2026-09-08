# AWS EC2 Linux Server Deployment & Administration

## 📌 Project Overview

This project demonstrates the deployment and administration of a Linux server using Amazon EC2.

The project covers AWS EC2 configuration, SSH connectivity, Linux user and group management, file permissions, Nginx web server deployment, SSH security, server logs, system monitoring, and web-service testing.

## 🛠️ Technologies Used

- AWS EC2
- Ubuntu Linux
- SSH
- Git Bash
- Nginx
- Linux Commands
- Security Groups
- systemd
- curl

## 🏗️ Architecture

Windows Laptop
      |
      | SSH
      ↓
AWS EC2 Instance
      |
      ↓
Ubuntu Linux Server
      |
      ↓
Nginx Web Server
      |
      ↓
Custom Website

## 🔧 Project Implementation

### 1. EC2 Instance Setup

- Created an AWS EC2 instance
- Selected Ubuntu Linux
- Configured a key pair
- Configured Security Group rules
- Connected to the server using SSH

### 2. Linux Server Verification

Verified the Linux server using:

```bash
whoami
pwd
uname -a
df -h
free -h
