Using the ansible deployments/provisioning script
=================================================

## Required Packages

* python / pip
* Vagrant
* ansible


## Setting Up Local Environment

### Get Vagrant   
https://www.vagrantup.com/downloads.html

### Have python2.7 on your computer

### clone this repo

### create a virtualenv
```
virtualenv env/ --python=python2.7
```

### Install ansible from requirements file
```
source env/bin/activate
pip install -r requirements.txt
```

### Vagrant up
```
vagrant up
```
Now you should have a development environment. If you need to manually profvision you can use or use ansible as shown below.
```
vagrant provision
```

### Verify  
go to http://localhost:8080 to see the phpinfo()
