 # Linux Commands Used

## Server Verification

```bash
whoami
pwd
uname -a
df -h
free -h
 ## User Management
sudo adduser projectuser
id projectuser
 ## Group Management
sudo groupadd cloudteam
sudo usermod -aG cloudteam projectuser
groups projectuser
 ## File Permissions
mkdir ~/project
touch ~/project/test.txt
ls -l ~/project
chmod 640 ~/project/test.txt
 ## Nginx
sudo apt update
sudo apt install nginx -y
sudo systemctl status nginx
sudo systemctl restart nginx
 ## SSH Security
sudo sshd -T | grep -E "port|permitrootlogin|passwordauthentication"
 ## SSH Logs
sudo journalctl -u ssh --no-pager -n 20
## Nginx Logs
sudo tail -n 20 /var/log/nginx/access.log
sudo tail -n 20 /var/log/nginx/error.log
 ## System Monitoring
uptime
top
free -h
df -h
 ## Nginx Testing
curl -I http://localhost
curl http://localhost | head -20
## Service Verification
systemctl is-active nginx
systemctl is-active ssh
hostname
