## Create Virtual Host On Ubuntu

* #### Create Virtual Host File
`sudo nano /etc/apache2/sites-available/local.domain.com.conf`

* #### Put this code
```
<VirtualHost *:80>
  DocumentRoot "/var/www/html/{projectPath}"
  ServerName local.domain.com

  <Directory /var/www/html/{projectPath}>
  AllowOverride All
  </Directory>
</VirtualHost>
```
*** if it's laravel project , refer to public folder ***
`"/var/www/html/{projectPath}/public"`

* #### Enable the new domain
`sudo a2ensite local.domain.com`

* #### Modify Hosts File * to add the domain record *
`sudo nano /etc/hosts`

* #### Add the record
`127.0.0.1  local.domain.com`

* #### Restart Apache
`sudo service apache2 restart`
