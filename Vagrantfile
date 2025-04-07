Vagrant.configure("2") do |config|
    config.vm.box = "bento/ubuntu-24.04"
    config.vm.hostname = "ubuntu2404"
    config.vm.network "private_network", type: "dhcp"
  
    config.vm.synced_folder ".", "/vagrant"
  
    config.vm.provision "shell", inline: <<-SHELL
    sudo apt update
    sudo apt install -y ansible
  SHELL

    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "/vagrant/playbook.yml"
        ansible.inventory_path = "/vagrant/inventory.ini"
        ansible.verbose = "v"
    end

    config.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 2
    end
  end
  