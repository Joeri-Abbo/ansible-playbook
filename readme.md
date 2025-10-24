# Ansible Playbook

A few playbooks to install and configure a few things on a new machine.

## Requirements

- Python 3.9+
- [pip](https://pip.pypa.io/)
- (Optional) [virtualenv](https://virtualenv.pypa.io/)

Install the tooling once with:

```bash
python3 -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
```

## Usage

- Clone the repo
- Copy `hosts.example` to `hosts` and list the target host(s)
- Copy `users.example.yaml` to `users.yaml` and define the users you want to create
- Run the playbook you need, e.g. `ansible-playbook user-create.yaml`

## Quality checks

Run the linters locally to ensure the playbooks stay healthy:

```bash
. .venv/bin/activate  # if you created a virtualenv
yamllint .
ansible-lint
```

GitHub Actions (`.github/workflows/ci.yml`) executes the same checks on every push and pull request.

## Playbooks

### Add Devops group

[add-devops-group.yaml](centos%2Fadd-devops-group.yaml)

### Install Dockerhost

[install-dockerhost.yaml](centos%2Finstall-dockerhost.yaml)

### Create users

[user-create.yaml](user-create.yaml)

### Add SSH Keys to users

[user-add-sshkeys.yaml](user-add-sshkeys.yaml)
