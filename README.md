openwrt-firewall
================

firewall config of your openwrt system.
compare: [http://wiki.openwrt.org/doc/uci/firewall]

Role Variables
--------------

there is a nested dict `firewall`. below you find another nested dict
`policies`. the layout is a bit weird because i use with_subelements.
policies describes the interface to interface iptables policy. there
is also `forwarding` to allow for extra inter-zone traffic as well as
`redirect` for port forwards.

you may want to consider `hash_behaviour=merge` in your ansible.cfg

Dependencies
------------

[lefant.openwrt-uci]

Example Playbook
----------------

[https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml]

Requirements
------------

must be kept minimal as this is supposed to run on openwrt embedded
systems. in particular we try get by with plain POSIX shell, using
neither python nor bash in any way. lua could be an option as that
seems to be the openwrt scripting language of choice.

License
-------

BSD

Author Information
------------------

Fabian Linzberger, [http://e.lefant.net/]



[https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml]: https://github.com/lefant/ansible-openwrt/blob/master/openwrt.yml
[http://wiki.openwrt.org/doc/uci/firewall]: http://wiki.openwrt.org/doc/uci/firewall
[lefant.openwrt-uci]: https://galaxy.ansible.com/list#/roles/1645
[http://e.lefant.net/]: http://e.lefant.net/
