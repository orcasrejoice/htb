# Description
This file lists several important or useful ```linux``` and ```bash``` commands. As for the very obvious or typical ones, such as ```exit``` to leave an environment or basic SQL queries for MySQL, they will not be listed in order to prevent this document from getting too cluttered.

## Simple generic commands
- ```rm <filename>```: deletes a file
- ```rmdir <directoryname>```: deletes a directory (only) if directory is empty
- ```rmdir -rf <directoryname>```: deletes a directory and everything inside
- ```ls```: list files in current directory
- ```ls -a```: lists all files in current directory, including hidden files
- ```pwd```: print working directory (shows current path)
- ```cat <filename.txt>```: shows contents of a ```.txt``` file
- ```sudo <command>```: SuperUser DO, allows user to operate with security privileges of another user (usually root)


## ```nmap```
- ```nmap <host-ip-address>```: scans IP address for open ports
- ```-sV```: shows service version of open ports
- ```-sC```: runs default scripts, provides additional details
- ```-p-```: scans all ports (1-65535) instead of only 1000 most common ports. very slow, recommend use with ```-T5``` (see below)
- ```-T1``` to ```-T5```: speeds of sending packages, from slowest to fastest. ```-T1``` is hard to detect, while ```-T5``` is very easily detected

## ```mysql```
- ```mysql -u <username> -p```: connects to MySQL as user ```username``` and prompts for password, then leads to root environment
- ```SHOW DATABASES;```: shows all databases within the root environment
- ```SHOW TABLES;```: shows all tables within the current database
- ```USE <database_name>;```: selects a specific database within the root environment
- ```SELECT * FROM <table_name>;```: selects everything from a table
