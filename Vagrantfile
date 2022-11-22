# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"
  config.vm.box_check_update = true
  config.vm.hostname = "royee-ubuntu"
  config.vm.post_up_message = "use the vagrant shh command to access the vm"
  config.vm.synced_folder "~", "/home/royee"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 2
  end
  config.vm.provision :shell, path: "bootstrap.sh"
end
