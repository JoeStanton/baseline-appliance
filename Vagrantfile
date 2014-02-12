# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define :web do |web|
    web.vm.box = "precise64"
    web.vm.box_url = "http://files.vagrantup.com/precise64.box"
    web.vm.network :private_network, ip: "192.168.0.100"
    web.vm.synced_folder ".", "/vagrant"

    config.vm.provision :ansible do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--natdnsproxy1", "off"]
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "off"]
  end
end
