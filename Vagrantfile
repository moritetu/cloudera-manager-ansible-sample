Vagrant.configure(2) do |config|
  config.vm.box = "centos/6"
  config.vm.network "forwarded_port", guest: 22, host: 2225
  config.vm.network "forwarded_port", guest: 7180, host: 7180
  config.vm.network "private_network", ip: "192.168.10.10"

  config.hostmanager.enabled = false
  config.hostmanager.manage_host = true
  config.hostmanager.manage_guest = true
  config.hostmanager.ignore_private_ip = false

  config.vm.hostname = "scm"

  config.vm.provider :virtualbox do |vb|
    vb.name = "scm"
    vb.memory = 4096
    vb.cpus = 2
  end
  config.vm.provision "ansible" do |ansible|
    ansible.verbose  = true
    ansible.playbook = "vagrant.yml"
  end
  config.vm.provision :shell, :inline => 'echo "127.0.0.1    localhost" > /etc/hosts'
  config.vm.provision :hostmanager
end
