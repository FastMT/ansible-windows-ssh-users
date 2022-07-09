# ansible-windows-ssh-users
Ansible template to configure users in Windows ssh server 

## Installation

Create requirements.yml file

```
# Include windows-ssh-users role
- src: https://github.com/FastMT/ansible-windows-ssh-users.git
  name: windows-ssh-users
  version: "v1.0.0"
```

Install external module into ~/.ansible/roles folder

```
ansible-galaxy install -r requirements.yml
```

## Usage

playbook.yml:

```
# Configure users
- role: "windows-ssh-users"
    vars:
      admin_users:
        - { user: "user1", ssh_key: "ssh-rsa AAAAB3NzaC1yc2E...." }
        - { user: "user2", ssh_key: "ssh-rsa AAAAB3NzaC1yc2E...." }
```        
