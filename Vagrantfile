# -*- mode: ruby -*-
# vi: set ft=ruby :

#CONFIG VAGRANT
Vagrant.configure("2") do |config|
  #DEFINE BOX NGINX
  config.vm.define "avaliacao3" do |avaliacao3|
    #DEFINE BOX OS
    avaliacao3.vm.box = "ubuntu/bionic64"
    #DEFINE BOX IP (PREFERABLY ON 192.168.56.0/21 RANGE)
    avaliacao3.vm.network "private_network", ip: "192.168.56.56"
    #PROVISION NGINX SERVER
    avaliacao3.vm.provision "ansible", playbook: "provisioning/nginx/nginx.yml"
    #PROVISION SAMBA SERVER
    avaliacao3.vm.provision "ansible", playbook: "provisioning/samba/samba.yml"
    #PROVISION EMAIL SERVER
    avaliacao3.vm.provision "ansible", playbook: "provisioning/email/email.yml"
    #PROVISION FTP SERVER
    avaliacao3.vm.provision "ansible", playbook: "provisioning/ftp/ftp.yml"
    #PROVISION FIREWALL
    avaliacao3.vm.provision "ansible", playbook: "provisioning/firewall/firewall.yml"
    #PROVISION MYSQL
    avaliacao3.vm.provision "ansible", playbook: "provisioning/database/database.yml"
    #PROVISION SQUID PROXY SERVER
    avaliacao3.vm.provision "ansible", playbook: "provisioning/proxy/proxy.yml"
  end
end
