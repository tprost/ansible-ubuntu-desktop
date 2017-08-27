# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = 'boxcutter/ubuntu1610-desktop'
  config.vm.provider 'virtualbox' do |vbox|
    vbox.gui = true
  end

  config.vm.provision 'ansible' do |ansible|
    ENV['ANSIBLE_NOCOWS'] = '1'
    ansible.playbook = 'installation.yml'
    ansible.sudo = true
  end
end
