Vagrant.configure("2") do |config|

  config.vm.define "web01" do |web01|
    web01.vm.box = "ubuntu/jammy64"
    web01.ssh.insert_key = false
	  web01.vm.network "private_network", ip: "192.168.*.*"
    web01.vm.network "forwarded_port", guest: 80, host: 8080
    web01.vm.hostname = "Jenkins"
    web01.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = "2"
    end
    web01.vm.provider :virtualbox do |vb|
      vb.gui = true
    end
  end



  config.vm.define "web02" do |web02|
    web02.vm.box = "ubuntu/jammy64"
    web02.ssh.insert_key = false
	  web02.vm.network "private_network", ip: "192.168.*.*"
    web02.vm.network "forwarded_port", guest: 9000, host: 9000
    web02.vm.hostname = "Sonarqube"
    web02.vm.provider "virtualbox" do |vb|
      vb.memory = "4096"
      vb.cpus = "2"
    end
    web02.vm.provider :virtualbox do |vb|
      vb.gui = true
    end
  end



  config.vm.define "web03" do |web03|
    web03.vm.box = "ubuntu/jammy64"
    web02.ssh.insert_key = false
    web03.vm.network "private_network", ip: "192.168.*.*"
    web03.vm.hostname = "Docker"
    web03.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = "2"
    end
    web03.vm.provider :virtualbox do |vb|
      vb.gui = true
    end
  end
end