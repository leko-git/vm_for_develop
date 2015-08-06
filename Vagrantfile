# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  # Название linux бокса
  config.vm.box = "ubuntu/trusty64"

  # Настройки предоставления
  config.vm.provision :shell, :path => "provisioning/provision.sh"
  
  # Задаем ip адрес в сети
  config.vm.network :private_network, ip: "10.10.10.10"
end
