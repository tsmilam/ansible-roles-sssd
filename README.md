Role Name
=========

sssd - install and configure system security services daemon

Requirements
------------

sssd.conf template assumes Active Directory is in use. This role uses 'realm' commands and is only tested on Enterprise Linux 7.

Role Variables
--------------
sssd/vars/main.yml
sssd_realm: domain.example.org
sssd_dc: dc01.example.org

Dependencies
------------

No dependencies defined, but don't forget to set up NTP and make sure DNS works.

Example Playbook
----------------

- hosts: foo 
  gather_facts: yes
  connection: ssh
  remote_user: bar 
  become: yes
  become_method: sudo
  vars_prompt:
   - name: "name"
     prompt: "What is your username?"
     private: no
   - name: "your_password"
     prompt: "Enter password"
     private: yes
  roles:
   - sssd 


License
-------

BSD

Author Information
------------------

Tyler Milam
