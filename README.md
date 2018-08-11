[![Build Status](https://travis-ci.org/while-true-do/ansible-role-system-update.svg?branch=master)](https://travis-ci.org/while-true-do/ansible-role-system-update)

# Ansible Role: system-update
| A role to install updates or security updates.

## Motivation

Updating a system is very common. Having a role, which helps for initial updates after installation or to enforce security updates, every now and then or via cron seems to be a good idea.

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while_true_do/system_update)

```
ansible-galaxy install while_true_do.system_update
```

Install from [Github](https://github.com/while-true-do/ansible-role-system-update)

```
git clone https://github.com/while-true-do/ansible-role-system-update.git while_true_do.system_update
```

## Requirements

Used Modules:

-   [command_module](https://docs.ansible.com/ansible/latest/modules/command_module.html)

Distribution specific modules:

-   [yum_module](https://docs.ansible.com/ansible/latest/modules/yum_module.html)
-   [dnf_module](https://docs.ansible.com/ansible/latest/modules/dnf_module.html)

## Dependencies

-   [reboot](https://github.com/while-true-do/ansible-role-reboot)

## Role Variables

Below you can find the default variables.

```yaml
# Reboot when needed (CentOS, RedHat).
wtd_system_update_autoreboot: True

# Only install security Updates (RedHat).
wtd_system_update_security_only: False
```

## Example Playbook

Simple Example:

```
- hosts: servers
  roles:
    - { role: while_true_do.system_update }
```

## Testing

All tests are located in [test directory](./tests/).

Basic testing:

```
bash ./tests/test-spelling.sh
bash ./tests/test-ansible.sh
```

## Contribute / Bugs

Thank you so much for considering to contribute. Every contribution helps us. We are really happy, when somebody is joining the hard work. Please have a look at the links first.

-   [Code of Conduct](./docs/CODE_OF_CONDUCT.md)
-   [Contribution Guidelines](./docs/CONTRIBUTING.md)
-   [Create an issue or Request](https://github.com/while-true-do/ansible-role-system-update/issues)
-   [See who was contributing already](https://github.com/while-true-do/ansible-role-system-update/graphs/contributors)

## License

This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Author Information

Site: [while-true-do.org](https://while-true-do.org)

Mail: [hello@while-true-do.org](mailto:hello@while-true-do.org)

