[![Build Status](https://travis-ci.org/Nani-o/ansible-role-ohmyzsh.svg?branch=master)](https://travis-ci.org/Nani-o/ansible-role-ohmyzsh)

ohmyzsh
=======

A simple role for installing [Oh-My-Zsh](http://ohmyz.sh/).

Compatibility
-------------

  - CentOS 6
  - CentOS 7
  - Ubuntu 14
  - Ubuntu 16
  - Ubuntu 18
  - Debian 7
  - Debian 8
  - Debian 9

Role Variables
--------------

- ohmyzsh_users

Users for which omyzsh will be configured.

```YAML
ohmyzsh_users:
  - bob
  - alice
```

Example Playbook
----------------

```YAML
    - hosts: servers
      vars:
        ohmyzsh_users:
          - bob
          - alice
      roles:
         - { role: ohmyzsh }
```

License
-------

MIT

Author Information
------------------

Sofiane MEDJKOUNE
