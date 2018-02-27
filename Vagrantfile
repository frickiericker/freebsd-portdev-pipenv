# https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=201904
FREEBSD_BASE_MAC = "080027D14C66"

Vagrant.configure("2") do |config|
  config.vm.box = "freebsd/FreeBSD-11.1-RELEASE"
  config.vm.base_mac = FREEBSD_BASE_MAC
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.ssh.shell = "sh"

  config.vm.provider :virtualbox do |v|
    v.memory = 1024
    v.cpus = 2
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "poudriere.yml"
  end
end
