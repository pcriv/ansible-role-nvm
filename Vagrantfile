Vagrant.configure('2') do |config|
  config.vm.define 'pablocrivella' do |c|
    c.vm.box = 'ubuntu/trusty64'
    c.vm.network :private_network, ip: '192.168.40.2'
    c.vm.hostname = 'pablocrivella.local'
    c.vm.provision 'ansible' do |ansible|
      ansible.playbook = 'test.yml'
      ansible.sudo = true
      ansible.inventory_path = 'vagrant-inventory'
      ansible.host_key_checking = false
    end
  end
end
