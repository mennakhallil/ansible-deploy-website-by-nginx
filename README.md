# Nginx Website Deployment with Ansible

Ansible playbook to deploy a website using Nginx.

## Requirements

- Ansible installed
- SSH access to servers
- Sudo privileges

## Setup

 Edit `inventory/hosts` with your server IP:
```ini
[webservers]
server1 ansible_host=YOUR_SERVER_IP ansible_user=ubuntu
```



## Usage

Deploy the website:
```bash
ansible-playbook -i inventory/hosts deploy-website.yml
```

Check without making changes:
```bash
ansible-playbook -i inventory/hosts deploy-website.yml --check
```

## What it does

- Installs Nginx
- Copies website files
- Configures Nginx
- Starts the service

## Test

Visit your server IP in a browser:
```
http://YOUR_SERVER_IP
```

## Author

Menna Khalil
