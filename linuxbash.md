# Description
This file lists several important or useful ```linux``` and ```bash``` commands. As for the very obvious or typical ones, such as ```exit``` to leave an environment or basic SQL queries for MySQL, they will not be listed in order to prevent this document from getting too cluttered.

# Simple generic commands
### Directories and files
- ```cd <dir_name>```: change directory
- ```rm <filename>```: delete (removes) a file
- ```rmdir <directoryname>```: delete a directory (only) if directory is empty
- ```rmdir -rf <directoryname>```: delete a directory and everything inside
- ```ls```: list files in current directory
- ```ls -a```: list all files in current directory, including hidden files
- ```pwd```: print working directory (shows current path)
- ```cp <source> <destination>```: copy files or directory
### File contents
- ```cat <filename>```: concatenate and display contents of a file
- ```grep <pattern> <filename>```: search for a pattern in a file
- ```wc <filename>```: count characters, words, and lines in a file
### Networking
- ```ping <host_ipaddress>```: ping IP address for package delivery and response, checks if machine is up
- ```wget <url>```: download files from the web
- ```netstat```: show network connections, routing tables, and interface stats
- ```curl <url>```: transfer data from or to a server
### Process management
- ```kill <PID>```: kill a process by its PID
- ```bg```: resume a suspended process in the background
- ```fg <process_number>```: bring a background job to the foreground, use process number only if multiple are running in background
- ```jobs```: list all background jobs
- ```ps```: display information about running processes
- press ```Ctrl + Z```: suspend a process
- press ```Ctrl + C```: cancel/stop a process
### Package management
- ```apt update```: update package lists for upgrades
- ```apt upgrade```: upgrade all installed packages
- ```apt install <package>```: install a package
- ```apt remove <package>```: removes a package
### Archives
- ```tar -cvf <archive.tar> <dir>```: creates a tarball archive
- ```tar -xvf <archive.tar>```: extract a tarball archive
- ```zip <archive.zip> <files>```: create a zip archive
- ```unzip <archive.zip>```: extract a zip archive
### User and group management
- ```whoami```: display the current user
- ```useradd <username>```: add a new user
- ```usermod <username>```: modify a user account
- ```userdel <username>```: delete a user account
- ```groupadd <groupname>```: create a new group
- ```passwd <username>```: change user password
- ```sudo <command>```: SuperUser DO, allow user to operate with security privileges of another user (usually root)
### Miscellaneous
- ```history```: show command history
- ```man <command>```: show the manual for a command
- ```clear```: clear the terminal screen (or press ```Ctrl + L```)

# ```nmap```
- ```nmap <host-ip-address>```: scan IP address for open ports
- ```-sV```: show service version of open ports
- ```-sC```: run default scripts, provides additional details
- ```-p-```: scan all ports (1-65535) instead of only 1000 most common ports. very slow, recommend use with ```-T5``` (see below)
- ```-T1``` to ```-T5```: speed of sending packages, from slowest to fastest. ```-T1``` is hard to detect, while ```-T5``` is very easily detected

# ```mysql```
- ```mysql -u <username> -p```: connect to MySQL as user ```username``` and prompts for password, then leads to root environment
- ```SHOW DATABASES;```: show all databases within the root environment
- ```SHOW TABLES;```: show all tables within the current database
- ```USE <database_name>;```: select a specific database within the root environment
- ```SELECT * FROM <table_name>;```: select everything from a table
