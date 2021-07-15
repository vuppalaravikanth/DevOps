

## Locate

### *[Home](linux.md)*


Locate files by Name
```
sudo apt install mlocate
man locate
whatis locate
locate passwd
locate --all 'passwd'
locate /etc --all 'passwd'
locate "passwd" | grep "/etc/passwd"
locate resolve
locate --all "*.conf" |grep resolve
locate --all -c resolved.conf
locate --all resolved.conf
locate --all resolved.conf| grep "/etc"
locate --all -c -i Resolved.conf
```
