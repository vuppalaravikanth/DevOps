### *[Home](index.md)*

Install Apache
```
root@ravi:~# sudo apt update  
root@ravi:~# sudo apt install apache2 
```
Enable firewall, Allow Apache and ssh to the Firewall Rules.
```
root@ravi:~# sudo ufw enable
root@ravi:~# sudo ufw app list
root@ravi:~# sudo ufw allow ssh
root@ravi:~# sudo ufw allow 'Apache'
root@ravi:~# sudo ufw status
```
Install Net tools and get IP address of the system
```
root@ravi:~# sudo apt install net-tools
root@ravi:~# ifconfig
```
Access the Default page for the Apache http://IpAddress <br/>
Crate a cusom web site using the below commands
```
root@ravi:~# sudo mkdir /var/www/ravi.com
root@ravi:~# sudo chown -R $USER:$USER /var/www/ravi.com
root@ravi:~# ls -l /var/www
root@ravi:~# sudo chmod -R 755 /var/www/ravi.com
root@ravi:~# ls -l /var/www
root@ravi:~# vim /var/www/ravi.com/index.html
```
Create the Web page
```
<html>
        <head>
                <title>
                        Apache
                </title>
        </head>
        <body>
                <h1>
                        Welcome to Apache
                </h1>
        </body>
</html>
```
Create the configuration file for the site.
```
root@ravi:~# vim /etc/apache2/sites-available/ravi.com.conf

<VirtualHost *:80>
        ServerAdmin webmaster@localhost
        ServerName ravi.com
        ServerAlias www.ravi.com
        DocumentRoot /var/www/ravi.com
        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```
Enable the ravi.com custom page and disable the default site.
```
root@ravi:~# sudo a2ensite ravi.com.conf
root@ravi:~# sudo a2dissite 000-default.conf
root@ravi:~# sudo systemctl restart apache2
root@ravi:~# sudo apache2ctl configtest
```
Access the web page using the address http://IpAddress

Access Error and access logs for the Apache
```
root@ravi:~# cat /var/log/apache2/access.log
root@ravi:~# cat /var/log/apache2/error.log
```

|Command |Description/Explanation|
| :---  | :--- |
|80|Default Non Secure port for Apache web server|
|443|Default Secure port for Apache web server|
|/etc/apache2|ServerRoot|
|/var/log/apache2/error.log|Error Log|
|/var/log/apache2/access.log|Access Log|
|/var/www/html/index.html|Default Web page|
|/etc/httpd/conf|Default configuratino file for RPM or Red Hat Server|
|/etc/apache2/apache2.conf|Default configuration file for Derbian linux or Ubuntu|


