# Populáció

`docker exec ldap ldapsearch -x -H ldap://localhost -b dc=intezet,dc=hu -D "cn=admin,dc=intezet,dc=hu" -wadmin`{{execute}}

`ldap/testusers/user.ldif`{{open}}

`cat testusers/user.ldif | docker exec ldap ldapmodify -x -H ldap://localhost -b dc=intezet,dc=hu -D "cn=admin,dc=intezet,dc=hu" -wadmin`{{execute}}

`ldap/admin.ldif`{{open}}

`cat admin.ldif | docker exec ldap ldapmodify -x -H ldap://localhost -b dc=intezet,dc=hu -D "cn=admin,dc=intezet,dc=hu" -wadmin`{{execute}}

`docker exec ldap ldapsearch -x -H ldap://localhost -b dc=intezet,dc=hu -D "cn=admin,dc=intezet,dc=hu" -wadmin`{{execute}}

