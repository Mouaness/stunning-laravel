Answers:
1-)Sudo is used to run a command as a superuser or administrator, 
allowing you to perform tasks that require elevated permissions.
For example, you might use the "sudo" command to install software, configure the system, or access files that are protected.

2-)apt-get is used to manage packages, including installation, upgrading, and removal of packages.
The "apt-get" command works by using a database of packages that are available from repositories specified in the system's software sources.

3-)curl error This error message suggests that there is an issue with the syntax of the command. The problem may be with the options --installdir and --filename not being properly formatted.

4-)sudo chgrp -R www-data storage bootstrap/cache
The command "sudo chgrp -R www-data storage bootstrap/cache" in Ubuntu means to change the group ownership of the "storage", "bootstrap/cache" directories and all of their subdirectories recursively (-R option) to the group "www-data". The "sudo" at the beginning of the command grants administrative privileges, allowing the change of group ownership, which is normally a privileged action.

5-)sudo chmod -R ug+rwx storage bootstrap/cache
"sudo chmod -R ug+rwx storage bootstrap/cache" is a command in the Ubuntu operating system that changes the file permissions for the "storage" and "bootstrap/cache" directories.
The "chmod" command is used to change the permissions on a file or directory. The "-R" option tells the command to operate recursively, meaning it will change the permissions on the directory and all of its contents.
The "ug+rwx" portion of the command specifies the permissions to be set. "u" refers to the owner of the file, "g" refers to the group owner, and "rwx" refers to the read, write, and execute permissions. The "+" sign tells the command to add these permissions to the existing permissions, rather than replace them.

Checkpoint 1
sudo apt-get update
sudo apt-get install apache2
sudo apt-get install mysql-server
sudo apt-get install php-mysql
sudo apt-get install php
sudo apt-get install libapache2-mod-php
sudo apt-get install php-mcrypt
sudo apt-get install php-pear
sudo apt-get install curl
sudo apt-get install php-curl
sudo apt-get install php-cli
sudo apt-get install git
sudo a2enmod rewrite
sudo systemctl restart apache2

Checkpoint 2:
cd /var/www/html
pwd
sudo git clone repositoy-url

Checkpoint 3:
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
sudo composer install

Checkpoint 4:
pwd sudo cp .env.example .env sudo vim .env (change APP_NAME)
php artisan key:generate

Checkpoint 5:
which apache2
cd /etc/apache2
sudo nano apache2.conf
Add the following lines to “apache2.conf”: " <Directory /var/www/html/repositoy-name/public> Options Indexes FollowSymLinks AllowOverride all Require all granted "
cd sites-enabled sudo nano 000-default.conf
" Add the following lines to “000-default.conf”, under the line “<VirtualHost *:80>” ServerAdmin webmaster@localhost DocumentRoot /var/www/html/repositoy-name/public/"
sudo service apache2 restart

Checkpoint 6:
sudo chgrp -R www-data storage bootstrap/cache
sudo chmod -R ug+rwx storage bootstrap/cache
