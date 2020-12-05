
minimal_centos
=========

* An Ansible role that checks and removes unneeded packages from an already minimal CentOS install

Requirements
------------

* CentOS Linux 7 - Minimal Installation

Role Variables
--------------

* N/A

Dependencies
------------

* N/A

Example Playbook
----------------

```yaml
---
# playbook for the minimal-centos role.
- hosts: all
  vars_files:
    - become-secret
  become: true
  roles:
    - minimal_centos
```
License
-------

* MIT

Author Information
------------------

* https://github.com/hubvu
