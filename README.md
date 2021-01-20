Netplan
=========

An ansible role to manage Netplan configuration

Requirements
------------

N/A

Role Variables
--------------


| Variable              | Purpose                                                             | Default |
| --------------------- | ------------------------------------------------------------------- | ------- |
| `netplan_lib_configs` | Dictionary of Netplan configurations located in /lib/netplan/*.yaml | {}      |
| `netplan_etc_configs` | Dictionary of Netplan configurations located in /etc/netplan/*.yaml | {}      |

Dependencies
------------

N/A

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - { role: netplan }
  vars:
    netplan_etc_configs:
      50-br1:
        network:
          version: 2
          bridges:
            br1:
              addresses:
                - 192.0.2.1/24

```

License
-------

BSD
