Using the ansible deployments/provisioning script
=================================================

## Required Packages

* python / pip
* Vagrant
* ansible
* libpq-dev (Postgres dependency)

### For Mac
```
brew install postgresql
```

### For Ubuntu
```
sudo apt-get install libpq-dev python-dev
```

## Setting Up Local Environment

1. Get Vagrant

```
vagrant up
```
Now you should have a development environment. If you need to manually profvision you can use or use ansible as shown below.

```
vagrant provision
```


## Deployment

Local Deployment shown but production/staging deployment is the same but just specifying different playbooks and using the right limit flag and private key for your environment. 

```
virtualenv env --python=python3
source env/bin/activate
pip install -r requirements.txt
ansible-playbook -i ansible.inventory provision.ansible.yaml --limit=local --private-key=~/.vagrant.d/insecure_private_key
```
Virtualenv suggested but not required
