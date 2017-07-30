Configure system log
====================

Sympa reports events and errors using syslog protocol.

* The log facility is ``LOCAL1`` by default, and it may be changed by [``log_facility``](../man/sympa.conf.5.md#log_facility) parameter in sympa.conf.

* The default value of [``log_socket_type``](../man/sympa.conf.5.md#log_socket_type) parameter is ``unix``, using Unix domain socket to communicate with syslog server.  Some platforms including Solaris prefer to ``stream``.  The value may also be ``inet``, using TCP or UDP connection.

Traditional syslog
------------------

Add following line to syslog.conf:
```
local1.* /var/log/sympa.log
```
Then restart syslog service.
