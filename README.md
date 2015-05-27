python
======

Installs Python

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name           | Default | Description                  |
|----------------|---------|------------------------------|
| python_version | 3.4.3   | Version of Python to install |

Dependencies
------------

- kbrebanov.git

Example Playbook
----------------

Install Python 3
```
- hosts: all
  roles:
    - { role: kbrebanov.python }
```

Install Python 2
```
- hosts: all
  roles:
    - { role: kbrebanov.python, python_version: 2.7.10 }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
