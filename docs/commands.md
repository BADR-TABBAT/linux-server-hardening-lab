# Useful Linux Commands

This document contains useful Linux commands for basic server administration and hardening.

## 1. System Information

```bash
hostnamectl
uname -a
uptime
whoami
```

## 2. System Updates

Update package list:

```bash
sudo apt update
```

Upgrade installed packages:

```bash
sudo apt upgrade -y
```

Remove unused packages:

```bash
sudo apt autoremove -y
```

## 3. Users and Groups

Check current user:

```bash
whoami
```

Display user ID and groups:

```bash
id
```

List system users:

```bash
cat /etc/passwd
```

List groups:

```bash
cat /etc/group
```

Create a new user:

```bash
sudo adduser username
```

Add user to sudo group:

```bash
sudo usermod -aG sudo username
```

## 4. SSH Management

Check SSH service status:

```bash
sudo systemctl status ssh
```

Edit SSH configuration file:

```bash
sudo nano /etc/ssh/sshd_config
```

Restart SSH service:

```bash
sudo systemctl restart ssh
```

Enable SSH at system startup:

```bash
sudo systemctl enable ssh
```

## 5. Firewall UFW

Check firewall status:

```bash
sudo ufw status
```

Allow SSH:

```bash
sudo ufw allow ssh
```

Allow HTTP:

```bash
sudo ufw allow 80
```

Allow HTTPS:

```bash
sudo ufw allow 443
```

Deny Telnet:

```bash
sudo ufw deny 23
```

Enable firewall:

```bash
sudo ufw enable
```

Disable firewall:

```bash
sudo ufw disable
```

## 6. Services Management

List running services:

```bash
systemctl list-units --type=service --state=running
```

Check service status:

```bash
systemctl status service-name
```

Stop a service:

```bash
sudo systemctl stop service-name
```

Start a service:

```bash
sudo systemctl start service-name
```

Restart a service:

```bash
sudo systemctl restart service-name
```

Disable a service at startup:

```bash
sudo systemctl disable service-name
```

Enable a service at startup:

```bash
sudo systemctl enable service-name
```

## 7. Network Commands

Show IP addresses:

```bash
ip a
```

Show routing table:

```bash
ip route
```

Test connectivity:

```bash
ping 8.8.8.8
```

Show open ports and listening services:

```bash
sudo ss -tulnp
```

Show network interfaces:

```bash
ip link show
```

## 8. File Permissions

List files with permissions:

```bash
ls -l
```

Change file permissions:

```bash
chmod 644 file-name
```

Change directory permissions:

```bash
chmod 755 directory-name
```

Change file owner:

```bash
sudo chown user:group file-name
```

Check permissions of important system file:

```bash
ls -l /etc/passwd
```

## 9. Logs and Monitoring

View system logs:

```bash
journalctl
```

View recent logs:

```bash
journalctl -xe
```

Check authentication logs:

```bash
sudo cat /var/log/auth.log
```

Monitor system processes:

```bash
top
```

Check disk usage:

```bash
df -h
```

Check memory usage:

```bash
free -h
```

## 10. Security Verification

Check open ports:

```bash
sudo ss -tulnp
```

Check firewall rules:

```bash
sudo ufw status verbose
```

Check failed login attempts:

```bash
sudo grep "Failed password" /var/log/auth.log
```

Check users with sudo privileges:

```bash
getent group sudo
```

## Notes

These commands are used in a lab environment to practice Linux server administration and basic hardening.

Before applying changes on a real server, each command should be tested carefully and documented.
