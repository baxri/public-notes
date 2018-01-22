
# MYSQL

## Changing the MySQL root user password

If you've set the password, and want to change it to something different (hint, hint ... more challenging), you can do that. This does require that you know the current password. With that password in hand, the command to change the root user password is:

`mysqladmin -u root -p'OLDPASSWORD' password NEWPASSWORD`

In the above command, there is no space between -p and 'OLDPASSWORD'. If you put a space between them, the command will fail.
After you issue that command, you will be prompted for your sudo (or administrator) password. This is not the MySQL root user password, but the system (or sudo) admin password.

