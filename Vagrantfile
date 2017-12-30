# vagrant plugin install vagrant-vultr dotenv
Dotenv.load

Vagrant.configure("2") do |config|
  config.vm.provider :vultr do |vultr, override|
    vultr.region = ENV["VULTR_REGION"]
    vultr.plan = ENV["VULTR_PLAN"]
    vultr.os = ENV["VULTR_OS"]
    vultr.token = ENV["VULTR_TOKEN"]
    override.ssh.private_key_path = ENV["VULTR_SSH_KEY"]
    override.vm.box = "vultr"
    override.vm.box_url = "https://github.com/p0deje/vagrant-vultr/raw/master/box/vultr.box"
  end

  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.ssh.shell = "sh"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "poudriere.yml"
  end
end
