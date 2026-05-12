
ifconfig (old):
``` shell
ifconfig ${interface_name}:1 ${address}/${mask} up
```

iproute2:
``` shell
ip address add ${address}/${mask} dev ${interface name} label ${interface name}:${description} 
```
