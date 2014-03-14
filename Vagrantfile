# -*- mode: ruby -*-
# vi: set ft=ruby :

VM_MEMORY = 4*1024
VM_CORES = 4

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = 'gentoo-2013-10-29'
  config.vm.hostname = 'cpp-craft'
  config.vm.box_url = 'https://dl.dropboxusercontent.com/s/xfl63k64zliixid/gentoo-20131029-i686.box'

  config.vm.provider :virtualbox do |vb|
    vb.customize ['modifyvm', :id, '--memory', VM_MEMORY]
    vb.customize ['modifyvm', :id, '--cpus',   VM_CORES]
  end

  config.vm.provision :chef_solo do |chef|
    chef.add_recipe 'build-essential'
    chef.add_recipe 'boost::source'
  end

end
