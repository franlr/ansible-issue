# ansible-issue
Manage the issue.net file as a MOTD file only if "Banner" sshd service's option has been enabled

Requirements
------------
This role requires Ansible 1.4 or higher.

Dependencies
------------

Make enabled "Banner /etc/issue.net" in `/etc/ssh/sshd_config`

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml.

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
issue_info:
- "Organization: ": "sample-organization"
- "Region: ": "sample-region"
```

Example
-------

```
# This is a playlist example
- host: myhost
  # Load the role to produce the /etc/issue.net file
  roles:
    - role: ansible-issue
      issue_info:
        - "test1: ": "string1"
        - "test2: ": "string2"
```

This playbook produces the `/etc/issue.net' file looking like this:

```
[root@localhost ~]# cat /etc/issue.net

test1: string1
test2: string2

```

License
-------

Apache v2.0

Author Information
------------------

This role was created in 2015 by [FranLR](https://github.com/franlr/)
