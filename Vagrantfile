Vagrant.configure("2") do |config|
    
    config.vm.define "ansible" do |ansible|
        ansible.vm.box = "centos7"
        ansible.vm.network "public_network", bridge: "network", ip: "192.168.1.50"
        ansible.vm.hostname = "ansible"
        ansible.vm.provider :virtualbox
        ansible.vm.disk :disk, size: "25GB", primary: true


        ansible.vm.provider "virtualbox" do |v|
            v.memory = "1024"
            v.cpus = 2  
            v.name = "ansible_master"
        end

     end

      config.vm.define "host1" do |host1|
        host1.vm.box = "centos7"
        host1.vm.network "public_network", bridge: "network", ip: "192.168.1.51"
        host1.vm.hostname = "host1"
        host1.vm.provider :virtualbox
        host1.vm.disk :disk, size: "20GB", primary: true


        host1.vm.provider "virtualbox" do |v|
            v.memory = "1024"
            v.cpus = 2  
            v.name = "host1"
        end

     end

      config.vm.define "host2" do |host2|
        host2.vm.box = "ubuntu/xenial64"
        host2.vm.network "public_network", bridge: "network", ip: "192.168.1.52"
        host2.vm.hostname = "host2"
        host2.vm.provider :virtualbox
        host2.vm.disk :disk, size: "20GB", primary: true


        host2.vm.provider "virtualbox" do |v|
            v.memory = "1024"
            v.cpus = 2  
            v.name = "host2"
        end

     end


 end