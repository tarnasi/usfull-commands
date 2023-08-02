# usfull-commands


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
ng config -g cli.packageManager yarn
