|Command |Description/Explanation|
| :---  | :--- |
|```pwd```|Print name of current/working directory|
|whoami|Name of the user who logged in|
|su ravi|Switch to user ravi|
|sudo su -|Switch to root user|
|who|List of all users currently logged in to the Linux machine|
|users|Print the user names of users currently logged in to the current host|
|w|Shows who logged in and what they are doing|
|```uname -a```|Print system information|
|```cat /etc/issue```<br>```lsb_release -d```<br>```hostnamectl```<br>|OS Version|
|uptime|How long the system is running|
|useradd ravi<br>passwd ravi|Add user Ravi and Set password for ravi user|
|adduser ravi sudo|Add user ravi to the |
|sudo usermod -a -G sudo hari| Add user Hari to Sudo Group|
|groups| List of groups current user belong to|
|groups hari| List of groups user hari belong to|
|date|System Datetime|
|cut -d: -f1 /etc/passwd \| column|List all local user accounts|
|history|List of commands executed by user|
