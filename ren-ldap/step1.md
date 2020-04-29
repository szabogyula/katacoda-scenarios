# Build image

Klónozzuk le a git repository-t.

`git clone https://git.sztaki.hu/aai/ren/ldap.git`

Lépjünk be a repo-ba `cd ldap` és állítsuk be a docker image környezeti paramétereit.

`cp environment/my-env.startup.yaml.dist environment/my-env.startup.yaml`
`vim environment/my-env.startup.yaml`

buildeljük le a docker image-et.

`make`


