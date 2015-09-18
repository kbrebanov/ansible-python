python
======

[![Ansible Role](https://img.shields.io/ansible/role/3943.svg)](https://galaxy.ansible.com/list#/roles/3943)

Installs Python

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name            | Default                   | Description                    |
|-----------------|---------------------------|--------------------------------|
| python3_version | 3.4.3                     | Version of Python3 to install  |
| python3_enabled | true                      | If Python3 should be installed |
| python2_version | 2.7.10                    | Version of Python2 to install  |
| python2_enabled | false                     | If Python2 should be installed |
| python_defaults | ["{{ python3_version }}"] | List of default Pythons        |

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

Install Python 3 and Python 2
```
- hosts: all
  roles:
    - { role: kbrebanov.python, python2_enabled: true, python_defaults: ["{{ python3_version }}", "2.7.10"] }
```

Install only Python 2
```
- hosts: all
  roles:
    - { role: kbrebanov.python, python3_enabled: false, python2_enabled: true, python_defaults: ['2.7.10'] }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
