
### *[Home](linux.md)*

## UFW - Uncomplicated Firewall

Install ufw and check status
```
root@ravi:~# sudo apt install ufw
root@ravi:~# man ufw
root@ravi:~# sudo ufw status
```
Default Configuration file
```
root@ravi:~# vim /etc/default/ufw
```
Disable and Reset
```
root@ravi:~# sudo ufw disable
root@ravi:~# sudo ufw status
root@ravi:~# sudo ufw reset
root@ravi:~# sudo ufw status
```
Add Default configuration and stop UFW
```
root@ravi:~# sudo ufw default deny incoming
root@ravi:~# sudo ufw default allow outgoing
root@ravi:~# sudo systemctl stop ufw
root@ravi:~# sudo ufw status
```
Add Rules to the Firewall
```
root@ravi:~# sudo ufw allow ssh
root@ravi:~# sudo ufw allow http
root@ravi:~# sudo ufw allow https
root@ravi:~# sudo ufw allow ftp
root@ravi:~# sudo ufw allow from 10.0.0.1
root@ravi:~# sudo ufw allow from 10.0.0.1 to any port 22
root@ravi:~# sudo ufw allow from 10.0.0.1/24 to any port 22
```
Start and Enable ufw
```
root@ravi:~# sudo systemctl start ufw
root@ravi:~# sudo ufw enable
```
Delete the Firewall Rules
```
root@ravi:~# sudo ufw status numbered
root@ravi:~# sudo ufw delete 5
root@ravi:~# sudo ufw status
root@ravi:~# sudo ufw status numbered
root@ravi:~# sudo ufw delete 8
root@ravi:~# sudo ufw status
```
