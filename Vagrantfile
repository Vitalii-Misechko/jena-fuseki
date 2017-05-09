# -*- mode: ruby -*-
# vi: set ft=ruby :

unless Vagrant.has_plugin?("vagrant-docker-compose")
  system("vagrant plugin install vagrant-docker-compose")
  puts "Dependencies installed, please try the command again."
  exit
end

unless Vagrant.has_plugin?("vagrant-vbguest")
  system("vagrant plugin install vagrant-vbguest")
  puts "Dependencies installed, please try the command again."
  exit
end

Vagrant.configure(2) do |config|
  config.vm.box = 'ubuntu/trusty64'
  config.vm.hostname = "JenaHost"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
  end
  config.vm.network :forwarded_port, guest: 3030, host: 3030
  config.vm.provision :docker
  config.vm.provision :docker_compose, yml: "/vagrant/vagrant-docker-compose.yml", rebuild: true, run: "always"
end