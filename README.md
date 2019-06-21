# ansible-role-go
installs golang (defaults to v1.12.6) on linux (arch amd64, i386 and armv6l ) under /opt/go-$version.

## example
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
    - go_version: 1.12.6
  roles:
    - ThorstenS-linux.ansible_role_go
EOF
$ chmod +x golang.yml
$ ./golang.yml
```


