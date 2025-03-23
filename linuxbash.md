# Description
This file lists several important or useful ```linux``` and ```bash``` commands. As for the very obvious or typical ones, such as ```exit```, ```-h```, ```man```, or basic SQL queries for MySQL, they will not be listed in order to prevent this document from getting too cluttered.

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
- ```grep <pattern> <filename>```: search for a pattern in a file (see more on ```grep``` below)
- ```wc <filename>```: count characters, words, and lines in a file
- ```nano <new_filename>```: create new file and open ```nano``` in-shell editor
### Networking
- ```ping <host_ipaddress>```: ping IP address for package delivery and response, checks if machine is up
- ```wget <url>```: download files from the web
- ```netstat```: show network connections, routing tables, and interface stats
- ```curl <url>```: transfer data from or to a server. useful for logins.
  - ```curl -X POST <host_ipaddress> -d <"username=admin&password=admin123">```: logs in to IP address with credentials ```admin``` and ```admin123```
  - ```-c cookies.txt```: save cookies to ```cookies.txt``` if authentication succeeds
  - ```ipconfig```: display or config IP settings for network interfaces
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
- ```chown <user>:<group> <file/dir>```: change owner of file or directory
- ```sudo <command>```: SuperUser DO, allow user to operate with security privileges of another user (usually root)
### More ```grep``` commands
- ```grep "<word>" <filename.txt>```: search for ```"word"``` in file
- ```-i```: search case-insensitively
- ```-l```: list file names only
- ```-n```: show line numbers of matches
- ```-o```: show matched word only instead of full line
- ```-w```: match whole words only
- ```-v```: exclude results with ```"word"```
- ```-rI```: exlude binary files
- ```-P```: use Perl-compatible regex for advanced pattern searching
- ```-E```: use for extended regex
- ```-E "<word1>|<word2>|<word3>"```: search for ```"word1"```, ```"word2"```, or ```"word3"```
- ```grep "<word>" *.<file_extension>```: search all ```.<file_extentension>``` files for ```"word"```
- ```grep "^<word>" <filename.txt>```: find lines starting with ```"word"```
- ```grep "<word>$" <filename.txt>```: find lines ending with ```"word"```
- ```grep -r "<word>" /dir1/dir2```: search for ```"word"``` in all files in ```/dir1/dir2``` (```-r```: recursive search)
- ``` | grep "<word>"```: filter results for ```"word"``` (use after command in bash/Linux)
- ```--color=auto```: highlight matches in color
### Miscellaneous
- ```history```: show command history
- ```man <command>```: show the manual for a command
- ```clear```: clear the terminal screen (or press ```Ctrl + L```)
- ```echo $variable```: capture and print value of variable
    - e.g. ```echo $MAIL```: prints something like ```/var/mail/username```
- ```uname```: a command for displaying system information. use ```man uname``` to see usage
