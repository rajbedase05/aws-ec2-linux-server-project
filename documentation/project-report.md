# AWS EC2 Linux Server Deployment & Administration

## 1. Project Title

AWS EC2 Linux Server Deployment & Administration

## 2. Introduction

This project demonstrates the deployment and administration of an Ubuntu Linux server using Amazon Web Services (AWS) EC2.

The project focuses on practical Linux system administration, SSH connectivity, user and group management, file permissions, Nginx web server deployment, security configuration, log analysis, system monitoring, and basic troubleshooting.

## 3. Objectives

The main objectives of this project are:

- Deploy a Linux server using AWS EC2.
- Connect to the server using SSH.
- Practice Linux system administration.
- Create and manage Linux users and groups.
- Configure file and directory permissions.
- Install and manage the Nginx web server.
- Host a custom website.
- Review SSH and Nginx logs.
- Monitor CPU, memory, disk, and system uptime.
- Test web services using command-line tools.

## 4. Technologies Used

- AWS EC2
- Ubuntu Linux
- SSH
- Git Bash
- Nginx
- Linux
- Security Groups
- systemd
- curl

## 5. Project Architecture

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

## 6. EC2 Server Deployment

An Ubuntu Linux EC2 instance was launched in AWS.

The EC2 configuration included:

- Ubuntu Linux AMI
- EC2 instance
- Key pair
- Security Group
- SSH access
- HTTP access for the web server

The server was successfully accessed remotely using SSH from a Windows laptop through Git Bash.

## 7. Linux Server Administration

The Linux server environment was verified using commands such as:

```bash
whoami
pwd
uname -a
df -h
free -h
8. User and Group Management

A dedicated Linux user named projectuser was created.

sudo adduser projectuser

A Linux group named cloudteam was created:

sudo groupadd cloudteam

The user was added to the group:

sudo usermod -aG cloudteam projectuser

User and group membership was verified using:

id projectuser
groups projectuser
9. File Permissions

A project directory and test file were created:

mkdir ~/project
touch ~/project/test.txt

File permissions were modified using:

chmod 640 ~/project/test.txt

The permission configuration was verified using:

ls -l ~/project

This demonstrated practical understanding of Linux file permissions.

10. Nginx Web Server Deployment

Nginx was installed using:

sudo apt update
sudo apt install nginx -y

The Nginx service was checked using:

sudo systemctl status nginx

A custom HTML website was configured and hosted through Nginx.

The website was successfully accessed through the EC2 public web endpoint.

11. SSH Security Configuration

The effective SSH configuration was checked using:

sudo sshd -T | grep -E "port|permitrootlogin|passwordauthentication"

The server was verified to use SSH on port 22 and key-based authentication.

SSH logs were also reviewed to understand successful and unsuccessful connection attempts.

12. SSH Log Analysis

SSH activity was reviewed using:

sudo journalctl -u ssh --no-pager -n 20

The logs demonstrated:

SSH server startup
Successful public-key authentication
Authentication connection attempts
Connection failures
SSH service activity
13. Nginx Log Analysis

Nginx access logs were reviewed using:

sudo tail -n 20 /var/log/nginx/access.log

Nginx error logs were reviewed using:

sudo tail -n 20 /var/log/nginx/error.log

Log analysis was used to understand web-server requests and identify possible service issues.

14. Linux System Monitoring

System resources were monitored using:

uptime
top
free -h
df -h

These commands provided information about:

System uptime
CPU and running processes
Memory usage
Disk usage
15. Nginx Service Testing

The Nginx web server was tested locally using:

curl -I http://localhost

The website content was also verified using:

curl http://localhost | head -20

A successful HTTP response confirmed that the Nginx service was serving the website correctly.

16. Final Verification

The final server configuration was verified using:

id
systemctl is-active nginx
systemctl is-active ssh
hostname

Both Nginx and SSH services were confirmed to be active.

17. Skills Demonstrated

This project demonstrates practical knowledge of:

AWS EC2
Linux administration
SSH
Linux users and groups
Linux file permissions
Nginx
Security Groups
Service management
Log analysis
System monitoring
Web-server troubleshooting
Command-line administration
18. Project Outcome

Successfully deployed and administered an Ubuntu Linux server on AWS EC2.

The project provided hands-on experience with cloud infrastructure, Linux administration, SSH security, web-server deployment, permissions, log analysis, system monitoring, and troubleshooting.

19. Screenshots

Implementation screenshots are available in the screenshots directory of this repository.

20. Author

Rajwardhan Bedase

