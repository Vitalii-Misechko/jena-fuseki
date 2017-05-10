# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.provider "docker" do |docker|
    docker.vagrant_vagrantfile = "host/Vagrantfile"
    docker.image = "stain/jena-fuseki"
    docker.create_args = ['--volume=/fuseki:/fuseki', '-eADMIN_PASSWORD=pw', '--restart=unless-stopped']
    docker.ports = ['3030:3030']
    docker.name = 'jena'
  end
end