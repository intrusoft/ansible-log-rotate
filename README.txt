# SRE Ansible Playbooks

This repo contains the Ansible playbooks needed for managing system XYZ
infrastructure. Maintained by team ABC.

## Playbooks

### logrotate.yml: Configures log rotation for 'custom-monitor'

## Requirements
- Ansible version x.x.x
- SSH access with sudo to target machines

## Controller Setup
```bash
python3 -m venv ~/.venvs/ansible
source ~/.venvs/ansible/bin/activate
pip install --upgrade pip
pip install ansible

## Testing Ad-Hoc Command Example
ansible --private-key ../sre-logrotate-0.pem -u ubuntu all -m shell -a "uptime" -i inventory.yml

## How to Run Playbook
ansible-playbook -i inventory.yml logrotate.yml --private-key ../sre-logrotate-0.pem

## Helpful Links
- Ansible Inventory https://docs.ansible.com/projects/ansible/latest/inventory_guide/intro_inventory.html
- Ansible Playbooks https://docs.ansible.com/projects/ansible/latest/playbook_guide/index.html
- Index of Ansible modules https://docs.ansible.com/projects/ansible/latest/collections/all_plugins.html


