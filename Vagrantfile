Vagrant.configure("2") do |config|
  config.vm.box = "debian/jessie64"
  config.ssh.insert_key = false
  config.vm.provision "shell", inline: <<-SHELL
    echo "Updating system"
    apt-get update
    apt-get dist-upgrade -y
    echo "Installing postgres"
    apt-get install -y postgresql-client-9.4 postgresql-9.4
  SHELL
end