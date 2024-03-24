# Ansible role [glusterfs](https://galaxy.ansible.com/ui/standalone/roles/buluma/glusterfs/documentation)

Install and configure glusterfs on your system.

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-glusterfs/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-glusterfs/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-glusterfs.svg)](https://github.com/buluma/ansible-role-glusterfs/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-glusterfs.svg)](https://github.com/buluma/ansible-role-glusterfs/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-glusterfs.svg)](https://github.com/buluma/ansible-role-glusterfs/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/glusterfs)](https://galaxy.ansible.com/ui/standalone/roles/buluma/glusterfs/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-glusterfs/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: buluma.glusterfs
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-glusterfs/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  gather_facts: no
  become: yes

  roles:
    - role: buluma.bootstrap
    - role: buluma.apt_autostart
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-glusterfs/blob/master/defaults/main.yml):

```yaml
---
# defaults file for glusterfs

# A list of bricks and their properties.
# glusterfs_bricks:
#   - name: brick1
#     device: /dev/vdb
#     mountpoint: /data/brick1
glusterfs_bricks: []

# A list of volumes and their properties.
# glusterfs_volumes:
#   - name: gv0
#     bricks: /data/brick1/gv0
#     replicas: 3
#     mountpoint: /mnt/gv0
#     rebalance: no
glusterfs_volumes: []
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-glusterfs/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.apt_autostart](https://galaxy.ansible.com/buluma/apt_autostart)|[![Ansible Molecule](https://github.com/buluma/ansible-role-apt_autostart/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-apt_autostart/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-apt_autostart.svg)](https://github.com/shadowwalker/ansible-role-apt_autostart)|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-glusterfs/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Debian](https://hub.docker.com/r/buluma/debian)|bullseye|
|[Fedora](https://hub.docker.com/r/buluma/fedora)|all|
|[Ubuntu](https://hub.docker.com/r/buluma/ubuntu)|all|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-glusterfs/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-glusterfs/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-glusterfs/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)

