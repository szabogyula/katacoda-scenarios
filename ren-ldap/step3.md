# Docker konténer futtatása

```
docker run --port 389:389 --port 636:636 --hostname ${HOSTNAME} --name ldap --detach \
  --volume /opt/ldap/database:/var/lib/ldap \
  --volume /opt/ldap/config:/etc/ldap/slapd.d \
  --volume /opt/ldap/certs:/container/service/slapd/assets/certs \
  sztaki/openldap-for-research-institutes:0.1.0
```

