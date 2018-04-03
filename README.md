PostgreSQL
==========

A brief description of the role goes here.

Requirements
------------
System must be registered on Satellite
Operating System (RHEL 7.4)
Software Components used by the application (Data Base “PostgreSQL”)
Database File System Mount Point: /var/lib/pgsql  & SIZE = 500GB LVM
Physical IPs: Master(IP) and Slave(IP)  and
Virtual IP( VIP) 

Role Variables
--------------

 cf_wal_level: 
 cf_synchronous_commit:              # synchronization level;
 cf_archive_mode: 
 cf_max_wal_senders: 
 cf_wal_keep_segments:          # in logfile segments, 16MB each; 0 disables
 cf_hot_standby: 
 master_ip: Master Server IP
 slave_ip: Slave Server IP
 vip: # virtual IP


Dependencies
------------

pacemaker 
resource-agents
resource-agents-paf
pcs
corosync

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { postgresql_ha: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

Rodney Moila
Email: rodneymoila@gmail.com

