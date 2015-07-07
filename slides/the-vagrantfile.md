##  The Vagrantfile

```
Vagrant.configure(2) do |config|
  # Installs the operating system
  config.vm.box           = 'ubuntu/trusty64'

  # Configures the virtual machine
  config.vm.network       'private_network', ip: '192.168.111.10'
  config.vm.synced_folder 'code/', '/home/vagrant/app'

  # Provisions the system
  config.vm.provision     'shell', path: 'provision/bootstrap.sh'
end
```


note:
  Three main things: Install OS, configure VM, provision system
