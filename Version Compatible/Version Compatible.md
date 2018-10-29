# Version Compatible
Description
```bash

```

# Table of Content
* Version OS
* Version MySQL
* Version PHP
* Version Web Server

## Version OS
```bash
$ lsb_release -a
```

## Version MySQL
```bash
$ mysql -u root -p
mariadb> show global variables like 'innodb_ver%' ;
```

## Version PHP
```bash
$ php --version
```

## Version Web Server
```bash
$ HEAD localhost
```

## License
Codeinsane license.

## Credit
http://www.fromdual.com/innodb-version