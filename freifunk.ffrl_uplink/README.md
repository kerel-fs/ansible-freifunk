Freifunk Rheinland Uplink
=========================

A role to connect a server to the Freifunk Rheinland Backbone.
You find further information at [Freifunk Hamburg IPv4-Uplink](http://wiki.freifunk.net/Freifunk_Hamburg/IPv4Uplink)
and [Freifunk KBU](https://kbu.freifunk.net/wiki/index.php?title=FFRL-Uplink).

Requirements
------------

You need a Freifunk Gateway and peering information from Freifunk Rheinland.

Role Variables
--------------

see defaults/main.yml

Example Playbook
----------------

    - hosts: supernodes
      roles:
        - { role freifunk.ffrl_uplink }

License
-------

BSD
