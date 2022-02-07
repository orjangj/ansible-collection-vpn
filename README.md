# Ansible collection for vpn

This collection includes Ansible roles and content to help with vpn automation.

Roles included in this collection (click on the link to see the role's README and documentation):

  - `orjangj.vpn.nordvpn` ([documentation](https://github.com/orjangj/ansible-collection-vpn/blob/master/roles/nordvpn/README.md))
  - `orjangj.vpn.forticlient` ([documentation](https://github.com/orjangj/ansible-collection-vpn/blob/master/roles/forticlient/README.md))

## Supported distributions

* Ubuntu 20.04

## Installation

Currently not installable from Ansible Galaxy. Historically this collection has been for personal use only.

Install using `ansible-galaxy` with git url:

```
ansible-galaxy collection install git+https://github.com/orjangj/ansible-collection-vpn.git
```

Or include this collection in your playbook's `requirements.yml` file:

```
---
collections:
  - name: https://github.com/orjangj/ansible-collection-vpn.git
    type: git
    version: master
```

## Usage

Here's an example playbook which installs Docker, and adds the ansible user to the Docker group:

```yaml
- hosts: all

  vars:
    nordvpn_users:
      - "{{ ansible_user_id }}"

  roles:
    - orjangj.vpn.nordvpn
    - orjangj.vpn.forticlient
```

## License

MIT
