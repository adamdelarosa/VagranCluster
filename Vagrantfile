# -*- mode: ruby -*-
# vi: set ft=ruby :
 # By Adam Delarosa gojiradam@gmail.com
$script = <<SCRIPT

#nothing here
cd /
wget "https://releases.hashicorp.com/consul/0.5.2/consul_0.5.2_linux_amd64.zip"
SCRIPT

#Vagrant 

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision "shell", inline: $script



config.vm.define "node1" do |node1|
    node1.vm.hostname = "node01"
    node1.vm.box = "ubuntu/trusty64"
    #node1.vm.network "private_network", ip: "192.168.100.206"
config.vm.provision "chef_solo" do |chef|
     chef.cookbooks_path = "cookbooks"
    end
end

# config.vm.define "node2" do |node2|
#    node2.vm.hostname = "node02"
#    node2.vm.box = "ubuntu/trusty64"
#    node2.vm.network "private_network", ip: "192.168.100.207"
# config.vm.provision "chef_solo" do |chef|
#     chef.cookbooks_path = "cookbooks"
#     chef.add_recipe "consul"
#    end
# end

# config.vm.define "node3" do |node3|
#    node3.vm.hostname = "node03"
#    node3.vm.box = "ubuntu/trusty64"
#    node3.vm.network "private_network", ip: "192.168.100.208"
# config.vm.provision "chef_solo" do |chef|
#     chef.cookbooks_path = "cookbooks"
#     chef.add_recipe "consul"
#    end
# end

end
