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

In your home directory create a file called ```.gitconfig``` and write in it your git credentials:

```ini
[user]
    name = Your Name
    email = yourgitemail@example.com
[push]
    default = matching
[credential "https://github.com"]
    username = yourgitusername
```
This file will simplify the pushing to git process. You will not need to provide your username at every push command.

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

# Node.js

[Node.js](https://nodejs.org) allows Java Script to run on computer from comand line. It comes with own package management system (npm). To install node.js on Ubuntu see [instructions](https://github.com/nodesource/distributions/blob/master/README.md). Shortcut for version 12 for Ubuntu:

```bash
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt-get install -y nodejs
```

# Vue

[Vue](https://vuejs.org/) - front-end (JS application that talks to API server). The library used to write programs in JS for the browsers and mobile phones.

For a rich in features administration project can be used [vue-admin-template](https://github.com/PanJiaChen/vue-admin-template) (note that node.js npm is required for this installation):

```bash
git clone https://github.com/PanJiaChen/vue-admin-template.git

cd vue-admin-template

npm install

npm run dev
```
Note that __vue-element-admin__ makes use of [eleme.io](https://element.eleme.io/#/en-US) library. Components documentation can be found [here](https://element.eleme.io/#/en-US/component).