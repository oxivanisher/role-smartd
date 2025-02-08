smartd
======
[![Ansible Lint](https://github.com/oxivanisher/role-smartd/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/oxivanisher/role-smartd/actions/workflows/ansible-lint.yml)

This role configures smartd from the smartmontools to make it more sensible with Raspberry Pis and systems with NVME drives. It
* Ensures smartd does not stop when no disks are found (rpis i.e.)
* Disable devicescan to reduce spam mails for nvme drives if `smartd_disable_devicescan` is set

Role Variables
--------------

| Name                      | Comment             | Default value                    |
|---------------------------|---------------------|----------------------------------|
| smartd_disable_devicescan | Disable device scan | `false` |

Dependencies
------------

None

Example Playbook
----------------
```yaml
- name: Debian clients
  hosts: debian
  roles:
    - role: oxivanisher.linux_base.smartd
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_base](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_base/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_base).
