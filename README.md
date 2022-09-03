# OpenLDAP Docker Compose

You can access the project through the following link: https://ldap.homelab.

## Config Files:

If you want, you can create a [groups-users.ldif](init/groups-users.ldif "groups-users.ldif") file and set some default configurations.

## Folders:

1. LDAP database files.

``` bash
/var/lib/ldap
```

2. LDAP config files.

``` bash
/etc/ldap/slapd.d/container/service/slapd/assets/config/bootstrap/ldif/custom
```

## Commands:

1. Enter the container.

``` bash
docker exec -it openldap bash
cd /container/service/slapd/assets/config/bootstrap/ldif/
```

2. Sign in as admin.

``` bash
cn=admin,dc=homelab
```

3. Sign in as reader.

``` bash
cn=ldap-reader,dc=homelab
```

## Backup:

``` bash
./data/backup/tools/slapd-backup-config
./data/backup/tools/slapd-backup-data
```

## Restore:

``` bash
./data/backup/tools/slapd-restore-config <filename>
./data/backup/tools/slapd-restore-data <filename>
<filename> created on step 1.
```

## References:

1. [Docker hub image.](https://hub.docker.com/r/osixia/openldap "Docker hub image")

1. [Github - A docker image to run OpenLDAP.](https://github.com/osixia/docker-openldap "Github - A docker image to run OpenLDAP")

1. [Exemplo de como configurar o LDAP no Gitea.](http://www.jouvinio.net/wiki/index.php/Gitea_Configuration_LDAP "Exemplo de como configurar o LDAP no Gitea")

1. [Import / Export ldap database.](http://vaab.blog.kal.fr/2010/03/10/import-export-ldap-database "Import / Export ldap database")

## License:

[MIT](LICENSE "MIT License")

## Created by: 

1. Luciano Sampaio.
