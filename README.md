# BitrixENV-PostFix-OpenDKIM
Ansible role for Deploy Postfix OpenDKIM in BitrixENV

# Steps
=======

1. Add the ROLES folder to your Ansible folder.
2. Change the variables in the roles/{{rolename}}/defaults/main.yml
3. Launch playbook-postfx_opendkim.yml
4. Add DNS records in domain management.
=======

After the distribution of DNS records, letters from your server will be signed with a certificate, and all kinds of checks of mail services will also pass.

For example: https://www.mail-tester.com/
