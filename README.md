# Ansible Role: bu-node

## Description

These are tasks to configure iptables on a CentOS host.

This is typically made to set, per-rule:

* chain
* comment
* source address
* destination port
* protocol
* target

### Requirements

* RHEL-only

## Role Variables

```yaml
variable: value # comment
```

## Tags

### Role-Specific tags:

* `iptables`
* `iptables_install`
* `iptables_config`

### Global tags:

* `install`
* `config`
### Dependencies

* `smacz42.common`
* `smacz42.iptables`
* `smacz42.httpd`

## Example Playbook

```yaml
- name: Roles in Common
  hosts: all
  gather_facts: true
  remote_user: root
  #no_log: true

  roles:
    - { role: common }
    - { role: iptables }
```

## TODO:

* ip6tables

## License

Licensed under the MIT License. See the LICENSE file for details.

## Author Information

This role was created in 2017 by [Andrew Cz](https://andrewcz.com), a student at The Ohio State University.
