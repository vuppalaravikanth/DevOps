### *[Home](linux.md)*

## History

List of commands executed by user
```
history
```
Print the last 10 commands executed by user
```
history 10
history | tail -n 10
```
Execute the last command
```
!!
```
Execute the last command with Sudo Permission
```
sudo !!
```
Search for the command and use it. Go to the End of the command
```
ctrl+R, ls(previous command), Right arrow. Ctrl+e or Shift+$
```
Search the History List for Keyword sshd
```
history | grep shhd
```
Give a Space before the command, So that it will not store in the History List
```
$ echo 'Hello'
```
Clear the history List
```
history -c
```
Delete the 10th command from History
```
history -d 10
```
