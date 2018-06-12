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

- ohmyzsh_install_default_zshrc

If set to true, installs default ohmyzsh ~/.zshrc from ~/.oh-my-zsh/templates/zshrc.zsh-template only upon the first clone of the ohmyzsh repo.
If a ~/.zshrc  already exists, it is backuped.

```YAML
ohmyzsh_install_default_zshrc: true
```

- ohmyzsh_plugins_repos

List of git repositories of ohmyzsh plugins to installs.

```YAML
ohmyzsh_plugins_repos:
  - https://github.com/oldratlee/hacker-quotes
```

- ohmyzsh_themes_repos

List of git repositories of ohmyzsh themes to installs.

```YAML
ohmyzsh_themes_repos:
  - https://github.com/bhilburn/powerlevel9k
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
