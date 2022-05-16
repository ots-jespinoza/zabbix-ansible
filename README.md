# zabbix-ansible-poc

Zabbix ansible PoC playbook.

## NOTE:

**Before you begin**, make sure to modify the *hosts*, *ansible.cfg*, and *group_vars/all* files to reflect your environment.

## Quickstart:

The included Dockerfile has everything you'll need, simply build, run, modify required config files and apply to your target infrastructure -- EG: *docker build -t zabbix-ansible-poc docker_image && docker run -it zabbix-ansible-poc bash*.

## Known bugs:

The *zabbix_web* role used from the *community.zabbix* ansible-galaxy collection will error out when trying to apply RedHat repo on nodes running Ubuntu. To get around this you can modify the roles *main./task.yml* removing the RedHat stanza found at line 54-58.
