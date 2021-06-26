19 UNIX Interview Questions
1.What OS are you running
uname
2.What is your kernel version
uname -r
3.For how long your machine is running
uptime
4.How many users are logged on to your system
w
5.What is user "shekhar" doing now
w|grep shekhar
6.When did user rohit logged in
w|grep rohit
7.From which machine user prakash has logged in
who|grep prakash
8.what is the login shell of user roshan
cat /etc/passwd|grep roshan|cut -d":" -f7
9.What is the home directory of user prakash
cat /etc/passwd|grep roshan|cut -d":" -f6
10.How many users do not have bash shell assigned to them
cat /etc/passwd|grep -v /bin/bash|wc -l
11.Create an alias named i to display ip address of your machine. Make is parmanent.
vim .bash_profile
alias i='ifconfig'
:wq
12.What group/s do you belong to
groups
13.What group/s are assigned to shekhar
groups shekhar
14.What are the last 10 commands that you have executed
tail .bash_history
15.How many times you have executed cd command receltly
cat .bash_history|grep cd
16.Can you read a file named /etc/fstab.
yes (but can't write to this file)
17.Can user shekhar read the same file
yes
18.Do you have the permission to modify /etc/sysctl.conf file. Who can modify it.
no.only root user.
19.How much of RAM do you have on your machine
free -m
20.What is the size of your swap
free -m|grep -i swap
21.How many processes are currently running (not sleeping)
top
22.Which process is taking the maximum CPU
top
23.Which process is taking the maximum memory
top
24.When I type ifconfig command I get the error message "command not found". What is the
problem and how can I solve it permaneltly.
--if normal user is not having permission of running ifconfig command.can solved by making
entry
in /etc/sudoers file by root user
--or if permission is there but path is not fount then set the path for ifonfig command
ex-- PATH=$PATH:/sbin/ifconfig
25.Is oracle running on your server
ps -ef|grep oracle
26.How many oracle databases are running on the server
27.How can you change the default permissions of a file to r--r--r when the file gets created
by using umask command
ex:umask 0222
28.What is the current date on your system
date +%D
29.What is the current time on your system
date +%T
30.How to find out the time required to run a specific command
time command
30. Find out all files in /tmp directory whose owner is shekhar
find /tmp -user shekhar
31.Find out all files older than 30 days whose extension is log and delete them - in one
command
Vi Questions
a. Go to the end of the file
G
b. GO to the begining of the file
gg or :1 enter
c. Find a word "tom" and replace it by "dick"
:1 $s/tom/dick/g
d. How to undo any mistake
ESC u
e. How to quit the file without saving and discard changes that you have made
q!
f. How to copy 30 lines and paste at the very begining
30 yy
ESC gg
p
