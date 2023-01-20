# Project-2

Documentation for project 2 

#INSTALLING THE NGINX WEB SERVER

`sudo apt update`

![sudo apt update](./Images/sudo-apt-update.png)

`sudo apt install nginx`

![sudo apt install nginx](./Images/sudo-apt-install-nginx.png)

`sudo systemctl status nginx`

![sudo systemctl status nginx](./Images/sudo-systemctl-status-nginx.png)

`Public IP address`

![Public IP address](./Images/Welcome-to-nginx!.png)

# INSTALLING MYSQL

`sudo apt install mysql server`

![sudo apt install mysql server](./Images/sudo-apt-install-mysql-server.png)

`sudo mysql`

![sudo mysql](./Images/sudo-mysql.png)

`mysql database`

![mysql database](./Images/mysql-database.png)

`mysql exit`

![mysql exit](./Images/mysql-exit.png)

# INSTALLING PHP

You have Nginx installed to serve your content and MySQL installed to store and manage your data. Now you can install PHP to process code and generate dynamic content for the web server.

`sudo apt install php-fpm php-mysql`

![sudo apt install php-fpm php-mysql](./Images/sudo-apt-install-php-fpm-php-mysql.png)

  # CONFIGURING NGINX TO USE PHP PROCESSOR

  When using the Nginx web server, we can create server blocks (similar to virtual hosts in Apache) to encapsulate configuration details and host more than one domain on a single server. In this guide, we will use projectLEMP as an example domain name.

On Ubuntu 20.04, Nginx has one server block enabled by default and is configured to serve documents out of a directory at /var/www/html. While this works well for a single site, it can become difficult to manage if you are hosting multiple sites. Instead of modifying /var/www/html, we’ll create a directory structure within /var/www for the your_domain website, leaving /var/www/html in place as the default directory to be served if a client request does not match any other sites.

`sudo mkdir /var/www/projectLEMP`

![sudo mkdir /var/www/projectLEMP](./Images/sudo-mkdir-va-www-projectLEMP.png)

`sudo chown -R $USER:$USER /var/www/projectLEMP`

![sudo chown -R $USER:$USER /var/www/projectLEMP](./Images/sudo-chown-R-%24USER-%24USER%20-var-www-projectLEMP.png)

`#/etc/nginx/sites-available/projectLEMP`

![#/etc/nginx/sites-available/projectLEMP](./Images/etc-nginx-sites-available-projectLEMP.png)

`sudo nginx -t`

![sudo nginx -t](./Images/sudo-nginx-t.png)

`sudo unlink /etc/nginx/sites-enabled/default`

![sudo unlink /etc/nginx/sites-enabled/default](./Images/sudo-unlink-etc-nginx-sites-enabled-default.png)

`sudo systemctl reload nginx`

![sudo systemctl reload nginx](./Images/sudo-systemctl-reload-nginx.png)

`sudo echo 'Hello LEMP from hostname`
![sudo echo 'Hello LEMP from hostname](./Images/sudo-echo-Hello-LEMP-from-hostname.png)

# TESTING PHP WITH NGINX

LEMP stack should now be completely set up

`PHP code that will return information about your server`

![PHP code that will return information about your server](./Images/PHP-code-that-will-return-information-about-your-server.png)

`Testing PHP with Nginx public IP info php`

![Testing PHP with Nginx public IP info php](./Images/php.png)

`404 Not Found`

![404 Not Found](./Images/404-Not-Found.png)

# RETRIEVING DATA FROM MYSQL DATABASE WITH PHP (CONTINUED)

To do list" and configure access to it, so the Nginx website would be able to query data from the DB and display it

`CREATE USER`

![CREATE USER](./Images/CREATE-USER.png)

`GRANT ALL ON example_database`

![GRANT ALL ON example_database](./Images/GRANT-ALL-ON-example-database.png)

`logging in to the MySQL console`

![logging in to the MySQL console](./Images/logging-in-to-the-MySQL-console.png)

`Show Databases`

![Show Databases](./Images/SHOW-DATABASES.png)

`CREATE TABLE example_database.todo_list`

![CREATE TABLE example_database.todo_list](./Images/CREATE-TABLE-example-database.todo-list.png)

`INSERT INTO example_database.todo_list(content) VALUES`

![INSERT INTO example_database.todo_list(content) VALUES](./Images/INSERT-INTO-example_database.todo_list(content)%20VALUES.png)

`SELECT FROM example_database.todo_list`

![SELECT FROM example_database.todo_list;](./Images/SELECT-FROM-example_database.todo_list.png)

The following PHP script connects to the MySQL database and queries for the content of the todo_list table, displays the results in a list. If there is a problem with the database connection, it will throw an exception.

![`TODO`](./Images/TODO.png)








