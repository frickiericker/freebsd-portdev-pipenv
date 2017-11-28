Vagrant.configure("2") do |config|
  config.vm.guest = :freebsd
  config.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true
  config.vm.box = "freebsd/FreeBSD-11.1-STABLE"
  config.ssh.shell = "sh"
  config.vm.base_mac = "080027D14C66"
end
