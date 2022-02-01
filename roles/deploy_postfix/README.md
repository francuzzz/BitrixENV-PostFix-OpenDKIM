
deploy_postfix
=========

Install and configure a mailing system Postfix

Requirements
------------

Installed and running server with BitrixENV

Role Variables
--------------
```
# === Credentials for certificate === #
domain: yourbestdomain.com
passphrase: # Set if you want passphrase
country_name: RU 
state_or_province: RU
locality_name: Moscow
email_address: admin@yourbestdomain.com
organization_name: Test Company LLC
# === Private Key  === #
key_size: 2048
key_type: RSA # Others include DSA, ECC, Ed25519, Ed448, X25519, X448
```


Example Playbook
----------------


```
- name: Install & Config Opendkim
  hosts: bitrix
  become: yes

  roles:
    - deploy_postfix.yml
```
