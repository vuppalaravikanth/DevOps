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

## History
|Command |Description/Explanation|
| :---  | :--- |
|history|List of commands executed by user|
|history 10<br>history \| tail -n 10|Print the last 10 commands executed by user|
|!!|Execute the last command|
|sudo !!|Execute the last command with Sudo Permission|
|ctrl+R, ls(previous command), Right arrow|Search for the command and use it|
|history \| grep shhd|Search the History List for Keyword sshd|
| echo 'Hello'|Give a Space before the command, So that it will not store in the History List|
|history -c|Clear the history List|
|history -d 10|Delete the 10th command from History|

## File Operations
|Command |Description/Explanation|
| :---  | :--- |
|tailf fileName.txt|tailf will print out the last 10 lines of the given file and then wait for this file to grow.|

## Directory Operations
|Command |Description/Explanation|
| :---  | :--- |
|pwd|Print name of current/working directory|
|cd ..|which changes to the previous working directory|
|cd dir1|Change to dir1|
|mkdir ravi|Create directory ravi|
|cd /|Go to dir /|
|cd |Go to root directory|
|mkdir 1 2 3|Create 3 directories 1, 2 and 3|






