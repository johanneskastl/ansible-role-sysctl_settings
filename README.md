![Ansible Lint](https://github.com/johanneskastl/ansible-role-sysctl_settings/workflows/Ansible%20Lint/badge.svg)

sysctl_settings
=========

Adjust sysctl settings.

Requirements
------------

None.

Role Variables
--------------

- `sysctl_parameters`: list of dicts containing sysctl parameters and their values
- `sysctl_file_name`: file name inside `/etc/sysctl.d/`, defaults to `50_ansible.conf` (MUST end in `.conf`...!)

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.sysctl_settings'
          sysctl_parameters:
            - name: 'fs.inotify.max_user_instances'
              value: '512'
          sysctl_file_name: '87_inotify.max_user_instances.conf'


License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
