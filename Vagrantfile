# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  #config.vm.box = "hashicorp/precise32"
  config.vm.define :front do |front|
    front.vm.hostname = "front"
    front.vm.box = "hashicorp/precise32"
    front.vm.network "private_network", ip: "192.168.33.10"
  end
  config.vm.define :worker do |worker|
    worker.vm.hostname = "worker"
    worker.vm.box = "hashicorp/precise32"
    worker.vm.network "private_network", ip: "192.168.33.20"
  end
  # config.vm.box_check_update = false
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  # config.vm.synced_folder "../data", "/vagrant_data"
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
end
