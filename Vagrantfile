# Install required plugins

# required_plugins = ["vagrant-hostsupdater", "vagrant-berkshelf"]
# required_plugins.each do |plugin|
#   exec "vagrant plugin install #{plugin}" unless Vagrant.has_plugin? plugin
# end

Vagrant.configure("2") do |config|

  config.vm.define "app" do |app|
    app.vm.box = "ubuntu/xenial64"
    app.vm.network "private_network", ip: "192.168.10.170"
    app.hostsupdater.aliases = ["development.project"]

    #sync app folder
    app.vm.synced_folder "app", "/app"

    #provision with chef
    app.vm.provision "chef_solo" do |chef|
      chef.add_recipe "pythonapp::pythonapp"
      chef.add_recipe "nginx::nginx"
    end

  end

end
