# Description
This file lists several important or useful ```linux``` and ```bash``` commands.

# Simple generic commands
- ```rm <filename>```: deletes a file
- ```rmdir <directoryname>```: deletes a directory (only) if directory is empty
- ```rmdir -rf <directoryname>```: deletes a directory and everything inside
- ```ls```: list files in current directory
- ```ls -a```: lists all files in current directory, including hidden files
- ```pwd```: print working directory (shows current path)
- ```cat <filename.txt>```: shows contents of a ```.txt``` file
- ```sudo <command>```: SuperUser DO, allows user to operate with security privileges of another user (usually root)


# ```nmap```
- ```nmap <host-ip-address>```: scans IP address for open ports
- ```-sV```: shows service and version of open ports
- ```-p-```: scans all ports (1-65535) instead of only 1000 most common ports. very slow, recommend use with ```-T5``` (see below)
- ```-T1``` to ```-T5```: speeds of sending packages, from slowest to fastest. ```-T1``` is hard to detect, while ```-T5``` is very easily detected
