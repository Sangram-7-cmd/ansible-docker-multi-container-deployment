# Ansible Docker Multi-Container Deployment

## Overview

This project automates Docker installation and multi-container deployment using Ansible Roles.

The role installs Docker, starts the Docker service, installs required Python dependencies, and deploys multiple containers using a reusable and scalable configuration.

---

## Features

- Docker Installation
- Docker Service Management
- Multi-Container Deployment
- Port Mapping
- Volume Mapping
- Environment Variable Support
- Reusable Ansible Role
- Group Variables
- Role Defaults
- Idempotent Execution

---

## Project Structure

```text
.
├── ansible.cfg
├── inventory
├── group_vars/
├── collections/
├── roles/
│   └──  docker/
        ├── defaults/
        ├── tasks/
        ├── templates/
        ├── handlers/
        └── vars/
└── site.yml
```

## Containers Deployed

### Nginx

- Port Mapping: 8080:80
- Custom HTML Template Deployment
- Volume Mapping

### Redis

- Port Mapping: 6379:6379
- Environment Variable Support

---

## Technologies Used

- Ansible
- Docker
- Rocky Linux
- Jinja2 Templates

---

## Run Project

Install collection:

```bash
ansible-galaxy collection install -r collections/requirements.yml
```

Run playbook:

```bash
ansible-playbook site.yml
```

---

## Learning Outcomes

- Ansible Roles
- Group Variables
- Default Variables
- Loops
- import_tasks
- Docker Modules
- Infrastructure Automation
- Idempotent Configuration Management
