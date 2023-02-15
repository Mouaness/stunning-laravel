<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

Answers:

1-)Sudo is used to run a command as a superuser or administrator,
allowing you to perform tasks that require elevated permissions.
For example, you might use the "sudo" command to install software, configure the system, or access files that are protected.

2-)apt-get is used to manage packages, including installation, upgrading, and removal of packages.
The "apt-get" command works by using a database of packages that are available from repositories specified in the system's software sources.

3-)curl error This error message suggests that there is an issue with the syntax of the command. 
The problem may be with the options --installdir and --filename not being properly formatted.

4-)sudo chgrp -R www-data storage bootstrap/cache
The command "sudo chgrp -R www-data storage bootstrap/cache" in Ubuntu means to change the group ownership of the "storage", "bootstrap/cache" directories and all of
their subdirectories recursively (-R option) to the group "www-data". The "sudo" at the beginning of the command grants administrative privileges, allowing the change
of group ownership, which is normally a privileged action.

5-)sudo chmod -R ug+rwx storage bootstrap/cache
"sudo chmod -R ug+rwx storage bootstrap/cache" is a command in the Ubuntu operating system that changes the file permissions for the "storage" and "bootstrap/cache"
directories.
The "chmod" command is used to change the permissions on a file or directory. The "-R" option tells the command to operate recursively, meaning it will change the
permissions on the directory and all of its contents.
The "ug+rwx" portion of the command specifies the permissions to be set. "u" refers to the owner of the file, "g" refers to the group owner, and "rwx" refers to the
read, write, and execute permissions. The "+" sign tells the command to add these permissions to the existing permissions, rather than replace them.

Checkpoint 1:

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

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains over 1500 video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the Laravel [Patreon page](https://patreon.com/taylorotwell).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Cubet Techno Labs](https://cubettech.com)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[Many](https://www.many.co.uk)**
- **[Webdock, Fast VPS Hosting](https://www.webdock.io/en)**
- **[DevSquad](https://devsquad.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[OP.GG](https://op.gg)**
- **[WebReinvent](https://webreinvent.com/?utm_source=laravel&utm_medium=github&utm_campaign=patreon-sponsors)**
- **[Lendio](https://lendio.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
