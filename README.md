Using the ansible deployments/provisioning script
=================================================

## Required Packages

* python / pip
* Vagrant
* ansible


## Setting Up Local Environment

1. Get Vagrant
https://www.vagrantup.com/downloads.html

2. Have python2.7 on your computer

3. clone this repo

4. create a virtualenv
```
virtualenv env/ --python=python2.7
```

5. Install ansible from requirements file
```
source env/bin/activate
pip install -r requirements.txt
```

6. Vagrant up
```
vagrant up
```
Now you should have a development environment. If you need to manually profvision you can use or use ansible as shown below.
```
vagrant provision
```
7. Verify  
go to http://localhost:8080 to see the phpinfo()
