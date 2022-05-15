FROM ubuntu:latest
RUN apt -qqqqy update ; apt -qqqy dist-upgrade ; \
    apt -qqqy install ansible git vim net-tools iputils-ping && \
    git clone https://github.com/ots-jespinoza/zabbix-ansible.git /zabbix-ansible
RUN ansible-galaxy install -r /zabbix-ansible/requirements.yml && \
    ansible-galaxy collection install -r /zabbix-ansible/requirements.yml

CMD /bin/bash
