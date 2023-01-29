# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false

  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.cpus = 1
    vb.memory = 2048
  end

  config.vm.define "zookeeper1" do |kafka|
    kafka.vm.hostname = "zookeeper1"
    kafka.vm.box = "centos/7"
    kafka.vm.network "private_network", ip: "192.168.0.2"
  end

  config.vm.define "kafka1" do |kafka|
    kafka.vm.hostname = "kafka1"
    kafka.vm.box = "centos/7"
    kafka.vm.network "private_network", ip: "192.168.0.3"
  end

  config.vm.define "kafka-connect1" do |kafka|
    kafka.vm.hostname = "kafka-connect1"
    kafka.vm.box = "centos/7"
    kafka.vm.network "private_network", ip: "192.168.0.4"
  end
end
