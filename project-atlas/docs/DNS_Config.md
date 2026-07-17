# DNS Server Configuration

## Overview

Project Atlas uses BIND9 as its internal enterprise DNS server.

The DNS server provides hostname resolution for internal devices while also supporting recursive lookups for external domains.

---

## DNS Server

* Software: BIND9
* Server IP: 10.10.50.10
* Internal Domain:

```text
atlas.local
```

---

## Configuration Files

Main DNS options:

```text
/etc/bind/named.conf.options
```

Zone definitions:

```text
/etc/bind/named.conf.local
```

Forward lookup zone:

```text
/etc/bind/db.atlas.local
```

Reverse lookup zone:

```text
/etc/bind/db.10.10.50
```

---

## Forward Lookup Zone

The forward lookup zone maps hostnames to IPv4 addresses.

Example:

```text
hq-sw1.atlas.local  -> 10.10.95.1
hq-r1.atlas.local   -> 10.255.255.2
hq-srv.atlas.local  -> 10.10.50.10
www.atlas.local     -> 10.10.50.10
files.atlas.local   -> 10.10.50.10
```

---

## Reverse Lookup Zone

The reverse lookup zone performs the opposite function.

It maps IPv4 addresses back to hostnames using PTR records.

Example:

```text
10.10.50.10
↓

hq-srv.atlas.local
```

---

## Recursive DNS

BIND9 was configured to allow recursive queries.

This enables the server to:

* Resolve internal enterprise names
* Forward unknown queries to public DNS servers

Example:

```text
hq-sw1.atlas.local
```

is answered locally, while

```text
youtube.com
```

is forwarded to an upstream DNS server.

---

## Validation

Configuration was validated using:

* named-checkconf
* named-checkzone
* dig
* nslookup
* ping <hostname> or ping <hostname.domainname>
---

