Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-8.3"

  config.vm.define :test do | test |
    test.vm.hostname = "test"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
  end

  config.vm.synced_folder ".", "/vagrant", disabled: true
end
