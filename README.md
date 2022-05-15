# zabbix-ansible

Zabbix ansible playbook.

## NOTE:

**Before you begin**, make sure to modify the *hosts*, *ansible.cfg*, and *group_vars/all* files to reflect your environment.

## Known bugs:

The *zabbix_web* role used from the *community.zabbix* ansible-galaxy collection will error out when trying to apply RedHat repo on a noed running Ubuntu. To get around this you can modify the roles *main./task.yml* removing the RedHat stanza found at line 54-58.
