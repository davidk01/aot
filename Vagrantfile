# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.define "packager" do |p|

    p.vm.box = "bento/ubuntu-14.04"
    # p.vm.network "forwarded_port", guest: 8080, host: 8080
    # p.vm.synced_folder "../", "/code"
    # p.vm.network "public_network"

    p.vm.provider "virtualbox" do |vb|
      vb.memory = 1024 * 8
      vb.cpus = 4
    end

    p.vm.provider "vmware_fusion" do |v|
      v.vmx["memsize"] = 1024 * 8
      v.vmx["numvcpus"] = 4
    end

    p.vm.provision :shell do |s|
      s.path = 'bin/vagrant-provisioner.sh'
      s.args = []
    end

  end

end
