VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.define "web" do |web|
        web.vm.box = "ubuntu/trusty64"

        web.vm.network "private_network", ip: "192.168.20.10"
        web.vm.network "forwarded_port", guest: 80, host: 8080 # Apache


        web.vm.provider "virtualbox" do |v|
            v.customize ["modifyvm", :id, "--memory", "1024"]
        end

        config.vm.provision :ansible do |ansible|
            ansible.sudo = true
            ansible.verbose = 'vvvv'
            ansible.playbook = "ansible/playbooks/provision.yml"
        end
    end
end
