# Linux Server Hardening Checklist

This checklist summarizes the basic security hardening steps for an Ubuntu Linux server.

## 1. System Updates

- [ ] Update package list
- [ ] Upgrade installed packages
- [ ] Remove unused packages
- [ ] Reboot the server if required

## 2. User Management

- [ ] Create a dedicated admin user
- [ ] Add the admin user to the sudo group
- [ ] Avoid using the root account directly
- [ ] Review existing user accounts
- [ ] Remove unnecessary users
- [ ] Use strong passwords

## 3. SSH Security

- [ ] Check if SSH service is running
- [ ] Disable root login via SSH
- [ ] Review SSH authentication settings
- [ ] Allow only required users if needed
- [ ] Restart SSH service after changes
- [ ] Test SSH access before closing the current session

## 4. Firewall Configuration

- [ ] Enable UFW firewall
- [ ] Allow SSH before enabling the firewall
- [ ] Allow only required ports
- [ ] Deny unnecessary services
- [ ] Check firewall status
- [ ] Review firewall rules regularly

## 5. Network Security

- [ ] Check server IP configuration
- [ ] Verify routing configuration
- [ ] Check open ports
- [ ] Identify listening services
- [ ] Disable unused network services

## 6. Service Management

- [ ] List running services
- [ ] Identify unnecessary services
- [ ] Stop unused services
- [ ] Disable unused services at startup
- [ ] Monitor critical services

## 7. File Permissions

- [ ] Check important system file permissions
- [ ] Apply the least privilege principle
- [ ] Avoid world-writable permissions
- [ ] Review ownership of important files
- [ ] Protect sensitive configuration files

## 8. Logs and Monitoring

- [ ] Check system logs
- [ ] Check authentication logs
- [ ] Review failed login attempts
- [ ] Monitor disk usage
- [ ] Monitor memory usage
- [ ] Monitor running processes

## 9. Basic Security Verification

- [ ] Verify UFW status
- [ ] Verify SSH configuration
- [ ] Check open ports
- [ ] Check users with sudo privileges
- [ ] Review active services
- [ ] Document all changes

## 10. Documentation

- [ ] Document commands used
- [ ] Document configuration changes
- [ ] Record issues encountered
- [ ] Record solutions applied
- [ ] Keep the checklist updated

## Future Improvements

- [ ] Configure SSH key-based authentication
- [ ] Install and configure Fail2Ban
- [ ] Configure automatic security updates
- [ ] Add log monitoring
- [ ] Create a backup strategy
- [ ] Add intrusion detection tools
