# Apache Web Server

## Overview

Project Atlas hosts an internal company website using the Apache HTTP Server.

The website is available to enterprise users through the internal DNS name.

---

## Web Server

* Software: Apache2
* Server IP: 10.10.50.10

Website:

```text
http://www.atlas.local
```

---

## Web Root

Default document directory:

```text
/var/www/html
```

The default Apache landing page was replaced with a custom internal homepage for Project Atlas.

---

## DNS Integration

The DNS server resolves:

```text
www.atlas.local
```

to

```text
10.10.50.10
```

allowing users to access the website by hostname rather than IP address.

---

## Verification

The website was tested from client systems using:

* Linux curl
* Windows browsers(firefox, google chrome)

Successful access confirmed:

* DNS resolution
* HTTP connectivity
* Apache service availability

---

