# CIS Ubuntu 24 (noble) Linux Benchmark

[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](https://github.com/dafneb/.github/blob/main/.github/CODE_OF_CONDUCT.md)
[![License](https://img.shields.io/badge/License-MIT-4baaaa.svg)](https://github.com/dafneb/.github/blob/main/LICENSE)
![GitHub Release](https://img.shields.io/github/v/release/dafneb/ansible-role-ubuntu24-cis)
![GitHub commit activity](https://img.shields.io/github/commit-activity/w/dafneb/ansible-role-ubuntu24-cis)
![GitHub contributors](https://img.shields.io/github/contributors/dafneb/ansible-role-ubuntu24-cis)

![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/dafneb/ansible-role-ubuntu24-cis/ansible-lint.yml?label=ansible-lint)

This role is designed as application of hardening and security rules to Ubuntu 24.

This role also implements settings and tasks from those roles:

- dafneb.ubuntu24-sa-server-init
- dafneb.ubuntu24-aide
- dafneb.ubuntu24-apparmor

Actual version is following: CIS Ubuntu Linux 24.04 LTS Benchmark v1.0.0 - 08-26-2024

## Requirements

No special requirements. Some tasks require "privileged role" at system. So, use [become](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_privilege_escalation.html#using-become) option at your inventory list.

## Role Variables

This role is designed so the end user should not have to edit the tasks themselves. All customizing should be done via the defaults/main.yml file or with extra vars within the project, job, workflow, etc.

## Example Playbook

    - hosts: servers
      roles:
        - role: dafneb.ubuntu24-cis
          vars:
            hardening_ansible_console_ip:
              - 127.0.0.1
            hardening_admin_device_ip:
              - 127.0.0.1

## License

[MIT](LICENSE)
