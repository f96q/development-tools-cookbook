Vagrant.configure('2') do |config|
  config.vm.box = 'ubuntu/eoan64'
  config.vm.network 'forwarded_port', guest: 3000, host: 3000
  config.vm.provision 'ansible_local' do |ansible|
    ansible.playbook = 'playbook.yml'
  end
  config.vm.provider 'virtualbox' do |vb|
    vb.memory = 8 * 1024
  end
  config.disksize.size = '60GB'
  config.ssh.forward_agent = true
end
