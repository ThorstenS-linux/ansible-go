# ansible-go
installs go on linux

```bash
#!/usr/bin/env ansible-playbook                                                                               
# install golang
#

- hosts: localhost
  vars:
    - go_installdir: "/usr/local/bin"
  roles:
    - ThorstenS-linux-go
```
