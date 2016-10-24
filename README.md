Using the ansible deployments/provisioning script
=================================================

## Required Packages

* Vagrant
* ansible

## Setting Up Local Environment

1. Get Vagrant

2. pip install ansible

```
pip install ansible
```

3. Vagrant up

```
cd /path/to/folder && vagrant up
```

if vagrant up doesn't provision or if you want to manually provision you can call ansible-playbook manually like so
```
ansible-playbook -i ansible.inventory provision.ansible.yaml --limit=local --private-key=~/.vagrant.d/insecure_private_key
```
