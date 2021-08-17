# ansible-playbooks
## Installing Ansible

https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-specific-operating-systems


## Clone this repository 

```bash
# git clone https://github.com/franrebo84/ansible-playbooks
# cd ansible_hardering_apache
```

## Preerequisites

Install required roles:

```bash 
# ansible-galaxy install -r requirements.yml
```


## Setting inventory file

Edit inventory file and change IP address, username, password and desired ssh port.

```
[servers]
myserver ansible_host=192.168.88.21 ansible_user=ubuntu ansible_password=ubuntu ansible_become_pass=ubuntu 
```


## Runing the Playbooks

Firt you must run ssh.yml playbook. This will change default ssh port to whatever is defined in inventory.

```bash
# ansible-playbook -i inventory install_docker.yml -v
```
