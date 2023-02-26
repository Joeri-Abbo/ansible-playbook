Ansible Playbook
================
A few playbooks to install and configure a few things on a new machine.

## Requirements

- Ansible
- Python

## Usage

- Clone the repo
- Edit the hosts file to include the IP address of the machine you want to configure
- Specify the users.yaml with the users you want to create
- Run the playbook

## Playbooks

### Add Devops group

[add-devops-group.yaml](centos%2Fadd-devops-group.yaml)

### Install Dockerhost

[install-dockerhost.yaml](centos%2Finstall-dockerhost.yaml)

### Create users

[user-create.yaml](user-create.yaml)

### Add SSH Keys to users

[user-add-sshkeys.yaml](user-add-sshkeys.yaml)