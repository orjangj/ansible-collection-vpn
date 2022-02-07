FortiClient
===========

An Ansible Role that installs and configures [FortiClient](https://www.fortinet.com/support/product-downloads#vpn)

Requirements
------------

This role has only been tested on Ubuntu 20.04.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml)

    forticlient_version: "7.0"

The FortiClient version to download (only 7.0 and 6.4 versions are available).

    forticlient_arch: "amd64"

The architecture to install for.

    forticlient_source: "apt"

The source to install from (either "apt" or "deb").

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all

      roles:
         - orjangj.vpn.forticlient

License
-------

MIT / BSD
