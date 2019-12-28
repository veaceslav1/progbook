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

    ```bash
    cd ~
    curl -sS https://getcomposer.org/installer -o composer-setup.php
    ```

Next, verify that the installer matches the SHA-384 hash for the latest installer found on the [Composer Public Keys / Signatures](https://composer.github.io/pubkeys.html) page. Copy the hash from that page and store it as a shell variable:

    ```bash
    HASH=544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061
    ```
Make sure that you substitute the latest hash for the highlighted value.

Now execute the following PHP script to verify that the installation script is safe to run:

    ```bash
    php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
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

User interface for MySQL server for convenience:

    ```bash
    sudo apt install phpmyadmin
    ```
After installation visit: http://localhost/phpmyadmin

# Atom

Development IDE

    ```bash
    sudo apt install atom
    ```

You may consider installing additional packages in atom IDE (In Atom Edit->Preferences->Install)L atom-vue, ide-vue, terminal-tab, vim-mode-plus

# Symfony

[Symfony](https://symfony.com/) is a set of reusable PHP components, and a PHP framework for web projects. See [documentation](https://symfony.com/doc/current/index.html).

# API-platform

REST and GraphQL framework to build modern API-driven projects. See [site](https://api-platform.com/) and [documentation](https://api-platform.com/docs).

# Vue

[Vue](https://vuejs.org/) - front-end (JS application that talks to API server). The library used to write programs in JS for the browsers and mobile phones.
