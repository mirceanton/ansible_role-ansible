Ansible Role: Ansible
=====================

An Ansible role that installs... well... Ansible... (as well as commonly used packages)

Requirements
------------

N/A

Role Variables
--------------

|          Variable          |     Type     | Default  |                Description                 |
| :------------------------: | :----------: | :------: | :----------------------------------------: |
|   `ansible_lint_install`   |     bool     |  `true`  |   Whether or not to install ansible-lint   |
| `ansible_molecule_install` |     bool     |  `true`  |     Whether or not to install molecule     |
| `ansible_molecule_driver`  |    string    | `docker` |  Which driver(s) to install for molecule   |
|  `ansible_apt_additional`  | list(string) |   `[]`   | List of additional apt packages to install |
|  `ansible_pip_additional`  | list(string) |   `[]`   | List of additional pip packages to install |

To check which packages are installed by default, take a look in the [defaults](defaults/main.yml) file.

Dependencies
------------

N/A

Example Playbook
----------------

``` yml
---
- hosts: all
  remote_user: root

  roles:
    - role: mirceanton.ansible
      vars:
        ansible_pip_additional: [ lxml, docker, jsondiff ]
        ansible_lint_install: false
        ansible_molecule_install: false
```

License
-------

MIT

Author Information
------------------

A role developed by [Mircea-Pavel ANTON](https://www.mirceanton.com).
