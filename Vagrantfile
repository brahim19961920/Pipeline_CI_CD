Vagrant.configure("2") do |configuration|
  configuration.vm.define "MachineDev" do |config|
    config.vm.box = "ubuntu/xenial64"
    config.vm.hostname = "machineDeveloppement"
    config.vm.network :private_network, ip: "192.168.33.10"
    config.vm.provider "virtualbox" do |vb|
		vb.memory = "2048"
	end
    end
end
