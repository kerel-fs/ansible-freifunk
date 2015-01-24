Freifunk Supernode
===============

A role to configure supernodes for a Freifunk Community.
This role depends on fastd and one of batman-adv-14, batman-adv-15.
Supernodes are connected to each other through a Tinc VPN.

Requirements
------------

Add this filter plugin to your ansible installation:
https://github.com/digineo/ansible-ipcalc

Role Variables
--------------

Group-specific variables:

    ff_domain: your domain, Ex: 'kbu.freifunk.net'
    ff_lease_time: dhcp-lease-time (default: 86400 seconds)
    ff_dns: list of DNS-Servers to announce via dhcp (default: 213.73.91.35 - ccc)
    ff_anycast_dns: unbound settings
      interface: list of addresses to bind to
      access_control: list of subnets to allow access from
    ff_forwarders: dict, forwarded DNS-Zones
      [zone]: Ex: ".", hack, dn42
      - [IP of DNS-Server to query]
    ff_network: used subnets in your network
      ipv4: Ex: 172.27.0.0/18
      ipv6: Ex: 2001:67c:20a0:b100::/60
      ipv6_ula: Ex: fdd3:5d16:b5dd::/64
    ff_orig_interval: batman-adv originator interval (default: 5000)
    fastd_pubkeys_repo: URL, fastd backbone keys are fetched from this
    fastd_pubkeys_repo_version: Version to fetch (default: master)

Host-specific variables:

    ff_server: subnets to be used by this host
      ipv4: Ex: 172.27.0.0/21
      ipv6: Ex: 2001:67c:20a0:b100::/64
      iface_mac: MAC of the fastd-vpn-interface (default: random)
    ff_gw_bandwidth: batman-adv gateway_mode announced bandwidth (default: 100MBit/100MBit)

Take a look at `defaults/main.yml`

Example Playbook
----------------

    - hosts: supernodes
      roles:
      - fastd
      - batman-adv-14
      - freifunk.supernode

License
-------

BSD
