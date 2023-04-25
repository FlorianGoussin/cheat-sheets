# PHP cheat sheet
Assuming the desired PHP version is already installed on the server.

## Set current PHP version

Set PHP version
```linux
sudo a2dismod php<old-php-version-number>
sudo a2enmod php<new-php-version-number>
sudo service apache2 restart
```

Apache 2 commands:
```linux
sudo systemctl restart apache2
```

OR

```linux
sudo service apache2 start
sudo service apache2 stop
sudo service apache2 restart
```
