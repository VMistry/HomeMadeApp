# required_plugins = ["vagrant-hostsupdater", "vagrant-berkshelf"]
# required_plugins.each do |plugin|
#   unless Vagrant.has_plugin? plugin
#     puts "Installing vagrant plugin #{plugin}"
#     Vagrant::Plugin::Manager.instance.install_plugin(plugin)
#     puts "Installed vagrant plugin #{plugin}"
#   end
# end

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network("private_network", ip: "192.168.11.101")
  # config.hostsupdater.aliases = ["nodeapp.local"]
  config.vm.synced_folder "../", "/home/ubuntu/GamePage"
  config.vm.provision "shell", path: "environment/provision.sh", privileged: false
end
