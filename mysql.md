
# MYSQL

## Start, stop, restart

Example was used in ubuntu 16.04 standart instalation

`/etc/init.d/mysql start`

`/etc/init.d/mysql stop`

`/etc/init.d/mysql restart`

## Changing the MySQL root user password

If you've set the password, and want to change it to something different (hint, hint ... more challenging), you can do that. This does require that you know the current password. With that password in hand, the command to change the root user password is:

`mysqladmin -u root -p'OLDPASSWORD' password NEWPASSWORD`

In the above command, there is no space between -p and 'OLDPASSWORD'. If you put a space between them, the command will fail.
After you issue that command, you will be prompted for your sudo (or administrator) password. This is not the MySQL root user password, but the system (or sudo) admin password.

## Recover your MySQL password

What if you've forgotten your MySQL root user password? This could be quite the predicament ... had the developers not thought of that eventuality. In order to recover the password, you simply have to follow these steps:

Stop the MySQL server process with the command sudo service mysql stop
Start the MySQL server with the command

 `sudo mysqld_safe —skip-grant-tables —skip-networking`

Connect to the MySQL server as the root user with the command mysql -u root
At this point, you need to issue the following MySQL commands to reset the root password:

`mysql> use mysql;`

`​mysql> update user set authentication_string=password('NEWPASSWORD') where user='root';`

`​mysql> flush privileges;`

`​mysql> quit`

`Where NEWPASSWORD is the new password to be used.`

Restart the MySQL daemon with the command sudo service mysql restart. You should now be able to log into MySQL with the new password.

And that's it. You can now set, reset, and recover your MySQL password.

## Open mysql server for remote connections

On your database server, as a user with root privileges, open your MySQL configuration file.
To locate it, enter the following command:

`mysql --help`

On Ubuntu 16, the path is typically /etc/mysql/mysql.conf.d/mysqld.cnf.

`bind-address = <ip address of your Magento web node>`

Restart Mysql CentOS: `service mysqld restart`
Restart Mysql Ubuntu: `service mysql restart`

You may also need to open port. Examle on ubuntu.

`sudo ufw allow 3306/tcp`
`sudo service ufw restart`

