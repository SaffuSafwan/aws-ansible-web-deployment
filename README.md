
# AWS Multi-Server Website Deployment Using Ansible

## Project Overview
Automated the deployment of a static website across three AWS EC2 instances using Ansible and Nginx.

A dedicated EC2 instance acts as the Ansible control node, managing three remote servers through SSH.

## Technologies Used
- AWS EC2
- Ansible
- Nginx
- Ubuntu Linux
- SSH
- YAML
- HTML

## Architecture
- 1 EC2 instance: Ansible Control Node
- 3 EC2 instances: Managed Web Servers

The control node uses Ansible to configure and deploy the website to all three managed servers.

## Implementation
1. Provisioned four Ubuntu EC2 instances on AWS.
2. Configured SSH authentication between the control node and managed servers.
3. Installed Ansible on the control node.
4. Configured the Ansible inventory.
5. Verified connectivity using the Ansible ping module.
6. Created a YAML playbook to automate:
   - Nginx installation
   - HTML website deployment
   - Nginx service startup and enablement
7. Executed the playbook across all three managed servers.
8. Verified that each server successfully hosted the website over HTTP.

## Deployment Command

```bash
ansible-playbook deploy.yml
```

## Results
- Successfully deployed the same website across three EC2 instances.
- Automated web server installation and configuration.
- Verified successful execution with zero failed or unreachable hosts.
- Confirmed website accessibility through all three servers.

## Security Notes
SSH private keys and AWS credentials are excluded from version control.

## Future Improvements
- Automate EC2 provisioning using Terraform.
- Configure HTTPS using TLS certificates.
- Add CI/CD using GitHub Actions.

