# Notes

This document contains personal notes, challenges, solutions, and lessons learned during the Linux Server Hardening Lab.

## Challenges

- Understanding the difference between normal users and sudo users
- Knowing which services are necessary and which services can be disabled
- Securing SSH without losing remote access
- Configuring firewall rules carefully
- Understanding Linux file permissions
- Checking open ports and running services

## Solutions

- Applied hardening steps progressively
- Tested each command in a lab environment
- Allowed SSH before enabling the firewall
- Reviewed active services before disabling anything
- Used documentation to organize commands and configuration steps
- Kept a checklist to track completed security actions

## Lessons Learned

- Linux server security starts with basic configuration
- System updates are essential for security and stability
- SSH must be secured because it is commonly used for remote administration
- A firewall should allow only required services
- User permissions must follow the principle of least privilege
- Documentation is important in system administration and cybersecurity

## Good Practices

- Keep the system updated regularly
- Use a dedicated admin user instead of working directly as root
- Review SSH configuration before restarting the service
- Allow SSH in the firewall before enabling UFW
- Check open ports regularly
- Disable unused services
- Monitor logs for suspicious activity
- Document every important change

## Common Commands Used

```bash
sudo apt update
sudo apt upgrade -y
sudo ufw status
sudo ufw allow ssh
sudo ufw enable
sudo systemctl status ssh
sudo ss -tulnp
systemctl list-units --type=service --state=running
