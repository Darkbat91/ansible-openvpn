[![Build Status](https://travis-ci.org/Darkbat91/openvpn.svg?branch=v1)](https://travis-ci.org/Darkbat91/openvpn)

# Ansible openvpn role
Basic ansible role to enable openvpn on a Centos server listening on TCP 443 to bypass firewalls and on 1194 for performance.

## Configuration
This server does not create any form of PKI and expects a folder to be passed to it in order to access its credentials

requires 1 variable

pki_dir: /path/to/my/pki

that directory is expected to have the below files within it to provision the server
```
vpn.pem - servers certificate
vpn.key - servers key
ta.key - key for openvpn signing
dh.pem - the dh parameters
ca.pem - ca for the server and clients
crl.pem - crl for the system
```

## Advanced

There are numerous other options within the [defaults/main.yml](./defaults/main.yml) that can change other parts of the behavior of the system

## Changelog
The [changelog](./CHANGELOG.md) is stored externally