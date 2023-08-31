# ![php](https://img.shields.io/badge/Php-8993BE?style=for-the-badge&logo=php&logoColor=white) E-Shop Website
E-shop web application built using php routing. Instead of relying on the web server to map the request path to a file, all requests are forwarded to [index.php](/src/index.php) which has defined routes and callbacks registered to each route. If the request URI is a valid route, the callback returns a page to the user else, redirected to the 404 page.

## Features
- Login and registration system
- Password reset
- Ordering system
- Update profile
- Order history
- CSRF protection
- Input sanitisation

    #### Admin Panel
- Create, modify and delete products, customers and faq
- Unlimited product pictures
- Image compression ([php_gd](https://php.net/manual/en/book.image.php)): 50%
- Image magic bytes verification
- Create or select product category
- Last 7 days sales and revenue stats using Chartjs
- Modify contact details and privacy policy

## Setup
- Create Virtual Host on your local Machine
- Create database
- Execute [db-settings.sql](src/db-settings.sql)
- Enter database config [db.php](src/views/db.php)
- Enable the php_gd/gd extension in php.ini

## Host File Entry
```
127.0.0.1 local.eshop.com
```

## Virtual Host Entry
```
<VirtualHost local.eshop.com:80>
     ServerAdmin tansheetalitaj@gmail.com
     DocumentRoot "C:/xampp/htdocs/eshop"
  DirectoryIndex index.php

     ServerName local.eshop.com
     ServerAlias local.eshop.com
  <Directory "C:/xampp/htdocs/eshop">
        Options All
        AllowOverride All
        Require all granted
 </Directory>
</VirtualHost>
```

## Admin Credentials
```
uri: /admin/login
username: admin
password: 123456
```
