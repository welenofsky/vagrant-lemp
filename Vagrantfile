# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"


Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.network :forwarded_port, guest: 443, host: 8443
  config.vm.network :forwarded_port, guest: 8888, host: 8888

  config.ssh.insert_key = false
  config.ssh.private_key_path = ["~/.vagrant.d/insecure_private_key"]

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision.ansible.yaml"
    ansible.inventory_path = "ansible.inventory"
    ansible.limit = "local"
  end

end
