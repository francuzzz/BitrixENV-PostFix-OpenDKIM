![BitrixENV logo](https://79410.selcdn.ru/data.mcart.ru/main/51a/51a9bd78e6e4b1c90c80896353172120/sh.png)

# BitrixENV-PostFix-OpenDKIM
Ansible role for Deploy Postfix OpenDKIM in BitrixENV

# Steps

1. Add the ROLES folder to your Ansible folder.
2. Change the variables in the roles/{{rolename}}/defaults/main.yml
3. Launch playbook-postfx_opendkim.yml
4. Add DNS records in domain management.

# DNS Records

### SPF
mail2.yourbestdomain.com. IN TXT "v=spf1 +a +mx +ip4:{{Your mail server IP adress}} ~all"								 
										 
### DKIM
yn._domainkey.yourbestdomain.com. IN TXT v=DKIM1; g=*; k=rsa; p=MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQC/c8fae+aGslyE2ewDBcy6sXf4yHTCaK6Sx+t9CSUiXF2jNL1SzE1pU14yte9Pa1V5bsXEqLNkdFJyr6QClHC8gQvQwHY4AyBjEj2JWAlHLZ0S1KFWZeuauBYGtGc/2G9MJWti3KsxiESeCvZp3DGYDPVdGeNVOmws/mmsuy3DjwIDAQAB\

### DMARC
_dmarc.yourbestdomain.com.    IN TXT "v=DMARC1; p=quarantine; pct=5;"


# Test it

After the propogation of DNS records, letters from your server will be signed with a certificate, and all kinds of checks of mail services will also pass.

For example: https://www.mail-tester.com/
