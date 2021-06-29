# File Permissions and Attributes

### *[Linux](linux.md)*

### File/Directory Listing Information
Special designation = - for file, d for directory<br/>
Permissions = rwx for owner, rwx for group, rwx for others<br/>
owner = the name of the user that owns the file/directory<br/>
group = the name of the group that has permissions on the file/directory<br/>

![image](https://user-images.githubusercontent.com/1942588/123860950-934f4e00-d8f4-11eb-9da8-4a9e869afacd.png)


| Number | Permission Type | Symbol |Binary Number|
| :---  | :---: | ---: |---:
| 4 | Read| r--|100|
| 2 | Write| -w-|010|
| 1 | Execute| --x|001|

|Number |Permission Type |Symbol|Binary Number|
| :---  | :---: | ---: | ---: |
|0 |No Permission| ---|000|
|1 |Execute| --x|001|
|2 |Write |-w-|010|
|3 |Execute + Write| -wx|011|
|4 |Read| r--|100|
|5 |Read + Execute| r-x|101|
|6 |Read +Write| rw-|110|
|7 |Read + Write +Execute| rwx|111|

### chown - change owner
Changing owner of the file abc.txt to hari
```
chown hari Ravali.txt
```
Changing owner and group to hari for the file Ravali.txt
```
chown hari:hari Ravali.txt
```
Changing the group and owner to Hari for the file Ravali.txt. 1001 id is mapped to user Hari, This mapping can be found in /etc/passwd file.
```
chown 1001:1001 Ravali.txt
```
### chgrp - change group
```
chgrp ravi a.txt
```
### chmod - change file mode bits
```
chmod u+x file.txt   Gves the user owner execute permissions.
chmod g-r file.txt   Removes the group read permissions
chmod o-r file.txt   Removes the others read permission
chmod a+w file.txt   Gives all of them the write permission
chmod +x file.txt    Gives all of them the execute permission
chmod u=rw file.txt  Gives user read and write permissions
chmod u=rw,g=rw,o=r file.txt  combination of permissions for file.
chmod u=rwx,ug+rw,o=r file.txt fishy combinations are also accepted
```

### chmod - Setting octal permissions

In this mode, file permissions are not represented as characters. 4 is Read, 2 is Write and 1 is execute. By adding thse numbers we change the file and directory permissions.<br>

![image](https://user-images.githubusercontent.com/1942588/123878848-dbc73580-d90d-11eb-85a7-3fb82288a8a7.png)

'764' absolute code says the following<br>
● Owner can read, write and execute<br>
● Usergroup can read and write<br>
● World can only read<br>
```
chmod 777 file.txt  results in rwxrwxrwx
chmod 664 file.txt  results in rw-rw-r--
chmod 750 file.txt  results in rwxr-x---
chmod 755 file.txt  results in rwx-r-xr-x
chmod 666 file.txt  results in rw-rw-rw-
chmod 700 file.txt  results in rwx------
chmod 000 file.txt  results in  ---------
chmod 755 *   results in rwxr-xr-x for all the files in folder.
```
06.51


*[Linux](linux.md)*

