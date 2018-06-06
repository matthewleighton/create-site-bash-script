
# createsite

A short script to work with Apache2, creating a local directory, virtual host, and modifying your /etc/hosts file.
Build for use with Ubuntu 18.04.

(Created for personal use/time saving. Only tested on my own setup).

## Installing

Place the createsite file in a location within your PATH.
I've done this in ~/bin, and included this in my PATH with the following line in ~/.bashrc:
```
export PATH=$PATH":$HOME/bin"
```

## Usage
From the command line run:
```
createsite example.com
```
This will:

- Create the directory /var/www/example.com
- Set the directory's ownership to the current user
- Create the site's .conf file at /etc/apache2/sites-available/example.com.conf
- Enable the site in Apache via a2ensite example.com
- Restart Apache
- Add the site to your /etc/hosts file with the following line:
 ```
127.0.0.1		local.example.com
 ```
 