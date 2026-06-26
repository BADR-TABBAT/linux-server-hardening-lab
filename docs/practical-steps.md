# Practical Steps

## 1. Update the System

The first step is to update the package list and upgrade installed packages.

```bash
sudo apt update
sudo apt upgrade -y
```

## 2. Create a New User

Create a new user for administration instead of using the root account directly.

```bash
sudo adduser adminuser
sudo usermod -aG sudo adminuser
```

## 3. Check SSH Service

Verify if SSH is installed and running.

```bash
sudo systemctl status ssh
```

## 4. Secure SSH Configuration

Edit the SSH configuration file.

```bash
sudo nano /etc/ssh/sshd_config
```

Recommended settings:

```text
PermitRootLogin no
PasswordAuthentication yes
```

Restart SSH after saving changes.

```bash
sudo systemctl restart ssh
```

## 5. Configure Firewall with UFW

Allow SSH before enabling the firewall.

```bash
sudo ufw allow ssh
sudo ufw enable
sudo ufw status
```

## 6. Check Open Ports

List listening services and open ports.

```bash
sudo ss -tulnp
```

## 7. Review Users

Check existing users on the system.

```bash
cat /etc/passwd
```

## 8. Check File Permissions

Example command to check permissions.

```bash
ls -l /etc/passwd
```

## 9. Disable Unnecessary Services

List active running services.

```bash
systemctl list-units --type=service --state=running
```

Disable a service if it is not needed.

```bash
sudo systemctl disable service-name
sudo systemctl stop service-name
```

## 10. Final Verification

After applying the hardening steps, verify the system status.

```bash
sudo ufw status
systemctl status ssh
ss -tulnp
```

## Summary

This practical section covers basic Linux server hardening steps:

- System updates
- Admin user creation
- SSH security
- Firewall configuration
- Open ports verification
- User review
- File permissions checking
- Service management
