# Futtató környezet kialakítása

Létre kell hozni a tanúsítványokat a konfigurációt és az ldap adatbázist tartalmazó könyvtárakat.

`mkdir -p /opt/ldap/certs /opt/ldap/database /opt/ldap/config`{{execute}}


# Docker konténer futtatása

Futtassuk a konténert, becsatolva a megfelelő könyvtárakat.

```
docker run -p 389:389 -p 636:636 --hostname ${HOSTNAME} --name ldap --detach \
  --volume /opt/ldap/database:/var/lib/ldap \
  --volume /opt/ldap/config:/etc/ldap/slapd.d \
  --volume /opt/ldap/certs:/container/service/slapd/assets/certs \
  sztaki/openldap-for-research-institutes:0.1.0
```{{execute}}

Nézzük az logokat:

`docker logs -f ldap`{{execute}}


ctrl+c leütésével ki lehet szállni a logok nézetéből.

