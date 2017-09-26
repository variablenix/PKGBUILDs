# openldap

This OpenLDAP PKGBUILD is the build from the Arch [core] repo. The difference with this build is it enables the following additional modules:

1. auditlog  (logging)
2. accesslog (logging)
3. syncprov  (replication)

```
42,43c42,45
<     --enable-backends --disable-ndb --enable-overlays=mod \
<     --with-cyrus-sasl --with-threads
---
>     --enable-backends --disable-ndb --enable-overlays=mod --enable-auditlog=mod \
>     --with-cyrus-sasl --with-threads --enable-syncprov=mod --enable-accesslog=mod \
>     --enable-deref=mod 
```
