## Vagrant Preparation Ansible Role

[![Build Status](https://travis-ci.org/bilalcaliskan/vagrant_preparation-ansible-role.svg?branch=master)](https://travis-ci.org/bilalcaliskan/vagrant_preparation-ansible-role)

Sets up Vagrant development environment.

## Requirements

No special requirements; note that this role requires root access, so either run it in a playbook with a global `become: yes`, or invoke the role in your playbook like:

      - hosts: all
        become: true
        roles:
          - role: bilalcaliskan.vagrant_preparation

## Role Variables

See the default values in 'defaults/main.yml'. You can overwrite them in 'vars/main.yml' if neccessary.

## Dependencies

None

## Example Playbook

      - hosts: all
        become: true
        vars_files:
          - vars/main.yml
        roles:
          - { role: bilalcaliskan.vagrant_preparation }

*Inside `vars/main.yml`*:
      timezone: Europe/Istanbul
      required_packages:
        - java-1.8.0-openjdk
        - firewalld

## License

MIT / BSD
