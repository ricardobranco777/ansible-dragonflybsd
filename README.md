# ansible-dragonflybsd

Ansible configuration for DragonflyBSD 4.2.0

Run:

```
# Update pkg
pkg update
# Ignore error
pkg upgrade
cp /usr/local/etc/pkg/repos/df-latest.conf.sample /usr/local/etc/pkg/repos/df-latest.conf
# Keep only Avalon repository
sed -i .bak '/^}/q' /usr/local/etc/pkg/repos/df-latest.conf
# The SSL certificate may be expired
sed -i .bak 's/https/http/' /usr/local/etc/pkg/repos/df-latest.conf
```

Enable SSH for root:

```
echo PermitRootLogin prohibit-password >> /etc/ssh/sshd_config
service sshd restart
pkg install python311
```

TODO
- Configure `qemu-guest-agent`

Run:

```
pkg autoremove
pkg clean
pkg audit -F
```
