# devops_vagrantfile
Create a development environment on your local machine using Vagrant in VirtualBox. This description applies to Vagrantfile.

## Table of variable
| variable        | must be used | example                                                                                                                                            |
| --------------- | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| :box            | yes          | :box => [ {:box_url => "https://alpha.release.flatcar-linux.net/amd64-usr/current/flatcar_production_vagrant.box", :box_local_file_name => "flatcar_production_vagrant.box", :box_name => "flatcar-alpha"} ]                                                                                                                     |
| :vm_name        | yes          | :vm_name => "admin.mycorp.org"                                                                                                                     |
| :hostname       | yes          | :hostname => "test19-server"                                                                                                                       |
| :network        | yes          | :network => [ { :network_type => "public_network", :bridge_type => "wlp0s20f3" }, { :network_type => "private_network", :ip => "192.168.56.11" } ] |
| :ssh            | no           | :ssh => [ { vm_username, :ssh_key_path => "files", :ssh_key_name => "id_rsa", :key_type => "rsa", :bit => 4096} ]                                  |
| :port           | no           | :port => [ { :guest => "80", :host => "8888" } ]                                                                                                   |
| :disk           | no           | :disks => [ { :disk_size => 10, :disk_type => "Standard"} ]                                                                                        |
| :resource_limit | no           | :resource_limit => [ {:cpu => 1, :memory => 512} ]                                                                                                 |
| :sync           | no           | :sync => [ { :src => ".", :dst => "/home/vagrant/vagrant" } ]                                                                                      |
| :file           | no           | :file => [ { :src => "files/id_rsa", :dst => "/home/vagrant/.ssh/id_rsa" } ]                                                                       |
| :sript          | no           | :script => "install.sh"                                                                                                                            |
| :shell          | no           | :shell => provision_ansible                                                                                                                        |
| :ansible        | no           | :ansible => [ { :group => "client"} ]                                                                                                              |
