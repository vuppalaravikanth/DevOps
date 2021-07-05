# File Operations

### *[Home](linux.md)*

Print file Contents 

```
cat file.txt
```
Print complete file on the screen
```
head -10 file.txt
```
Print first 10 lines from the file

```
tail -10 file.txt
tail -10 file.txt |grep tom
```
Print last 10 lines from the file, In the second command line it searches for word tom.
```
tailf file.txt
xtail file.txt
tail -f file.txt
```
the above commands will  print out the last 10 lines of a file and then wait for the file to grow, Again prints the growing lines.


