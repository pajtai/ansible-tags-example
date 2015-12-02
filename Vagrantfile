# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.provider "virtualbox" do |v|
      host = RbConfig::CONFIG['host_os']
  end

  config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "192.168.12.148"

  config.vm.provision :ansible do |ansible|
     ansible.playbook = "ansible/site.yml"
     ansible.inventory_path = "ansible/hosts"
     ansible.verbose = "v"
     ansible.limit = "vagrant"
     ansible.tags = "example-3"
  end
end
