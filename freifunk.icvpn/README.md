Freifunk IC-VPN
===============

A role to connect a server to the Freifunk Intercity VPN.
You find all information at the [Freifunk Wiki](http://wiki.freifunk.net/IC-VPN).

Requirements
------------

You need a Freifunk Gateway that should be connected to the Intercity VPN.

Role Variables
--------------

see defaults/main.yml

Example Playbook
----------------

    - hosts: supernodes
      roles:
         - freifunk.icvpn

License
-------

BSD
