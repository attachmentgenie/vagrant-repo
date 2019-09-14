#  vagrant-repo

vagrant starter kit 

## Requirements
    Virtualbox                        => https://www.virtualbox.org
    Vagrant                           => http://www.vagrantup.com
    vagrant-hostmanager               => vagrant plugin install vagrant-hostmanager
    vagrant-cachier  (optional)       => vagrant plugin install vagrant-cachier
    vagrant-puppet-install (optional) => vagrant plugin install vagrant-puppet-install
    vagrant-triggers (optional)       => vagrant plugin install vagrant-triggers
    
## Preparation
    git submodule update --init
    
## Setup
    vagrant up

## Inspec tests

    bundle exec rake
    bundle exec rake inspec[proxy] 

## TLDR
    
    - name: aptly
      public_vhosts:
        - http://aptly.repo.vagrant
    - name: nexus
      public_vhosts:
        - http://nexus.repo.vagrant