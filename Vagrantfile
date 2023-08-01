# vim: set ft=ruby:
# frozen_string_literal: true

Vagrant.configure('2') do |config|
  config.disksize.size = '40GB'
  config.vm.box = 'generic/freebsd13'
  # config.vm.box = 'freebsd/FreeBSD-13.2-RELEASE'
  config.vm.define 'poudriere'

  config.vm.provision 'shell', path: 'bootstrap'

  config.vm.provider :libvirt do |v|
    v.cpus = 4
    v.memory = 4096
  end

  config.vm.synced_folder '.', '/vagrant', disabled: true
end
