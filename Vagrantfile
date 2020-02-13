
Vagrant.configure("2") do |config|
  config.vm.define "manager1" do |manager1|
    manager1.vm.box = "ubuntu/xenial64"
    manager1.vm.network "private_network", ip: "192.168.50.100"
    manager1.vm.provision "shell", path: "scripts/provisioner.sh", privileged: false
  end

  config.vm.define "worker1" do |worker1|
    worker1.vm.box = "ubuntu/xenial64"
    worker1.vm.network "private_network", ip: "192.168.50.101"
    worker1.vm.provision "shell", path: "scripts/provisioner.sh", privileged: false
  end

  config.vm.define "worker2" do |worker2|
    worker2.vm.box = "ubuntu/xenial64"
    worker2.vm.network "private_network", ip: "192.168.50.102"
    worker2.vm.provision "shell", path: "scripts/provisioner.sh", privileged: false
  end


end
