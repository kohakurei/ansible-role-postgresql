Ansible role: postgresql
====
Requirements
----
None.

Role variables:
----
user must set variables.
```
postgresql_user_name: "postgres_user"
postgresql_user_password: "postgres_password"
postgresql_db_name: "postgres_db"
```

available variables are listed in defaults. (see `defaults/main.yml`)
```
postgresql_version: "9.3"
postgresql_user_roles: "SUPERUSER[,...]"
postgresql_db_encoding: "UTF8"
postgresql_user_connection:
  - name: "{{ postgresql_user_name }}"
    type: "local"
    database: "all"
```

Example playbook:
----
```
- hosts:
  rolse:
    - { role: postgresql }
```

Testing Ansible version:
---
2.0.1
