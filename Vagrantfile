# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false

  config.vm.define "zookeeper1" do |zookeeper|
    zookeeper.vm.hostname = "zookeeper1"
    zookeeper.vm.box = "centos/7"
    zookeeper.vm.network :private_network, ip: "192.168.0.2"
    zookeeper.vm.network :forwarded_port, guest: 22, host: 2202, id: "ssh"
    zookeeper.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.cpus = 1
      vb.memory = 2048
    end
  end

  config.vm.define "kafka1" do |kafka|
    kafka.vm.hostname = "kafka1"
    kafka.vm.box = "centos/7"
    kafka.vm.network :private_network, ip: "192.168.0.3"
    kafka.vm.network :forwarded_port, guest: 22, host: 2203, id: "ssh"
    kafka.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.cpus = 1
      vb.memory = 2048
    end
  end

  config.vm.define "kafka-connect1" do |kafka_connect|
    kafka_connect.vm.hostname = "kafka-connect1"
    kafka_connect.vm.box = "centos/7"
    kafka_connect.vm.network :private_network, ip: "192.168.0.4"
    kafka_connect.vm.network :forwarded_port, guest: 22, host: 2204, id: "ssh"
    kafka_connect.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.cpus = 1
      vb.memory = 2048
    end
  end
end
