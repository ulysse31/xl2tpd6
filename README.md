# xl2tpd6

This is a fork of the official xl2tpd source (v1.3.17) with modified source
and setups to generate xl2tpd6: an IPv6 L2TP server, allowing IPv4 inside
IPv6 tunneling. This versions have kernel support for kernel L2TP.

## STATUS:
For now, server builds and seems fully functional, but listen-addr is NOT
taken into account in the configuration, it will listen on :: (any IPV6 address)

Scripts for package generation are not yet functional, simply compile it,
it will generate an xl2tpd6 binary, that you can copy manually to same
binary path as your legacy xl2tpd.

For the configuration, it will by default try to read /etc/xl2tpd/xl2tpd6.conf

For the Startup, you will have inside debian/xl2tpd6.init a rc.init file that works

Of course, this binary can run aside of the legacy xl2tpd binary
(one listening in IPv4, the other in IPv6).

