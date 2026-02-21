# Ansible Web Server Automation

## Overview

This project demonstrates automated web server provisioning using Ansible.

Environment:
 - 3 Ubuntu 24.04 LTS servers on VirtualBox
 - 1 Ansible control node (ansible-mgmt)
 - 2 Managed nodes (app01, app02)


## Architecture

ansible-mgmt
 |--SSH -> app01
 |--SSH -> app02


## What This Playbook Does

- Install nginx
- Ensure nginx service is running
- Deploy HTML template
- Use Jinja2 templating
- Use group_vars for variable management
- Structured using Ansible Roles


## Directory Structure

ansible-practice/
 |----inventory
 |----site.yml
 |----group_vars/
 |  |
 |   ----web.yml
 |----roles/
 |----webserver/
 |----tasks/
 |----templates/
 |----defaults/
  ----README.md

 
## Key Concepts Demonstrated

- Idempotency (confirmed: changed=0 on second run)
- Infrastructure as Code
- Role-based structure
- Variable management
- Template rendering


## How to Run

ansible-playbook -i inventory site.yml


## Future Improvements

- Add handlers
- Environment separation (dev/prod)
- Ansible Vault integration

