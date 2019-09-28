#  vagrant-repo

A vagrant setup that create artifact stores.

## Requirements
    Virtualbox                  => https://www.virtualbox.org
    Vagrant                     => http://www.vagrantup.com
    vagrant-hostmanager         => vagrant plugin install vagrant-hostmanager
    vagrant-puppet-install      => vagrant plugin install vagrant-puppet-install
    vagrant-cachier  (optional) => vagrant plugin install vagrant-cachier
    
## Preparation

    git submodule update --init
    bundle install
    
## Setup

    vagrant up

## Inspec tests

    bundle exec rake
    bundle exec rake inspec[centos7] 

## TLDR

### (G)UI interfaces

    
    - name: aptly
      public_vhosts:
        - http://aptly.repo.vagrant
    - name: nexus
      public_vhosts:
        - http://nexus.repo.vagrant
