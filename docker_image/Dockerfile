FROM ubuntu:latest
ARG DEBIAN_FRONTEND=noninteractive
RUN apt -qqqqy update ; apt -qqqy dist-upgrade ; \
    apt -qqqy install ansible git vim vim-editorconfig net-tools iputils-ping && \
    git clone https://github.com/ots-jespinoza/zabbix-ansible.git /zabbix-ansible
RUN ansible-galaxy install -r /zabbix-ansible/requirements.yml && \
    ansible-galaxy collection install -r /zabbix-ansible/requirements.yml
RUN sed -i 's/{{ ansible_os_family }}.yml/Debian.yml/g' /root/.ansible/collections/ansible_collections/community/zabbix/roles/zabbix_web/tasks/main.yml  && \
    sed -i '54,58d' /root/.ansible/collections/ansible_collections/community/zabbix/roles/zabbix_web/tasks/main.yml

CMD /bin/bash
