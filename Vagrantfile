# -*- mode: ruby -*-
# vi: set ft=ruby :

# Provision shell setup script
$script = <<SCRIPT
sudo apt-get install python-pip -y
pip install -r /home/vagrant/vagrant_sync/pip_requirements.txt
SCRIPT


Vagrant.configure("2") do |config|
  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "hashicorp/precise64"
  config.vm.box_version = "1.1.0"

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:5000" will access port 5000 on the guest machine.
  config.vm.network "forwarded_port", guest: 5000, host: 5000

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  config.vm.synced_folder "./app", "/home/vagrant/vagrant_sync"

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  config.vm.provision "shell", inline: $script
end
