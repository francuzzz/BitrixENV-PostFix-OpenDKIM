
deploy_opendkim
=========

Deploy Domain Keys Identified Mail on Bitrix ENV server 

Requirements
------------

Installed and configured Postfix

Role Variables
--------------
```
postfix_dir: /etc/postfix 
domain: yourbestdomain.com
short_domain: yn  # first and last letter of the domain name. For example: YourbestdomaiN
dns_folder: /home/user/ansible/dns # For example. Add your path to the folder where the file with DNS record will be saved.
```

Example Playbook
----------------

```
- name: Install & Config Opendkim
  hosts: bitrix
  become: yes

  roles:
    - deploy_opendkim.yml
```

