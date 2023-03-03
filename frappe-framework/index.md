# Frappe Framework

## Inrodution

Frappe, pronounced fra-pay, is a full stack, batteries-included, web framework written in Python and Javascript with MariaDB as the database. It is the framework which powers ERPNext, is pretty generic and can be used to build database driven apps.

## Why Frappe?

The key difference in Frappe compared to other frameworks is that meta-data is also treated as data. This enables you to build front-ends very easily. We believe in a monolithic architecture, so Frappe comes with almost everything you need to build a modern web application. It has a full featured Admin UI called the Desk that handles forms, navigation, lists, menus, permissions, file attachment and much more out of the box.

## Rapid Application Development

After setting up Frappe Framework, you can be productive in no time. Creating models, wiring controller code and updating views are all handled by the framework.

## Easy Deployment

Bench is the all-in-one tool to manage all things Frappe. It handles app updates, database migrations, generating configs for nginx and supervisor, scaffolding new apps and much more.

## Extensible architecture

Build powerful extensions on top of Frappe by creating your own apps. Apps can bring their own models or modify existing ones in Frappe.

---

## Prerequisites Frappe Framework

Before we can start with Frappe, be sure you understand the stack it's built on.

### (1.) Python

Frappe uses Python 3 for server-side programming. It is highly recommended to learn Python before you start building apps with Frappe Framework.

### (2.)MariaDB

To create database-driven apps with Frappe, you must understand the basics of database management and common SQL queries.

### (3.)HTML/CSS

If you want to build user interfaces using Frappe Framework, you will need to learn basic HTML / CSS and the Bootstrap CSS Framework.

### (4.) JavaScript / jQuery

To customize forms and create interactive user interfaces, you will have to learn JavaScript and the library jQuery.

### (5.) Jinja Templating

For building Web Views and Print Templates, you will have to learn the Jinja Templating language.

### (6.) Git / GitHub

Learn how to contribute to an open source project using Git and GitHub, two great tools to help you manage your code and share it with others.

---

## Installation

Before you can use Frappe, you need to install it. We have a complete installation guide which covers all possibilities, this guide will also help you understand the backend stack.

## System Requirements

This guide assumes you are using a personal computer, VPS or a bare-metal server. You also need to be on a *nix system, so any Linux Distribution and MacOS is supported. However, we officially support only the following distributions.

(1.) MacOS

(2.) Desbian/Ubuntu

``` bash
1. python 3.10+ (v14)

2. Node.js 1RR6

3. Redis

4. MariaDB 10.6.6+ / Postgres v12 to v14

5. yarn 1.12+

6. pip 20+

7. wkhtmltopdf (version 0.12.5 with patched qt)

```

# Installtion process in Debian / Ubuntu

## Install git, python, and redis

```bash
sudo apt install git python-dev 
python-pip redis-server
````

## Install MariaDB

```bash
sudo apt install software-properties-common
```

If you are on Ubuntu version older than 20.04, run this before installing MariaDB:

```bash
sudo apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8
sudo add-apt-repository 'deb [arch=amd64,i386,ppc64el] http://ftp.ubuntu-tw.org/mirror/mariadb/repo/10.3/ubuntu xenial main'
```

If you are on version Ubuntu 20.04, then MariaDB is available in default repo and you can directly run the below commands to install it:

```bash
sudo apt-get update
sudo apt-get install mariadb-server
```

During this installation you'll be prompted to set the MySQL root password. If you are not prompted, you'll have to initialize the MySQL server setup yourself. You can do that by running the command:

```bash
mysql_secure_installation
```

Remember: only run it if you're not prompted the password during setup.

It is really important that you remember this password, since it'll be useful later on. You'll also need the MySQL database development files.

```bash
apt-get install mariadb-client-10.3
```

Now, edit the MariaDB configuration file.

```bash
nano /etc/mysql/my.cnf
```

And add this configuration

```bash
[mysqld]
character-set-client-handshake = FALSE
character-set-server = utf8mb4
collation-server = utf8mb4_unicode_ci

[mysql]
default-character-set = utf8mb4
```

Now, just restart the mysql service and you are good to go.

```bash
service mysql restart
```

## Install Node

We recommend installing node using nvm

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```

After nvm is installed, you may have to close your terminal and open another one. Now run the following command to install node.

nvm install 14
Verify the installation, by running:

```bash
node -v
# output
v14.17.2
```

## Finally, install yarn using npm

```bash
npm install -g yarn
Install wkhtmltopdf
```

## Install wkhtmltopdf

```bash
apt-get install xvfb libfontconfig wkhtmltopdf
```

## Install Bench CLI

Install bench via pip3

```bash
pip3 install frappe-bench
```

Confirm the bench installation by checking version

```bash
bench --version
# output
5.2.1
```
