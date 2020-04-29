# Docker konténer futtatása

--hostname ${HOSTNAME}

```
docker run -p 389:389 -p 636:636 --hostname ${HOSTNAME} --name ldap --detach \
  --volume /opt/ldap/database:/var/lib/ldap \
  --volume /opt/ldap/config:/etc/ldap/slapd.d \
  --volume /opt/ldap/certs:/container/service/slapd/assets/certs \
  sztaki/openldap-for-research-institutes:0.1.0
```{{execute}}


`docker logs ldap`{{execute}}

`docker start ldap`{{execute}}

`docker logs -f ldap`{{execute}}

