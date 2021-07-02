Vagrant.configure("2") do |config|

   config.vm.define "server1" do |server1|
     server1.vm.box = "bento/centos-7.2"
     server1.vm.hostname = "server1"
     server1.vm.network "private_network", type: "dhcp"

 
     config.vm.provider "virtualbox" do |vb|
       vb.memory = 40000
       vb.cpus = 8
     end
   end
 
   config.vm.define "server2" do |server2|
     server2.vm.box = "bento/centos-7.2"
     server2.vm.hostname = "server2"
     server2.vm.network "private_network", type: "dhcp"
 
     config.vm.provider "virtualbox" do |vb|
       vb.memory = 40000
       vb.cpus = 8
     end
   end
 
   config.vm.provision "ansible" do |ansible|
     ansible.playbook = "playbook.yml"
   end
 
end
