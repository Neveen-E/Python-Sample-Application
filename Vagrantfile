# Install required plugins

required_plugins = ["vagrant-hostsupdater", "vagrant-berkshelf"]
required_plugins.each do |plugin|
  exec "vagrant plugin install #{plugin}" unless Vagrant.has_plugin? plugin
end

Vagrant.configure("2") do |config|

  config.vm.define "pythonapp" do |pythonapp|
    pythonapp.vm.box = "ubuntu/xenial64"
    pythonapp.vm.network "private_network", ip: "192.168.10.170"
    pythonapp.hostsupdater.aliases = ["development.project"]

    #sync app folder
    pythonapp.vm.synced_folder "app", "/app"

    #provision with chef

  end

end
