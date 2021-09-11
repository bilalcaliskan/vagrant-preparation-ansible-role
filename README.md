# Vagrant Preparation Ansible Role

[![CI](https://github.com/bilalcaliskan/vagrant_preparation-ansible-role/workflows/CI/badge.svg?event=push)](https://github.com/bilalcaliskan/vagrant_preparation-ansible-role/actions?query=workflow%3ACI)

Sets up Vagrant development environment.

## Requirements

This role requires minimum Ansible version 2.4 and maximum Ansible version 2.9. You can install suggested version with pip:
```
$ pip install "ansible==2.9.16"
```

No special requirements. Also note that this role requires root access, so either run
it in a playbook with a global `become: true`, or invoke the role in your playbook.

## Role Variables
See the default values in [defaults/main.yml](defaults/main.yml). You can overwrite them in [vars/main.yml](vars/main.yml) if neccessary or you can set them while running playbook.

Also please see the Redhat ansible_os_family specific variables in [vars/redhat.yml](vars/redhat.yml) and Debian ansible_os_family specific variables in [vars/debian.yml](vars/debian.yml).

## Dependencies

None

## Example Playbook File

```yaml
- hosts: all
  become: true
  roles:
    - role: bilalcaliskan.vagrant_preparation
```

## Development
This project requires below tools while developing:
- [Ansible 2.4 or higher](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
- [pre-commit](https://pre-commit.com/)
- [ansible-lint](https://ansible-lint.readthedocs.io/en/latest/installing.html#using-pip-or-pipx) - required by [pre-commit](https://pre-commit.com/)
- [Bash shell](https://www.gnu.org/software/bash/) - required by [pre-commit](https://pre-commit.com/)

## License
Apache License 2.0
