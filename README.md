# [Ansible role motd](#motd)

Creates a motd for Linux systems.

|GitHub|Downloads|Version|
|------|---------|-------|
|[![github](https://github.com/mullholland/ansible-role-motd/actions/workflows/molecule.yml/badge.svg)](https://github.com/mullholland/ansible-role-motd/actions/workflows/molecule.yml)|[![downloads](https://img.shields.io/ansible/role/d/mullholland/motd)](https://galaxy.ansible.com/mullholland/motd)|[![Version](https://img.shields.io/github/release/mullholland/ansible-role-motd.svg)](https://github.com/mullholland/ansible-role-motd/releases/)|
## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/mullholland/ansible-role-motd/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true
  # vars:
  #   example_var: "value"
  roles:
    - role: "mullholland.motd"
```



## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/mullholland/ansible-role-motd/blob/master/defaults/main.yml):

```yaml
---
# EXAMPLE (/etc/motd)
# Details what will be shown can be found in templates/etc/motd.j2
# ---------------------------------------------------------------
# This system is managed by Ansible
# ---------------------------------------------------------------
#
# System:
#   Hostname:     default-2.12-debian9
#   FQDN:         default-2.12-debian9
#   Distribution: Debian
#   - Version:    9.13
#   - Release:    stretch
#   Virtual:      Yes
#   - Type:       docker
#
#   CPUs:         8
#   Memory:       31.3GB
#   Swap:         24.0GB
#
#   Kernel:       5.15.18-200.fc35.x86_64
#   Timezone:     UTC(+0000)
#
# Network:
#   DNS Search:    XXX.tld
#   DNS Server(s): 8.8.8.8
#
# Interfaces:
#   Interface: eth0
#     ip: 172.17.0.2
#     mac: 02:42:ac:11:00:02
#   Interface: lo
#     ip: 127.0.0.1
#
# Mounts:
#   Mount: /dev/mapper/luks-XXX(/etc/hosts)(X.XGB)
#   Mount: /dev/mapper/luks-XXX(/etc/resolv.conf)(X.XGB)
#   Mount: /dev/mapper/luks-XXX(/etc/hostname)(X.XGB)
#
# ---------------------------------------------------------------

# Remove the folder /etc/update-motd.d
motd_remove_dynamic_motd: true

# Interface filter
motd_interfaces_startswith:
  # - "lo"
  - "eth"
  - "ens"
  - "eno"
  - "vmbr"
  - "wg"
  - "wire"
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/mullholland/ansible-role-motd/blob/master/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://mullholland.net) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/mullholland/ansible-role-motd/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/mullholland):

|container|tags|
|---------|----|
|[EL](https://hub.docker.com/r/mullholland/enterpriselinux)|all|
|[Amazon](https://hub.docker.com/r/mullholland/amazonlinux)|Candidate|
|[Fedora](https://hub.docker.com/r/mullholland/fedora/)|all|
|[Ubuntu](https://hub.docker.com/r/mullholland/ubuntu)|all|
|[Debian](https://hub.docker.com/r/mullholland/debian)|all|

The minimum version of Ansible required is 2.10, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/mullholland/ansible-role-motd/issues).

## [License](#license)

[MIT](https://github.com/mullholland/ansible-role-motd/blob/master/LICENSE).

## [Author Information](#author-information)

[Mullholland](https://mullholland.net)
