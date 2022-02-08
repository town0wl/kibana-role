Kibana role
=========

Роль для установки, начальной конфигурации и запуска Kibana в виде сервиса на хостах с ОС: Debian, Ubuntu, CentOS, RHEL.

Requirements
------------

Поддерживаются только ОС семейств debian и EL.

Role Variables
--------------

| Variable name | Default | Description |
|-----------------------|----------|-------------------------|
| kibana_version | "7.14.0" | Параметр, который определяет какой версии kibana будет установлен |
| kibana_install_type | remote | При установке значения 'remote' загрузка дистрибутива происходит через управляющий хост ansible |
| elastic_service_ip | Cчитывается из ansible facts хоста с именем ***elastic-host*** | IP-адрес сервиса Elasticsearch |


Example Playbook
----------------

    - hosts: kibana
      roles:
         - { role: kibana-role }

License
-------

BSD
