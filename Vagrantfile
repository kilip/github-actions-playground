Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/jammy64"

    config.vm.define 'ubuntu'

    # Prevent SharedFoldersEnableSymlinksCreate errors
    config.vm.synced_folder ".", "/vagrant", disabled: true

    config.vm.define "k8s-0" do |c|
      c.vm.box = "ubuntu/jammy64"
      c.vm.network "public_network", ip: "10.10.10.11"
    end
    config.vm.define "k8s-1" do |c|
      c.vm.box = "ubuntu/jammy64"
      c.vm.network "public_network", ip: "10.10.10.12"
    end
    config.vm.define "k8s-2" do |c|
      c.vm.box = "ubuntu/jammy64"
      c.vm.network "public_network", ip: "10.10.10.11"
    end

end