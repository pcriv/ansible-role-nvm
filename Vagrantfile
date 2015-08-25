Vagrant.configure('2') do |config|
  config.vm.define 'ansible-role-nvm' do |c|
    c.vm.box = 'ubuntu/trusty64'
    c.vm.network :private_network, ip: '192.168.40.2'
    c.vm.hostname = 'ansible-role-nvm.local'

    c.vm.provider :virtualbox do |vb|
      vb.name = 'ansible-role-nvm'
    end

    c.vm.provision :ansible do |ansible|
      ansible.playbook = 'test.yml'
      ansible.sudo = true
      ansible.inventory_path = 'vagrant-inventory'
      ansible.host_key_checking = false
      ansible.verbose = 'vvv'
      ansible.extra_vars = {
        nvm_env: ENV['NVM_ENV'],
        nvm_users: ['vagrant']
      }
    end
  end
end
