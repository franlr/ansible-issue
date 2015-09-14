# ansible-issue
Manage the issue.net file as a MOTD file only if "Banner" sshd service's option has been enabled

Requirements
------------
This role requires Ansible 1.4 or higher.

Example
-------

```
# This is a playlist example
- host: myhost
  # Load the role to produce the /etc/issue.net file
  roles:
    - issue
```

This playbook produces the `/etc/issue.net' file looking like this:

```
[root@localhost ~]# cat /etc/issue.net

Organization: sample-organization
Region: sample-region


```

Role variables
--------------

License
-------

Apache v2.0

Author Information
------------------

This role was created in 2015 by [FranLR](https://github.com/franlr/)
