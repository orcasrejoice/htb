# Description
Everything you need to know about ```smbclient```

### Notes
- Once you're connected and in an ```smbclient``` shell, you'll see something like this: ```smb: \>```. Then, use regular bash/Linux commands to navigate.

### How to list all shares
1. ```smbclient -L //<IP_ADDRESS> -U <username>```
### How to connect to ```smbclient```
1. ```smbclient //<IP_ADDRESS>/<share_name> -U <username>```
