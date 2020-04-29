# Birtokba vétel

Telepítsük a legnagyszerűbb ldap klienst: **ldapvi**

`apt install ldapvi`{{execute}}

Indítsuk el a kedvenc editorunkkal és vegyük birtokba az ldap adatbázist.

`ldapvi -h localhost -D uid=admin,ou=people,dc=intezet,dc=hu -w user --discover`{{execute}}

