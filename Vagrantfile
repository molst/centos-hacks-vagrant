# -*- mode: ruby -*-
# vi: set ft=ruby :
ENV['DEFAULT_VAGRANT_PROVIDER'] = 'virtualbox'

Vagrant.configure(2) do |config|
  config.vm.box = "puphpet/centos65-x64"
  config.vm.synced_folder "/Users/molst/dev", "/home/vagrant/dev" 
  config.vm.provision "shell", inline: <<-SHELL
    yum install git rpm-build ruby rubygems ruby-devel gcc libxml2 rubygem-nokogiri zlib-devel libxslt-devel libxslt pcre.x86_64 pcre-devel.x86_64 openssl-devel.x86_64 gcc-c++ autoconf automake -y
    gem install bundler fpm fpm-cookery
  SHELL
end
