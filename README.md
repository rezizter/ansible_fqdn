fqdn [![Build Status](https://github.com/rezizter/ansible_fqdn/actions/workflows/ci.yml/badge.svg)](https://github.com/rezizter/ansible_fqdn/actions/workflows/ci.yml)
====

Sets Fully qualified domain name (FQDN)

Requirements
------------

Ansible version 2.0+

## Platforms

* Ubuntu
* Debian
* AlmaLinux
* RockyLinux
* Windows

Credits
-------

This is a modified role from [![Holms.fqdn](https://github.com/holms/ansible-fqdn)]

Role Variables
--------------


| Variable name | Variable value | Default |
|---------------|----------------|---------|
|*hostname*     | hostname (eg. vm1) | `inventory_hostname_short` |
|*fqdn*         | domain name (eg. vm1.test.com) | `inventory_hostname` |
|*ip_address*         | ip address (eg. 192.168.0.20) | `ansible_default_ipv4.address` |

Example
-------

```
- hosts: mx.mydomain.com:mx
  user: root

  roles:
    - { role: fqdn, fqdn: "mx.mydomain.com", hostname: "mx" }
```

License
-------

MIT

