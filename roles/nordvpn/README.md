NordVPN
=======

An Ansible Role that installs and configures [NordVPN](https://www.nordvpn.com/).

Requirements
------------

This role has only been tested on Ubuntu 20.04.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml)

    nordvpn_users: []

A list of users to add to the nordvpn group.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      
      vars:
        nordvpn_users:
          - "{{ ansible_user_id }}"

      roles:
         - orjangj.vpn.nordvpn

License
-------

MIT / BSD
