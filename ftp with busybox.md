
### Server on busybox machine:
``` shell
tcpsvd -vE <ADDR> 21 ftpd -wvA <FTP_ROOT> &
```
This will start ftp server with allowed anonymous login and upload functionality.

### Upload a file:
```shell
ftp -u <IP_ADDR>:<DEST_FILE> <SOURCE_FILE>
```
