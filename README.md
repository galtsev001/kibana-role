Kibana role
=========

Роль для установки Kibana

Requirements
------------

Поддреживаются ОС Linux семейств Debian и RHEL.

Role Variables
--------------

| Variable name       | Default  | Description  
|---------------------|----------|-------------------------  
| kibana_version      | "7.14.0" | Параметр, определяющий устанавливаемую версию Kibana  
| kibana_install_type | "remote" | Параметр, определяющий способ получения дистрибутива - удаленно или из локального файла. Возможные значения: "remote", "local"  

Example Playbook
----------------

Example Playbook
----------------

	- hosts: all
	  roles:
		 - { role: kibana-role }

License
-------

MIT
