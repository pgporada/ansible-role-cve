# Ansible Role: CVE
This role checks CVEs

- - - -

# Role Variables

Dirty COW vuln. http://dirtycow.ninja

        cve_2016_5195: false

- - - -

# Example Playbook
```
---
- hosts: localhost
  connection: local
  become: true
  become_method: sudo
  roles:
    - ansible-role-cve
```

- - - -

# How to hack away at this role
Before submitting a PR, please create a test and run it through test-kitchen.

```
git clone git@bitbucket.org:greenlancer/ansible-role-cve.git
bundle install
bundle exec kitchen create
bundle exec kitchen converge
bundle exec kitchen verify
bundle exec kitchen destroy
```
