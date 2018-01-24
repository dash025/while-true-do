[![Build Status](https://travis-ci.org/while-true-do/ansible-role-system-update.svg?branch=master)](https://travis-ci.org/while-true-do/ansible-role-system-update)

# Ansible Role: system-update
| A role to install updates or security updates.

For now the role is compatible to Redhat/CentOS, only. This will change over time and more Derivates will be included.

## Motivation

Updating a system is very common. Having a role, which helps for initial updates after installation or to enforce security updates, every now and then or via cron seems to be a good idea.

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while-true-do/system-update)

```
ansible-galaxy install while-true-do.system-update
```

Install from [Github](https://github.com/while-true-do/ansible-role-system-update)

```
git clone https://github.com/while-true-do/ansible-role-system-update.git while-true-do.system-update
```

## Requirements

**Used Modules**

-   [yum_module](http://docs.ansible.com/ansible/latest/yum_module.html)

## Dependencies

None.

## Role Variables

Below you can find the default variables.

```yaml
---
# Per default only security updates will be installed
wtd_system_update_security_only: True
# Auto Reboot, if needed. (kernel + glibc)
wtd_system_update_autoreboot: True
```

## Example Playbook

Simple Example:

```
- hosts: servers
  roles:
    - { role: while-true-do.system-update }
```

## Testing

This role is currently tested with syntax-checking and linting.
You can find the tests in [./tests](./tests/).

## Contribute / Bugs

Thank you so much for considering to contribute. Every contribution helps us. We are really happy, when somebody is joining the hard work. Please have a look at the links first.

-   [Contribution Guidelines](./docs/CONTRIBUTING.md)
-   [Create an issue or Request](https://github.com/while-true-do/ansible-role-system-update/issues)
-   [See who was contributing already](https://github.com/while-true-do/ansible-role-system-update/graphs/contributors)

## License

This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Author Information

Blog: [blog.while-true-do.org](https://blog.while-true-do.org)

Mail: [hello@while-true-do.org](mailto:hello@while-true-do.org)

