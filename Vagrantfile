# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  # Название linux бокса
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end

  # Настройки предоставления
  config.vm.provision :shell, :path => "provisioning/provision.sh"

  # Задаем ip адрес в сети
  config.vm.network :private_network, ip: "10.10.10.10"

  # Пробрасываем порты
  config.vm.network "forwarded_port", guest: 80, host: 8888
  config.vm.network "forwarded_port", guest: 5432, host: 8889
  config.vm.network "forwarded_port", guest: 1080, host: 8890
end
