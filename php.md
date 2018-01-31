
## How to Install Different PHP (5.6, 7.0 and 7.1) Versions in Ubuntu

First start by adding Ondřej Surý PPA to install different versions of PHP – PHP 5.6, PHP 7.0 and PHP 7.1 on Ubuntu system.

`sudo apt install python-software-properties`

`sudo add-apt-repository ppa:ondrej/php`

2. Next, update the system as follows.

`sudo apt-get update`

3. Now install different supported versions of PHP as follows.

### For Apache Web Server

`sudo apt install php5.6   [PHP 5.6]`

`sudo apt install php7.0   [PHP 7.0]`

`sudo apt install php7.1   [PHP 7.1]`

### For Nginx Web Server

`sudo apt install php5.6-fpm   [PHP 5.6]`

`sudo apt install php7.0-fpm   [PHP 7.0]`

`sudo apt install php7.1-fpm   [PHP 7.1]`

4. To install any PHP modules, simply specify the PHP version and use the auto-completion functionality to view all modules as follows.

`------------ press Tab key for auto-completion ------------ `

`sudo apt install php5.6`

`sudo apt install php7.0`

`sudo apt install php7.1`


5. Now you can install most required PHP modules from the list.

`sudo apt install php5.6-cli php5.6-xml php5.6-mysql`

`sudo apt install php7.0-cli php7.0-xml php7.0-mysql `

`sudo apt install php7.1-cli php7.1-xml php7.1-mysql`

6. Finally, verify your default PHP version used on your system like this.

`php -v `

## Set Default PHP Version in Ubuntu

`sudo update-alternatives --set php /usr/bin/php5.6`

`sudo update-alternatives --set php /usr/bin/php7.0`

`sudo update-alternatives --set php /usr/bin/php7.1`

8. To set the PHP version that will work with Apache web server, use the commands below. First disable the current version with the a2dismod command and then enable the one you want with the a2enmod command.

`sudo a2dismod php7.0`

`sudo a2enmod php7.1`

`sudo systemctl restart apache2`

9. After switching from one version to another, you can find your PHP configuration file, by running the command below.

`sudo update-alternatives --set php /usr/bin/php7.1`

`php -i | grep "Loaded Configuration File"`




















