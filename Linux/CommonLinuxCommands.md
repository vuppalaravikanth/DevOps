# List of all Linux commands commanly used

### *[Home](linux.md)*

|Command |Description/Explanation|
| :---  | :--- |
|whoami|Name of the user who logged in|
|clear|Clears the terminal|
|whatis mkdir|display one-line manual page descriptions of command mkdir|
|man mkdir|Displays the manual of commands|
|exit|exit out of terminal|
|su ravi|Switch to user ravi|
|sudo su -|Switch to root user|
|who|List of all users currently logged in to the Linux machine|
|users|Print the user names of users currently logged in to the current host|
|w|Shows who logged in and what they are doing|
|uname -a|Print system information|
|cat /etc/issue<br>lsb_release -d<br>hostnamectl<br>|OS Version|
|uptime|How long the system is running|
|useradd ravi<br>passwd ravi|Add user Ravi and Set password for ravi user|
|adduser ravi sudo|Add user ravi to the |
|sudo usermod -a -G sudo hari| Add user Hari to Sudo Group|
|groups| List of groups current user belong to|
|groups hari| List of groups user hari belong to|
|date|System Datetime|
|cut -d: -f1 /etc/passwd \| column|List all local user accounts|

## File Operations
tailf will print out the last 10 lines of the given file and then wait for this file to grow.
```
tailf fileName.txt
```

## Directory Operations

```
pwd
``` 
Print name of current/working directory<br>
```
cd ..
```
which changes to the previous working directory
```
cd dir1
```
Change to dir1
```
mkdir ravi
```
Create directory ravi
```
cd /
```
Go to dir /
```
cd 
```
Go to root directory
```
mkdir 1 2 3
```
Create 3 directories 1, 2 and 3
```
mkdir -p a/b/c/d
```
p stands for make parent directories as needed.
```
cd -
```
Go to the Previous directory









