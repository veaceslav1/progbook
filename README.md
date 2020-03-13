# Programming Book

Notes on how to develop programs based on APIs.

# Tools

This guide if focused on tools that run on Ubuntu/Linux operational system.

## PHP

PHP language is used for the back-end (API) server. To make sure the PHP is installed in your system:

```bash
sudo apt update
sudo apt install curl php-cli php-mbstring git unzip
```

## Composer

A dependency manager for PHP ([site](https://getcomposer.org)):

Here is an instruction on how to install __composer__ for current user only:

```bash
cd ~
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'e0012edf3e80b6978849f5eff0d4b4e4c79ff1609dd1e613307e16318854d24ae64f26d17af3ef0bf7cfb710ca74755a') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php --install-dir=~/.local/bin --filename=composer
php -r "unlink('composer-setup.php');"
```
Log out from your computer and log in to make sure `~/.local/bin` directory is in the `$PATH`.

To check if the `$PATH` variable contains `~/.local/bin` use:

```bash
echo $PATH
```

## Git

Version control/collaboration.

```bash
sudo apt install git
```

# MySQL server

Database server.

```bash
sudo apt install mysql-server
```

MySQLWorkbench (optional) will help to visualise databases.

```bash
sudo apt install mysql-workbench
```

# Atom

Development IDE

```bash
sudo apt install atom
```

Install additional packages:

```bash
apm i atom-vue ide-vue terminal-tab vim-mode-plus docblockr
```
Alternatively, you may install packages using Atom IDE using the menu path: Edit->Preferences->Install.

# Symfony

[Symfony](https://symfony.com/) is a set of reusable PHP components, and a PHP framework for web projects. See [documentation](https://symfony.com/doc/current/index.html).

# API-platform

REST and GraphQL framework to build modern API-driven projects. See [site](https://api-platform.com/) and [documentation](https://api-platform.com/docs).

# Vue

[Vue](https://vuejs.org/) - front-end (JS application that talks to API server). The library used to write programs in JS for the browsers and mobile phones.
