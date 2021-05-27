repmgr-cluster
=========

This repository is to manage and configure RepMgr Cluster on RHEL Postgres Server.


[Roles](#Roles)
========
* haproxy
* postgres_repmgr
* ssh_setup



[Playbooks](#Playbooks)
==========

### repmgr_install.yml
    This is the main playbook which will install and configure RepMgr Cluster in Postgres DB.

### repmgr_upgrade.yml
    This playbook is used to updgrade RepMgr CLuster. 

### playbooks/postgresql_enable_ssh.yml
    This playbook will enable passwordless ssh connnectivity from master to replica servers and vice versa for postgres user.

### playbooks/postgresql_disable_ssh.yml
    This playbook will disable passwordless ssh connnectivity from master to replica servers and vice versa for postgres user.

### awx-health-check.yml
    This playbook will perform health check status on pre-determined services, api end-poits, and look for errors in the logs.

### repmgr-determine-primary-ha-script.yml
    This playbook will provide primary database server in cluster.

### repmgr-failover.yml
    This playbook will failover to another server in cluster
    
### repmgr-fix-failed.yml 
    This playbook will fix failed DB server in cluster
    
### repmgr-fix-splitbrain.yml 
    This playbook will fix splitbrain in DB server in cluster
    
### repmgr-clone.yml 
    This playbook will create clone from master to stansby DB server in cluster
    
### repmgr-fix-splitbrain.yml 
    This playbook will fix splitbrain in DB server in cluster
    
### repmgr-database-status.yml 
    This playbook will give Database services and confiuration status in cluster
    
### repmgr-master-configuration.yml 
    This playbook will give Master confiuration status in cluster    
    
    
[Database recovery from backups](#Database-recovery-from-backups)
================================
