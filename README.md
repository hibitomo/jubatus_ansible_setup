# jubatus_setup

## ansible install

```
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

## setup jubatus

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

- `-u`: user name in remote host
- `-K`: Prompt for the password to use with sudo

example

```
$ ansible-playbook ./playbooks/jubatus_distribute.yml -i hosts -u jubatus -K
```
