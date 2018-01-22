
# NGINX

## Ubuntu Linux: Start / Restart / Stop Nginx Web Server

How do I restart / stop / start the nginx web server under a Ubuntu Linux operating systems using command line option?
The nginx web server can be restarted using any one of the following command line syntax. Use systemctl on systemd based version such as Ubuntu Linux 16.04LTS and above:

`sudo systemctl restart nginx`

OR (older Ubuntu Linux version):

`OR (older Ubuntu Linux version):`

The same commands can be used to start / stop / restart the nginx server on a Ubuntu Linux:

`sudo systemctl start nginx`

`sudo systemctl stop nginx `

`sudo systemctl restart nginx`

OR

`sudo service nginx start`

`sudo service nginx stop`

`sudo service nginx restart`

OR 

`sudo /etc/init.d/nginx start`

`sudo /etc/init.d/nginx stop`

`sudo /etc/init.d/nginx restart`


