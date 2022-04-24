# ansible-tor-bridge-debian
Tor obfs4 bridge setup automation for Debian based on [this guide](https://community.torproject.org/relay/setup/bridge/debian-ubuntu/).

## Setup

Create a "hosts" file, e.g.:
```
[bridges]
111.222.333.444 or_port=5566 obfs4_port=6655 name="MyBridge"

[all:vars]
ansible_connection=ssh
ansible_user=root

contact=test@test.com
```

## Deploy
```
$ ansible-playbook deploy-tor-bridge.yml
```