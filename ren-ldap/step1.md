# Build image

Klónozzuk le a git repository-t.

`git clone https://git.sztaki.hu/aai/ren/ldap.git`{{execute}}

Lépjünk be a repo-ba `cd ldap`{{execute}} és állítsuk be a docker image környezeti paramétereit.

`cp environment/my-env.startup.yaml.dist environment/my-env.startup.yaml`{{execute}}

szerkesszük meg a környezeti paramétereket tartalmazó file-t

`environment/my-env.startup.yaml`{{open}}

buildeljük le a docker image-et.

`make`{{execute}}

