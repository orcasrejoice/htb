# Description
Everything I know about ```Microsoft SQL```.

### Check if ```xp_cmdshell``` is enabled
1. ```EXEC sp_configure 'show advanced options', 1;```
2. ```RECONFIGURE;```
3. ```EXEC sp_configure 'xp_cmdshell';```
### Enabled ```xp_cmdshell``` (requires admin privileges)
1. ```EXEC sp_configure 'xp_cmdshell', 1;```
2. ```RECONFIGURE;```
### Search for a file
1. ```EXEC xp_cmdshell 'dir C:\ /s /b | findstr <filename.txt>';```
