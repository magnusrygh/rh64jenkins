Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"
  config.vm.network "forwarded_port", guest: 8080, host: 5858
  config.vm.provision "ansible" do |ansible|
      ansible.playbook="ansible/playbook.yml"
      ansible.sudo = true
  end
  config.vm.post_up_message = "Use http://127.0.0.1:5858 to run war from /home/vagrant/sync"
end
