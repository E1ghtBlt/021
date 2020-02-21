
Vagrant.configure("2") do |config|
    config.vm.define "centos" do |centos|
    centos.vm.box ="centos/7"
    end
    config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.box = "ubuntu/bionic64"
    ubuntu.vm.provision "shell",
    inline:
    "apt-get update
    apt-get install -y apache2"
    ubuntu.vm.netvork "forwarded_port" , guest:80 , host: 8080
    end


end
