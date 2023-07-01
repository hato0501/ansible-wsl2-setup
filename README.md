# ansible-wsl2-setup
Ansible playbook for building WSL2 for development with devcontainer

## Quick Start
```sh
#!/bin/bash

# Update the package lists for upgrades for packages that need upgrading, as well as new packages that have just come to the repositories.
sudo apt-get update -y

# Install git
sudo apt-get install git -y

# Clone the Ansible playbook repository
git clone https://github.com/hato0501/ansible-wsl2-setup.git

# Go into the cloned directory
cd ansible-wsl2-setup

# Install ansible
sudo apt-get install software-properties-common -y
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt-get install ansible -y

# Run the Ansible playbook
ansible-playbook -i inventories/hosts.ini -l jammy playbook.yaml
```

## Please edit
- git config -> [roles/common/tasks/004_setup-git.yaml](roles/common/tasks/004_setup-git.yaml)

## Run
```sh
# Dry run
ansible-playbook -i inventories/hosts.ini -l jammy playbook.yaml --diff --check
 
# Real run
ansible-playbook -i inventories/hosts.ini -l jammy playbook.yaml --diff
```


## Stack
- common: [host_vars/localhost.yaml](host_vars/localhost.yaml)
- awscli

## Prerequired
- Ansible
