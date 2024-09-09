# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "host1" do |host1|
    host1.vm.box = "starboard/ubuntu-arm64-20.04.5"
    host1.vm.box_version = "20221120.20.40.0"
    host1.vm.box_download_insecure = true
    host1.vm.provider "vmware_desktop" do |vm|
        vm.ssh_info_public = true
        vm.gui = true
        vm.linked_clone = false
        vm.vmx["ethernet0.virtualdev"] = "vmxnet3"
        vm.memory = "1024"
        vm.cpus = "2"
    end
  end

  config.vm.define "host2" do |host2|
    host2.vm.box = "starboard/ubuntu-arm64-20.04.5"
    host2.vm.box_version = "20221120.20.40.0"
    host2.vm.box_download_insecure = true
    host2.vm.provider "vmware_desktop" do |vm|
        vm.ssh_info_public = true
        vm.gui = true
        vm.linked_clone = false
        vm.vmx["ethernet0.virtualdev"] = "vmxnet3"
        vm.memory = "1024"
        vm.cpus = "2"
    end
  end
  config.vm.provision "shell", path: "provision.sh"
end