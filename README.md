# ansible-dragonflybsd

Ansible configuration for DragonflyBSD 4.2.0

Run:

```
pkg update
pkg upgrade
```

NOTE: If any of the above command fail, run `cp /usr/local/etc/pkg/repos/df-latest.conf.sample /usr/local/etc/pkg/repos/df-latest.conf` and retry both.

Now run:

```
echo PermitRootLogin prohibit-password >> /etc/ssh/sshd_config
service sshd restart
pkg install python311
```

TODO
- Configure `qemu-guest-agent`
- Merge into https://github.com/ricardobranco777/ansible-freebsd
