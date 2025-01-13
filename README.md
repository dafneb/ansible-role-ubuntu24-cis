CIS Ubuntu Linux Benchmark
==========================

This role is designed as application of hardening and security rules to Ubuntu 24.

This role also implements settings and tasks from those roles:

* dafneb.ubuntu24-sa-server-init
* dafneb.ubuntu24-aide
* dafneb.ubuntu24-apparmor

Actual version is following: CIS Ubuntu Linux 24.04 LTS Benchmark v1.0.0 - 08-26-2024

Requirements
------------

No special requirements. Some tasks require "privileged role" at system. So, use [become](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_privilege_escalation.html#using-become) option at your inventory list.

Role Variables
--------------

This role is designed so the end user should not have to edit the tasks themselves. All customizing should be done via the defaults/main.yml file or with extra vars within the project, job, workflow, etc.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: dafneb.ubuntu24-cis }

License
-------

MIT

