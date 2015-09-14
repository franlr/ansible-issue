# ansible-issue
Manage the issue.net file as a MOTD file only if "Banner" sshd service's option has been enabled

Requirements
------------
This role requires Ansible 1.4 or higher.

Dependencies
------------

Change "#Banner none" by "Banner /etc/issue.net" into `/etc/ssh/sshd_config` and restart the sshd service

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml.

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
issue_content: "Organization: sample-organization"
```

Example
-------

```
# This is a playlist example
- hosts: localhost
  # Load the role to produce the /etc/issue.net file
  roles:
    - role: ansible-issue
      issue_content: "test1: string1"
```

This playbook produces the `/etc/issue.net' file looking like this:

```
[root@localhost ~]# cat /etc/issue.net

test1: string1

```

Supported Platforms
-------------------

EL: 6

License
-------

Apache v2.0

Author Information
------------------

This role was created in 2015 by [FranLR](https://github.com/franlr/)
