# -*- mode: ruby -*-
# vi: set ft=ruby :

# This vagrant file is used for testing. It will build an openvpn box for
# experimenting with different configs

Vagrant.configure("2") do |config|
  config.vm.box = "debian/jessie64"
  config.vm.provision :shell, :path => "bootstrap", :args => "test.openvpn.local"

  # Forward local port 8080 to guest port 80
  config.vm.network "forwarded_port", guest: 1194, host: 1194, protocol: 'udp'

  config.vm.hostname = "test-openvpn.openvpn.local"
end
