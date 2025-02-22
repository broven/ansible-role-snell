# Ansible Role: Snell

This Ansible role installs and configures Snell proxy server on Linux systems.

## Requirements

- Ansible 2.9 or higher
- A supported Linux distribution (with systemd)
- Supported architectures: amd64, i386, aarch64, armv7l

## Installation

```bash
ansible-galaxy install git+https://github.com/broven/ansible-role-snell.git
```

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
# Snell version
snell_version: "v4.1.1"

# Installation directory
snell_install_dir: "/usr/local/bin"

# Service configuration
snell_port: 8388
snell_psk: "your_psk_here"  # Please change this in your playbook
```

## Example Playbook

```yaml
- hosts: servers
  become: yes
  vars:
    snell_port: 8388
    snell_psk: "your_secure_psk"
  roles:
    - ansible-role-snell
```

## Installation

1. Clone this repository or install via ansible-galaxy:
```bash
ansible-galaxy install broven.snell
```

2. Include the role in your playbook.

## Testing

To test the role on your local machine:

```bash
ansible-playbook tests/test.yml
```

## License

MIT

## Author Information

Created by broven 