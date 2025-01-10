## Create user "rose" with uid 1522 and designate the home directory as /var/www/rose
### UID stands for user identifier. It is a unique numerical value assigned to each user account. The system uses it to identify and differentiate between different user.
### The /etc/passwd file stores user account information. This file contains a list of all user accounts on the system, along with their corresponding UIDs, group IDs, home directories and login shells.
```
sudo cat /etc/passwd
```
## How to find the UID of a user, Group, or an account
```
id -u username
```
## Change the UID of a user in Linux
```
sudo usermod -u new_uid username
```
## Create a new user with a specific UID
```
sudo useradd -u uid username
```
## Set a password to the created user
```
sudo passwd username
```
### To designate a home directory in linux, you can use useradd or usermod command
## Create a home directory for a new user
```
useradd -m username
```
## Create a home directory for existing user
```
sudo usermod -m -d /home/new_directory username
```
## Change the home directory for an existing user
```
usermod -d /path/to/dir username
```
## Verify the home directory
```
grep username /etc/passwd
```
