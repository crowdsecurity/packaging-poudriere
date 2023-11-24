# vim: set ft=ruby:
# frozen_string_literal: true

Vagrant.configure('2') do |config|
  config.disksize.size = '60GB'
  config.vm.box = 'generic/freebsd14'
  # config.vm.box = 'freebsd/FreeBSD-13.2-RELEASE'
  # config.vm.box = 'freebsd/FreeBSD-14.0-RELEASE'
  config.vm.define 'poudriere'

  config.vm.provision 'shell', path: 'bootstrap'
#  config.vm.provision 'shell', path: 'bootstrap-freebsd'
#  config.vm.provision 'shell', path: 'bootstrap-pfsense'
#  config.vm.provision 'shell', path: 'bootstrap-opnsense'

  config.vm.provider :libvirt do |v|
    v.cpus = 4
    v.memory = 4096
  end

  config.vm.synced_folder '.', '/vagrant', disabled: true
end
