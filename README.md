# Website Cheat Sheet
Documentation for ispconfig administrator about website management and view system log for fix other problem

# Table of Content
* ISPConfig
* Auth Log
* Fail2ban Log
* Apache Log
* FTP Log
* Website Log
* Export Log

## Auth Log
```bash
$ cd /var/log
$ tail -f auth.log
```

## Fail2ban Log
```bash
$ cd /var/log
$ tail -f fail2ban.log
```

## Apache Log
```bash
$ cd /var/log/apache2
$ tail -f access.log
$ tail -f error.log
```

## FTP Log
```bash
$ cd /var/log/pure-ftpd
$  tail -f transfer.log
```

## Website Log
```bash
$ cd /var/www/[Website]/log
$ tail -f error.log
```

## Export Log
```bash
$ tail -n 1000 access.log > today.log
```

## License
Codeinsane license.