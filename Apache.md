root@ravi:~# sudo apt update  
root@ravi:~# sudo apt install apache2


root@ravi:~# sudo ufw enable
root@ravi:~# sudo ufw app list
root@ravi:~# sudo ufw allow ssh
root@ravi:~# sudo ufw allow 'Apache'
root@ravi:~# sudo ufw status

root@ravi:~# sudo mkdir /var/www/ravi.com
root@ravi:~# sudo chown -R $USER:$USER /var/www/ravi.com
root@ravi:~# ls -l /var/www
root@ravi:~# sudo chmod -R 755 /var/www/ravi.com
root@ravi:~# ls -l /var/www
root@ravi:~# vim /var/www/ravi.com/index.html


<html>
        <head>
                <title>
                        Beautiful
                </title>
        </head>
        <body>
                <h1>
                        Hello Beautiful, How are you doing
                </h1>
        </body>
</html>

root@ravi:~# vim /etc/apache2/sites-available/ravi.com.conf

<VirtualHost *:80>
        ServerAdmin webmaster@localhost
        ServerName ravi.com
        ServerAlias www.ravi.com
        DocumentRoot /var/www/ravi.com
        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>


root@ravi:~# sudo a2ensite ravi.com.conf
root@ravi:~# sudo a2dissite 000-default.conf
root@ravi:~# sudo systemctl restart apache2
root@ravi:~# sudo apache2ctl configtest

root@ravi:~# sudo apt install net-tools
root@ravi:~# ifconfig

http://IpAddress


root@ravi:~# cat /var/log/apache2/access.log
root@ravi:~# cat /var/log/apache2/error.log

