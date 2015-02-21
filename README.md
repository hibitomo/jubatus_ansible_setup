# jubatus_setup

Jubatus playbooks for Ubuntu.

## Ansible Install

```
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

And the ansible host should have SSH access available to remote hosts, based on SSH-Key.

## Setup Jubatus

### Download

```
$ git clone https://github.com/hibitomo/jubatus_setup
$ cd jubatus_setup
$ ansible-playbook ./playbooks/jubatus_distribute.yml -i hosts -u ansible -K
```

### Setup Inventory file

```
$ cat ./hosts
[jubatus]
127.0.0.1

[jubatus-client]
127.0.0.1
```

### Deploy

- `-i`: Inventory file
- `-u`: User name in remote host
- `-K`: Prompt for the password to use with sudo

example

```
$ ansible-playbook ./playbooks/jubatus_distribute.yml -i hosts -u jubatus -K
```
