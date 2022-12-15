
## 1. spin up new OS.

    cd /Users/duyhanhnguyen/git/oracle/hanh/vagrant_ansible/vagrant/spin_new_os
  
    vagrant up
  
to provision server (execute script after spin server)
  
    vagrant provision

## 2. Setup Oracle

    cd oracle_si_fs
    vagrant up 
    
    cd ~/git/oracle/hanh/vagrant_ansible/vagrant/oracle_si_fs
    setup Oracle
         ansible-playbook linux_oracle.yml -e hostgroup=myhostgroup -i inventory.yaml
         includes 3 roles:
            roles:
               - linuxfororacle_prep. -> prepare oracle installation
               - setup -> Install Oracle software 
               - oraswdb-install -> Create DB and listener, tnsnames
    
    
## 3. Setup OGG

    cd ogg
    vagrant up 
  
