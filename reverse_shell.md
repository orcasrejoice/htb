# Description
This file describes how to upgrade a non-interactive shell (reverse shell) to a fully interactive one.
### How do I know if I'm in a non-interactive shell?
You're probably in an interactive shell if you've tried to execute a MySQL prompt and the program froze.

# Upgrade your shell
1. ```python3 -c 'import pty; pty.spawn("/bin/bash")'```
2. ```stty raw -echo; fg```
3. ```script /dev/null -c bash```
