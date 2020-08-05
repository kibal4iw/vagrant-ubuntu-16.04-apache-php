Vagrant.configure("2") do |config|
    config.vm.box = "damianlewis/ubuntu-16.04-apache-php"
    config.vm.box_version = "1.0.0"

    # Networking
    config.vm.network "private_network", ip: "192.168.3.4"

    # File sharing
    config.vm.synced_folder "./htdocs", "/var/www/html", type: "nfs"

    # Configuration
    config.vm.provider "virtualbox" do |v|
    	v.name = "Dev"
    	v.customize ["modifyvm", :id, "--memory", "1024"]
    end
end