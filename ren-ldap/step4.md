# Populáció

`docker exec ldap ldapsearch -x -H ldap://localhost -b dc=intezet,dc=hu -D "cn=admin,dc=intezet,dc=hu" -wadmin`{{execute}}

Vizsgáljuk meg a tesztusereket az editorban. Van egy `admin`, akit a későbbiekben felruházhatunk admin jogosultságokkal.

`ldap/testusers/user.ldif`{{open}}

`cat testusers/user.ldif | docker exec ldap ldapmodify -x -H ldap://localhost -D "cn=admin,dc=intezet,dc=hu" -wadmin`{{execute}}

Vizsgáljuk meg az admin csoporthoz való rendelését az `ądmin` usernek. Nyissk meg a file-t az editorban, és írjuk át a megfelelő attribútumot.

`ldap/admin.ldif`{{open}}

Majd futtassuk le az ldapmodify-t az adatbázison.

`cat admin.ldif | docker exec ldap ldapmodify -x -H ldap://localhost -D "cn=admin,dc=intezet,dc=hu" -wadmin`{{execute}}

Listázzuk újra az ldap adatbázist.

`docker exec ldap ldapsearch -x -H ldap://localhost -b dc=intezet,dc=hu -D "cn=admin,dc=intezet,dc=hu" -wadmin`{{execute}}

