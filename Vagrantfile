# -*- mode: ruby -*-
# vi: set ft=ruby :

# Configuration Settings #######################################################
VAGRANTFILE_API_VERSION = "2"
VAGRANT_SCRIPT_DIR = "vagrantinstall"
VM_BOX = "ubuntu/trusty64"
SSH_PORT = 8022
WEB_PORT = 8080
SQL_PORT = 33306
MEMORY = 2048
################################################################################

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = VM_BOX
    config.vm.provision :shell, path: VAGRANT_SCRIPT_DIR+"/vagrant-bootstrap.sh"

    # Script an installation like Symfony or Laravel and add it here
    # config.vm.provision :shell, path: VAGRANT_BIN_DIR+"/install-something.sh", privileged: false

    config.vm.network "forwarded_port", guest: 22,   host: SSH_PORT
    config.vm.network "forwarded_port", guest: 80,   host: WEB_PORT
    config.vm.network "forwarded_port", guest: 3306, host: SQL_PORT

    config.vm.synced_folder ".", "/vagrant", id: "vagrant",
        owner: "vagrant",
        group: "www-data",
        nfs: false,
        mount_options: ["dmode=777,fmode=777"]

    config.vm.provider "virtualbox" do |vb|
        vb.customize ["modifyvm", :id, "--memory", MEMORY]
    end
end
