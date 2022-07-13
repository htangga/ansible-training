# Vault Command

ansible-vault `option` `file.yml`

# most useful options:
- encrypt
- decrypt
- view


# Examples

For Example, if we want to encrypt inventories/staging/host_vars/host1.yml:
```
ansible-vault encrypt inventories/staging/host_vars/host1.yml
```
and then prompt your password


For Example, if we want to decrypt inventories/staging/host_vars/host1.yml:
```
ansible-vault decrypt inventories/staging/host_vars/host1.yml
```
and then prompt your password


For Example, if we want to view inventories/staging/host1.yml:
```
ansible-vault view inventories/staging/host_vars/host1.yml
```
and then prompt your password


For Example, if we want to run our playbook with encrypted inventories/staging/host_vars/host1.yml then we should use this command:
```
ansible-playbook -i inventories/staging/hosts webserver.yml --ask-vault-pass
```
and then prompt your password