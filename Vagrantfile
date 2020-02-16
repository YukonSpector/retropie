HOSTNAME = "retropie"
DOMAIN=".local"
PRIVATE_IP="192.168.33.10"
BOX="debian/stretch64"
RAM = "8192"
CPU_COUNT = "2"
CPU_CAP = "50"
PLAYBOOK = "ansible.yaml"
GUI = "true"

Vagrant.configure("2") do |config|
  config.vm.box = BOX
  config.vm.hostname = HOSTNAME + DOMAIN
  config.vm.box_check_update = false
  # config.vbguest.auto_update = false
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "private_network", ip: PRIVATE_IP
  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", RAM]
    vb.customize ["modifyvm", :id, "--cpus", CPU_COUNT]
    vb.customize ["modifyvm", :id, "--usbohci", "on"]
    vb.customize ["modifyvm", :id, "--usbehci", "on"]
    vb.customize ["modifyvm", :id, "--usbxhci", "on"]
    vb.customize ["modifyvm", :id, "--graphicscontroller", "vmsvga"]
    vb.customize ["modifyvm", :id, "--vram", 32]
    # vb.customize ["modifyvm", :id, "--cpuexecutioncap", CPU_CAP]
    vb.gui = GUI
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = PLAYBOOK
  end
end
