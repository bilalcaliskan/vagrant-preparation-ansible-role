## Vagrant Preparation Ansible Role

[![CI](https://github.com/bilalcaliskan/vagrant_preparation-ansible-role/workflows/CI/badge.svg?event=push)](https://github.com/bilalcaliskan/vagrant_preparation-ansible-role/actions?query=workflow%3ACI)

Sets up Vagrant development environment on RHEL/CentOS 7/8 servers.

### Requirements

No special requirements. Also note that this role requires root access, so either run
it in a playbook with a global `become: true`, or invoke the role in your playbook like:

```yaml
- hosts: all
  become: true
  roles:
    - bilalcaliskan.vagrant_preparation
```

### Role Variables
See the default values in [defaults/main.yml](defaults/main.yml). You can overwrite them in [vars/main.yml](vars/main.yml) if neccessary or you can set them while running playbook.

### Dependencies

None

### Example Playbook File

```yaml
- hosts: all
  become: true
  roles:
    - role: bilalcaliskan.vagrant_preparation
```

### License

MIT / BSD
