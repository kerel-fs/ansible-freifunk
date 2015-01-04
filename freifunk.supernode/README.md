Freifunk Supernode
===============

A role to set up supernodes for a Freifunk Community.
Supernodes are connected to each other through a Tinc VPN.

Requirements
------------

Add this filter plugin to your ansible installation:
https://github.com/digineo/ansible-ipcalc

Role Variables
--------------

Take a look at `defaults/main.yml`

Example Playbook
----------------

    - hosts: supernodes
      roles:
         - role: freifunk.icvpn

License
-------

BSD
