# Samba File Server

## Overview

Project Atlas uses Samba to provide Windows-compatible network file sharing.

Shared folders allow users from different departments to access common resources across the enterprise network.

---

## File Server

* Software: Samba
* Server IP: 10.10.50.10

---

## Configuration File

```text
/etc/samba/smb.conf
```

---

## Shared Folders

The following departmental shares were created:

* Public
* IT
* HR
* Finance
* Sales

Each share is mapped to its own directory under:

```text
/srv/shares/
```

---

## Access

Users access shared folders using:

```text
\\hq-srv.atlas.local\
```

or

```text
\\10.10.50.10\
```


---

## Verification

Testing confirmed that clients could:

* Browse available shares
* Open shared folders
* Upload files
* Download files

Testing was performed from both Linux and Windows client systems.

---

