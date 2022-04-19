# -*- mode: ruby -*-
# vi: set ft=ruby :

#CONFIG VAGRANT
Vagrant.configure("2") do |config|
  #DEFINE BOX NGINX
  config.vm.define "samba" do |samba|
    #DEFINE BOX OS
    samba.vm.box = "ubuntu/bionic64"
    #DEFINE BOX IP (PREFERABLY ON 192.168.56.0/21 RANGE)
    samba.vm.network "private_network", ip: "192.168.56.56"
    #DEFINE PATH TO THE ANSIBLE PLAYBOOK
    samba.vm.provision "ansible", playbook: "provisioning/samba.yml"
  end
end
