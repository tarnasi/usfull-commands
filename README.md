# usfull-commands

## Find a port and kill the process
```
windows: netstat -a -o -n | findstr :8999
windows: taskkill /PID [PID] /F
```

## Postgres Connection commands

### Debian based systems like Ubuntu:

```$ sudo -i -u postgres```

### Redhat based systems like Centos/Fedora:

```
$ su - postgres
$ createdb [dbname];


$ psql
```

### Windows:

```
$ psql -U postgres
```


## MSSQL Commands

```
[connect to the sql server command line in docker container]
/opt/mssql-tools/bin/sqlcmd -S 192.168.1.10 -U sa
```


## DATABASES Connections

```
[MSSQL]
Data Source=localhost,1433;Initial Catalog=mahdekodak;Persist Security Info=True;User ID=sa;Password=***********
- for asp.net local connection
Data Source=DB_SERVER;Initial Catalog=DB_NAME;User ID=DB_USER;Password=DB_PASSWORD;Connect Timeout=30;Encrypt=False;Trust Server Certificate=True;Application Intent=ReadWrite;Multi Subnet Failover=False

[Postgres]

[MYSQL]

```

## Angular

- Change package manager (global)

```bash
ng config -g cli.packageManager yarn
```

# Ubuntu git error insuffisante to .git/object
```bash
cd /path/to/repo/.git
sudo chgrp -R groupname .
sudo chmod -R g+rwX .
sudo find . -type d -exec chmod g+s '{}' +
```


# Docker Pipline for using in Docker Hub or any server

Pipline
```
1- Create a Dockerfile
2- Create new Image from Dockerfile
3- Image should have tag (version)
4- docker create [docker build -t my-app:1.0.0 .]
5- Create new Tag based on version
     - [docker tag my-app:1.0.0 saxonsoftware/my-app:2.0.0]
6- User for sending data to docker hub [docker push saxonsoftware/my-app:2.0.0]

Use [docker login] or Docker desktop for login into docker for access to push and pull
```
