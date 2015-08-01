# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.define 'arcade' do |arcade|
        arcade.vm.box = 'ubuntu/trusty64'
        arcade.vm.provider "virtualbox" do |vb|
            vb.gui = true
        end
    end

    config.vm.provision 'ansible', run: 'always' do | ansible |
        ansible.groups = {
        'arcade' => ['arcade']
    }
        ansible.playbook = 'ansible/site.yml'
    end
end
