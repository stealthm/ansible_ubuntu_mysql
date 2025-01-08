# Ansible Role: Ubuntu MySQL

An Ansible role for MySQL installation

Sets the root password, mysql or mariadb packages

## Role Variables
All variables that can be overridden are stored in the [defaults/main.yml]

## Requirements

Ansible

This role requires root access, so run it in a playbook with a global become: yes

## Dependencies
You need to install Ansible collections:
```bash
ansible-galaxy collection install -r requirements.yml
```

## Testing
- Molecule, Molecule-plugins

You can install it like this:
```bash
pip3 install molecule-plugins
pip3 install ansible-lint
pip3 install python-vagrant
pip3 install docker
pip3 install podman
```
- Docker image

You need Ubuntu image with systemd and dbus support (thanks https://github.com/antmelekhin/docker-systemd ) or use Vagrant
```bash
docker build -t ubuntu-server24 -f molecule/default/Dockerfile-24.04 .
```
- Example

```bash
molecule test
molecule test -s vagrant
```

## Tested on

ansible-core     >=2.18

molecule         >=24

molecule-plugins >=23

## Supported platforms
Ubuntu
  - 20.04
  - 22.04
  - 24.04

## License

MIT
