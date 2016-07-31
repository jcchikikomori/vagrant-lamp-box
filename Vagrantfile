# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # Used box
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = 'vagrant-lamp-box'

  # Accessing "localhost:8080" will access port 80 on the guest machine.
  config.vm.network :forwarded_port, guest: 80, host: 8080

  # Private Network
  config.vm.network :private_network, ip: "192.168.68.8"

  # Share an additional folder to the guest VM. The first argument is the path on the host to the actual folder.
  # The second argument is the path on the guest to mount the folder.
  config.vm.synced_folder "./", "/var/www/html"

  # Install stuff
  config.vm.provision :shell, :path => ".provision/bootstrap.sh"

  # uncomment the following lines when having trouble with the box's start up
  config.vm.provider :virtualbox do |vb|
   vb.gui = false
   vb.memory = 1024
  end

end
