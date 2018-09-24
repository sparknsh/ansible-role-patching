# Ansible Role: Patching

#### Version: 1.0.3

[![pipeline status](https://gitlab.com/sparknsh/ansible-role-patching/badges/master/pipeline.svg)](https://gitlab.com/sparknsh/ansible-role-patching/commits/master)
[![Ansible Role](https://img.shields.io/ansible/role/29003.svg)](https://galaxy.ansible.com/sparknsh/patching)
[![Ansible Role](https://img.shields.io/ansible/role/d/29003.svg)](https://galaxy.ansible.com/sparknsh/patching)

Development of this project is managed in a private repository then pushed out to [GitLab](https://gitlab.com/sparknsh/ansible-role-patching) and [GitHub](https://github.com/sparknsh/ansible-role-patching) when we have a new version for you. If you have any issues please contact [sparknsh](https://www.sparknsh.com/contact?type=issue&name=ansible-role-patching)

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
patching_reboot_server: False
```

Reboot of the server is the most important variable to set. If you don't want the server to reboot leave it alone. If you want the server to reboot you need to change this variable.

```yaml
patching_upgrade_all: False
patching_repo_clean: True
```

By default update will always run. If you want to run a upgrade changing the variable will disable update and run upgrade. `patching_repo_clean` is going to clean up old files off your server.

```yaml
patching_update_security: False
```

RHEL distros offer the ability to patch just security updates. Change this to True and just patch all security updates.

#### Coming Soon

Fedora Support in Version 1.5.0

## Example Playbook

```yaml
- hosts: all
  vars_files:
    - vars/main.yml
  roles:
    - { role: sparknsh.patching }
```

## License

MIT

## Author Information

This role was created in 2018 by [sparknsh](https://www.sparknsh.com) at [Rebel Media, Inc.](https://www.rebelmedia.io/)
