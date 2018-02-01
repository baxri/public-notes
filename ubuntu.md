
#Ubuntu

## User Management

To add a user account, use the following syntax, and follow the prompts to give the account a password and identifiable characteristics, such as a full name, phone number, etc.

`sudo adduser username`

To delete a user account and its primary group, use the following syntax:

`sudo deluser username`

specify home directory when creating a user in linux:

`sudo adduser --home /home/username username`

we may need also this:

`sudo chown -R group:username /home/username/`

To add a user to a group, use the following syntax:

`sudo adduser username groupname`

To add or delete a personalized group, use the following syntax, respectively:

`sudo addgroup groupname`
`sudo delgroup groupname`

Get User and groyp list:

`compgen -u`
`compgen -g`

Get users by froyp name

`getent group group-name`

