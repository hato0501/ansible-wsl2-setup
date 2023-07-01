# ansible-wsl2-setup
Ansible playbook for building WSL2 for development with devcontainer

## Run
```sh
# Dry run
ansible-playbook -i inventories/hosts.ini -l jammy playbook.yaml --diff --check
 
# 実際に実行
ansible-playbook -i inventories/hosts.ini -l jammy playbook.yaml --diff
```


## Stack


## Prerequired