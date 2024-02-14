Vagrant.configure("2") do |config|
    config.vm.provider :vmware_workstation do |vmware, override|
      vmware.gui = false
      vmware.vmx["numvcpus"] = "2"
    end
    
    config.vm.define "master" do |master|
      master.vm.box = "bento/ubuntu-20.04"
      master.vm.hostname = "master"
      master.vm.network "private_network", ip: "192.168.50.10"
      master.vm.provision "ansible" do |ansible|
        ansible.playbook = "provision/master/playbook.yml"
        ansible.config_file = "provision/ansible.cfg"
      end
    end
  
    config.vm.define "node" do |node|
      node.vm.box = "bento/ubuntu-20.04"
      node.vm.hostname = "node"
      node.vm.network "private_network", ip: "192.168.50.11"
      node.vm.provision "ansible" do |ansible|
        ansible.playbook = "provision/node/playbook.yml"
        ansible.config_file = "provision/ansible.cfg"
      end
    end
  end
  