### 19 UNIX Interview Questions<br>
1.What OS are you running<br>
```
uname<br>
```
2.What is your kernel version<br>
```
uname -r<br>
```
3.For how long your machine is running<br>
```
uptime<br>
```
4.How many users are logged on to your system<br>
```
w<br>
```
5.What is user "shekhar" doing now<br>
```
w|grep shekhar<br>
```
6.When did user rohit logged in<br>
```
w|grep rohit<br>
```
7.From which machine user prakash has logged in<br>
```
who|grep prakash<br>
```
8.what is the login shell of user roshan<br>
```
cat /etc/passwd|grep roshan|cut -d":" -f7<br>
```
9.What is the home directory of user prakash<br>
```
cat /etc/passwd|grep roshan|cut -d":" -f6<br>
```
10.How many users do not have bash shell assigned to them<br>
```
cat /etc/passwd|grep -v /bin/bash|wc -l<br>
```
11.Create an alias named i to display ip address of your machine. Make is parmanent.<br>
```
vim .bash_profile<br>
alias i='ifconfig'<br>
:wq<br>
```
12.What group/s do you belong to<br>
```
groups<br>
```
13.What group/s are assigned to shekhar<br>
```
groups shekhar<br>
```
14.What are the last 10 commands that you have executed<br>
```
tail .bash_history<br>
```
15.How many times you have executed cd command receltly<br>
```
cat .bash_history|grep cd<br>
```
16.Can you read a file named /etc/fstab.<br>
```
yes (but can't write to this file)<br>
```
17.Can user shekhar read the same file<br>
```
yes<br>
```
18.Do you have the permission to modify /etc/sysctl.conf file. Who can modify it.<br>
no.only root user.<br>
19.How much of RAM do you have on your machine<br>
```
free -m<br>
```
20.What is the size of your swap<br>
```
free -m|grep -i swap<br>
```
21.How many processes are currently running (not sleeping)<br>
```
top<br>
```
22.Which process is taking the maximum CPU<br>
```
top<br>
```
23.Which process is taking the maximum memory<br>
```
top<br>
```
24.When I type ifconfig command I get the error message "command not found". What is the<br>
problem and how can I solve it permaneltly.<br>
--if normal user is not having permission of running ifconfig command.can solved by making<br>
entry<br>
in /etc/sudoers file by root user<br>
--or if permission is there but path is not fount then set the path for ifonfig command<br>
ex-- PATH=$PATH:/sbin/ifconfig<br>
25.Is oracle running on your server<br>
```
ps -ef|grep oracle<br>
```
26.How many oracle databases are running on the server<br>
27.How can you change the default permissions of a file to r--r--r when the file gets created<br>
by using umask command<br>
ex:umask 0222<br>
28.What is the current date on your system<br>
```
date +%D<br>
```
29.What is the current time on your system<br>
date +%T<br>
30.How to find out the time required to run a specific command<br>
time command<br>
30. Find out all files in /tmp directory whose owner is shekhar<br>
find /tmp -user shekhar<br>
31.Find out all files older than 30 days whose extension is log and delete them - in one<br>
command<br>
Vi Questions<br>
a. Go to the end of the file<br>
G<br>
b. GO to the begining of the file<br>
gg or :1 enter<br>
c. Find a word "tom" and replace it by "dick"<br>
:1 $s/tom/dick/g<br>
d. How to undo any mistake<br>
ESC u<br>
e. How to quit the file without saving and discard changes that you have made<br>
q!<br>
f. How to copy 30 lines and paste at the very begining<br>
30 yy<br>
ESC gg<br>
p<br>
