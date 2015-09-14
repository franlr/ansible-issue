# ansible-issue
Manage the issue.net file as a MOTD file only if "Banner" sshd service's option has been enabled

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

GPLV2

Author
------

Fran LR
