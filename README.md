# AlexGx_infra
AlexGx Infra repository

## one line someinternalhost connect
ssh -o ProxyCommand='ssh -W %h:%p appuser@35.190.203.58' appuser@someinternalhost

## via `ssh someinternalhost` connect config
```
Host bastion
  Hostname 35.190.203.58
  User appuser

Host internalhost
  Hostname 10.142.0.2
  User appuser
  Proxycommand ssh bastion -W %h:%p
```

bastion_IP = 35.190.203.58
someinternalhost_IP = 10.142.0.2

