# ansible-go
installs go on linux

```bash
$ ansible-galaxy install --roles-path /tmp ThorstenS-linux.ansible_role_go
$ export ANSIBLE_ROLES_PATH=/tmp

$ cat >> golang.yml <<EOF
#!/usr/bin/env ansible-playbook
# install golang
#

- hosts: localhost
  become: yes
  vars:
    - go_installdir: "/usr/local/bin"
  roles:
    - ThorstenS-linux.ansible_role_go
EOF
$ chmod +x golang.yml
$ ./golang.yml
```


