Vagrant.configure("2") do |config|

  # Ubuntu Jammy 22.04
  config.vm.box = "ubuntu/jammy64"

  # Shared folder
  config.vm.synced_folder "F:/AFMS", "/vagrant"

  # -------------------------
  # DEV
  # -------------------------
  config.vm.define "dev" do |dev|
    dev.vm.hostname = "dev"

    dev.vm.network "private_network",
     ip: "192.168.56.10"

    dev.vm.provider "virtualbox" do |vb|
      vb.name = "AFMS-DEV"
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  # -------------------------
  # QA
  # -------------------------
  config.vm.define "qa" do |qa|
    qa.vm.hostname = "qa"

    qa.vm.network "private_network",
     ip: "192.168.56.11"

    qa.vm.provider "virtualbox" do |vb|
      vb.name = "AFMS-QA"
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  # -------------------------
  # PROD
  # -------------------------
  config.vm.define "prod" do |prod|
    prod.vm.hostname = "prod"

    prod.vm.network "private_network",
     ip: "192.168.56.12"
    prod.vm.provider "virtualbox" do |vb|
      vb.name = "AFMS-PROD"
      vb.memory = 2048
      vb.cpus = 2
    end
  end

end
