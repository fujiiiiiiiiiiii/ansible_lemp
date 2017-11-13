Vagrant.configure(2) do |config|
  config.vm.provider "virtualbox"
  config.vm.box = "centos71"
  config.vm.box_url = "https://dl.dropboxusercontent.com/s/4bggam4yjdhhfpf/centos-7.1-x86_64.box"

  config.vm.provider :virtualbox do |vbox|
    vbox.name = "local-lemp"
  end

  config.vm.network "private_network", ip: "192.168.111.222"

# provision by shell
  config.vm.provision "shell", inline: <<-SHELL
    # ansible
    sudo ansible-playbook -i /vagrant/ansible/hosts.local /vagrant/ansible/playbook.yml --connection=local -vvvv
  SHELL
end
