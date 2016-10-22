# Ansible Role: CVE
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-cve-blue.svg)](https://galaxy.ansible.com/pgporada/cve/)
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.txt)

This role mitigates/patches the defined CVEs.

- - - -

# Role Variables

Dirty COW vuln. http://dirtycow.ninja. Defaults to false.

        cve_2016_5195: false

- - - -

# Example Playbook
```
---
- hosts: localhost
  connection: local
  become: true
  become_method: sudo

  vars:
    cve_2016_5195: true

  roles:
    - ../ansible-role-cve
```

- - - -

# How to hack away at this role
Before submitting a PR, please create a test and run it through test-kitchen.

```
git clone git@github.com:pgporada/ansible-role-cve.git
bundle install
bundle exec kitchen create
bundle exec kitchen converge
bundle exec kitchen verify
bundle exec kitchen destroy
```

- - - -

# Author Information

Phil Porada

- - - -

# License

MIT

(c) 2016 GreenLancer.com
