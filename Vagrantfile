# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false

  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.cpus = 1
    vb.memory = 2048
  end

  config.vm.define "kafka1" do |kafka|
    kafka.vm.hostname = "kafka1"
    kafka.vm.box = "centos/7"
  end

  config.vm.define "kafka2" do |kafka|
    kafka.vm.hostname = "kafka2"
    kafka.vm.box = "centos/7"
  end

  config.vm.define "kafka3" do |kafka|
    kafka.vm.hostname = "kafka3"
    kafka.vm.box = "centos/7"
  end
end
