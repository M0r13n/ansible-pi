# Ansible playbooks for all my raspberry pi projects
This is a collection of Ansible playbooks that I use to manage my fleet of raspberries.

This will always be a work in progress and I will constantly add/change/improve things. Feel free to use any of the playbooks.

## Setup
1. Install Python3:
  1. `sudo apt install python3`
1. Install pip:
  2. `sudo apt install python3-pip python3-venv`
1. Install Ansible
  1. `pip3 install ansible`
1. Clone this repo. 
1. Install dependencies:
 1. `ansible-galaxy collection install -r requirements.yml`


## Playbooks

### Default

Path: `./playbooks/default.yml`

- sets default settings
- sets correct locale, hostname and timezone
- updates packages via apt

### Docker

Path: `./playbooks/docker.yml`

- Installs Docker
- Installs Docker-Compose
- run with `ansible-playbook  playbooks/docker.yml --become --limit docker`
