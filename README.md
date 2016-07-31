# Vagrant LAMP Box

## Originally authored by panique ([link](https://www.dev-metal.com/super-simple-vagrant-lamp-stack-bootstrap-installable-one-command/))

## Packed with all LAMP (Apache 2 & PHP5) packages you need, plus...

* Git for version control of your project
* Other Esssential Tools for development

## Getting Started

* Clone the project

* Download VirtualBox at [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads "VirtualBox - Downloads") (*"platform packages"*) and install it.  
* Download Vagrant at [https://www.vagrantup.com/downloads.html](https://www.vagrantup.com/downloads.html "Vagrant - Downloads") and install it.

From the project root, run:

    `vagrant up`

Edit the `hosts` file of your machine, add:

    `192.168.68.8    vagrant-test.local.com`

Open your browser and visit http://vagrant-test.local.com

Voila! And that's it!

## Other suggestions

* If you having a 32-bit physical machine using, you can change the `config.vm.box` value into ` "ubuntu/trusty32" ` or whatever dist you want on your VM.
