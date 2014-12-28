Freifunk IC-VPN
===============

A role to connect a server to the Freifunk Intercity VPN.
You find all information at the [Freifunk Wiki](http://wiki.freifunk.net/IC-VPN).

Requirements
------------

You need a Freifunk Gateway that should be connected to the Intercity VPN.

Role Variables
--------------

    icvpn_hostname = 'koeln1'
    icvpn_ipv4_addr = 10.207.0.57/16
    icvpn_ipv6_addr = fec0::a:cf:0:57/96

Example Playbook
----------------

    - hosts: supernodes
      roles:
         - { role: freifunk.icvpn, x: 42 }

License
-------

BSD
