# Ambition & Réussite

Web application of the Ambition & Réussite association.

# Setup

## Requirements :

* Servers :
    * Apache2 server
    * MySQL server
* Tools:
    *  Nodejs (https://nodejs.org/en/download/)
    *  npm
    *  bower (https://bower.io/#install-bower)
    *  composer (https://getcomposer.org/download/)

## Server configuration

To properly serve the application, you need to create an Apache2 virtualhost

```
<VirtualHost *:80>
   DocumentRoot "[YOUR_PATH]"
   ServerName localhost
   <Directory [YOUR_PATH]>
       AllowOverride All
       Order allow,deny
       Allow from all
   </Directory>
</VirtualHost>
```

`Note: We could have use a custom server name, but for further needs (service-worker.js), localhost is important. So be sure to remove the already existing virtualhost that use localhost. Check your host file to be sure that localhost is bound`

## Install dependencies

You need to install the bower dependencies by running the __bower install__ command a the project root

```bash
    $ bower install
```

...
