# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.provider 'virtualbox' do |v|
    v.linked_clone = true if Vagrant::VERSION =~ /^1.8/
  end

  config.vm.network "private_network", type: "dhcp"

  config.vm.define 'CentOS_7' do |co7|
    co7.vm.box =  'puppetlabs/centos-7.2-64-nocm'
    co7.vm.hostname = 'centos-7'
    co7.vm.provision 'shell', inline: 'yum install epel-release -y'
  end

  config.vm.define 'CentOS_6' do |co6|
    co6.vm.box = 'puppetlabs/centos-6.6-64-nocm'
    co6.vm.hostname = 'centos-6'
    co6.vm.provision 'shell', inline: 'yum install epel-release -y'
  end

  config.vm.define 'Ubuntu_1404' do |u14|
    u14.vm.box = 'puppetlabs/ubuntu-14.04-64-nocm'
    u14.vm.hostname = 'ubuntu-1404'
    u14.vm.provision 'shell', inline: 'apt-get install software-properties-common -y'
    u14.vm.provision 'shell', inline: 'add-apt-repository "deb http://archive.ubuntu.com/ubuntu $(lsb_release -sc) main universe restricted multiverse"'
    u14.vm.provision 'shell', inline: 'add-apt-repository "deb http://archive.ubuntu.com/ubuntu $(lsb_release -sc)-updates main universe restricted multiverse"'
  end

  config.vm.define 'Ubuntu_1204' do |u12|
    u12.vm.box = 'puppetlabs/ubuntu-12.04-64-nocm'
    u12.vm.hostname = 'ubuntu-1204'
    u12.vm.provision 'shell', inline: 'apt-get install software-properties-common -y'
    u12.vm.provision 'shell', inline: 'apt-get install python-software-properties -y'
    u12.vm.provision 'shell', inline: 'add-apt-repository "deb http://archive.ubuntu.com/ubuntu $(lsb_release -sc) main universe restricted multiverse"'
    u12.vm.provision 'shell', inline: 'add-apt-repository "deb http://archive.ubuntu.com/ubuntu $(lsb_release -sc)-updates main universe restricted multiverse"'
  end

  config.vm.define 'Debian_8' do |d8|
    d8.vm.box = 'puppetlabs/debian-8.2-64-nocm'
    d8.vm.hostname = 'debian-82'
  end

  config.vm.define 'Debian_7' do |d7|
    d7.vm.box = 'puppetlabs/debian-7.8-64-nocm'
    d7.vm.hostname = 'debian-78'
  end
end
