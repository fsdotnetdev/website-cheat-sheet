# WMIC
Documentation

## Startup
```bash
wmic startup list full > c:\startup.txt
```

## DNS Cache
```bash
ipconfig /displaydns > C:\dnscache.txt
```

## List Process
```bash
wmic process list full | more > c:\list_process.txt
```

## List Service
```bash
wmic service list full > c:\list_service.txt
```

## List Job
```bash
wmic job list full > c:\list_job.txt
```

## Product Name
```bash
wmic /node:10.100.100.239 /user:LAB\administrator /password:"P@ssw0rd" product get name > c:\log_product.txt
```

## Process Call
```bash
wmic /node:10.100.100.239 /user:LAB\administrator /password:"P@ssw0rd" process call create > c:\log_process.txt
```

## Check List
```bash
tasklist /s \\10.100.100.239 /u LAB\administrator /p P@ssw0rd > c:\tasklist.txt
```

## Program Initial Connection
```bash
netstat -b 5 >> C:\connections.txt

https://commandwindows.com/netstat.htm
```