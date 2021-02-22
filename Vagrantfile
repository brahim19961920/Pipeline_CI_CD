



$script_inject_pk =<<-'SCRIPT'
#ls /vagrant
cat /vagrant/id_rsa.pub >> /home/vagrant/.ssh/authorized_keys
SCRIPT

Vagrant.configure("2") do |configuration|

  configuration.vm.define "MachineAnsible" do |config|
    
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "machineAnsible"
    config.vm.network :private_network, ip: "192.168.33.10"
    config.vm.provider "virtualbox" do |vb|
		vb.memory = "2048"
	end 
    config.vm.provision "file", source: "./id_rsa", destination: "/home/vagrant/.ssh/"
    end

  configuration.vm.define "MachineDev" do |config|

    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "machineDeveloppement"
    config.vm.network :private_network, ip: "192.168.33.20"
    config.vm.provider "virtualbox" do |vb|
		vb.memory = "2048"
	end
    config.vm.provision "shell", inline: $script_inject_pk
    end

  configuration.vm.define "MachineJenkins" do |config|
    
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "machineJenkins"
    config.vm.network :private_network, ip: "192.168.33.30"
    config.vm.provider "virtualbox" do |vb|
		vb.memory = "6000"
	end
    config.vm.provision "shell", inline: $script_inject_pk
    end

  configuration.vm.define "MachineTomcat" do |config|
    
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "machineTomcat"
    config.vm.network :private_network, ip: "192.168.33.40"
    config.vm.provider "virtualbox" do |vb|
		vb.memory = "4000"
	end
    config.vm.provision "shell", inline: $script_inject_pk
    end



  configuration.vm.define "MachinePreProd" do |config|

    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "machinePreProd"
    config.vm.network :private_network, ip: "192.168.33.50"
    config.vm.provider "virtualbox" do |vb|
                vb.memory = "2048"
        end
    config.vm.provision "shell", inline: $script_inject_pk
    end

  configuration.vm.define "MachineMonitoring" do |config|

    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "machineMonitoring"
    config.vm.network :private_network, ip: "192.168.33.60"
    config.vm.provider "virtualbox" do |vb|
                vb.memory = "6000"
        end
    config.vm.provision "shell", inline: $script_inject_pk
    end






end
