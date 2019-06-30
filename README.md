# Ansible Role: Patching

#### Version: 1.2.0

[![](https://img.shields.io/badge/role-sparknsh.patching-blue.svg)](https://galaxy.ansible.com/sparknsh/patching)

Development of this project is managed in a private repository then pushed out to [GitLab](https://gitlab.com/sparknsh/ansible-role-patching) and [GitHub](https://github.com/sparknsh/ansible-role-patching) when we have a new version for you. If you have any issues please contact [sparknsh](https://www.sparknsh.com/contact?type=issue&name=ansible-role-patching)

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
patching__audit_packages: false
```

This variable gives you the ability to see what was installed and updated on every server.

```yaml
patching__upgrade_all: false
patching__repo_clean: true
```

By default update will always run. If you want to run a upgrade changing the variable will disable update and run upgrade. `patching__repo_clean` is going to clean up old files off your server.

```yaml
patching__update_security: false
```

RHEL distros offer the ability to patch just security updates. Change this to True and just patch all security updates.

#### Coming Soon

  - Reboot support in Version 1.3.0
  - Fedora Support in Version 1.5.0

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

This role was created in 2019 by [sparknsh](https://www.sparknsh.com) at [Rebel Media, Inc.](https://www.rebelmedia.io/)
