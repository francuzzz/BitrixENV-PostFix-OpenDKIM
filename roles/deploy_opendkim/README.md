
deploy_opendkim
=========

Deploy Domain Keys Identified Mail on Bitrix ENV server 

Requirements
------------

Installed and configured Postfix

Role Variables
--------------

postfix_dir: /etc/postfix 
domain: yourbestdomain.com
short_domain: yn  # first and last letter of the domain name. For example: YourbestdomaiN
dns_folder: /home/user/ansible/dns


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- name: Install & Config Opendkim
  hosts: bitrix
  become: yes

  roles:
    - deploy_opendkim.yml


