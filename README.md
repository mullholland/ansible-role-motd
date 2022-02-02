# [motd](#motd)

|GitHub|GitLab|
|------|------|
|[![github](https://github.com/mullholland/ansible-role-motd/workflows/Ansible%20Molecule/badge.svg)](https://github.com/mullholland/ansible-role-motd/actions)|[![gitlab](https://gitlab.com/mullholland/ansible-role-motd/badges/master/pipeline.svg)](https://gitlab.com/mullholland/ansible-role-motd)|[![quality](https://img.shields.io/ansible/quality/unset)](https://galaxy.ansible.com/mullholland/motd)|

Creates a motd for Linux systems.

## [Role Variables](#role-variables)

These variables are set in `defaults/main.yml`:
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
```


## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
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





## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/mullholland):

-   [debian9](https://hub.docker.com/r/mullholland/docker-molecule-debian9)
-   [debian10](https://hub.docker.com/r/mullholland/docker-molecule-debian10)
-   [debian11](https://hub.docker.com/r/mullholland/docker-molecule-debian11)
-   [ubuntu1804](https://hub.docker.com/r/mullholland/docker-molecule-ubuntu1804)
-   [ubuntu2004](https://hub.docker.com/r/mullholland/docker-molecule-ubuntu2004)
-   [centos7](https://hub.docker.com/r/mullholland/docker-molecule-centos7)
-   [centos-stream8](https://hub.docker.com/r/mullholland/docker-molecule-centos-stream8)
-   [centos-stream9](https://hub.docker.com/r/mullholland/docker-molecule-centos-stream9)
-   [ubi8](https://hub.docker.com/r/mullholland/docker-molecule-ubi8)
-   [fedora34](https://hub.docker.com/r/mullholland/docker-molecule-fedora34)
-   [fedora35](https://hub.docker.com/r/mullholland/docker-molecule-fedora35)
-   [amazonlinux](https://hub.docker.com/r/mullholland/docker-molecule-amazonlinux)
-   [rockylinux8](https://hub.docker.com/r/mullholland/docker-molecule-rockylinux8)
-   [almalinux8](https://hub.docker.com/r/mullholland/docker-molecule-almalinux8)

The minimum version of Ansible required is 2.10, tests have been done to:

-   The last 2 versions.
-   The current version.





If you find issues, please register them in [GitHub](https://github.com/mullholland/ansible-role-motd/issues)

## [License](#license)

MIT


## [Author Information](#author-information)

[Mullholland](https://github.com/mullholland)

## [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)
