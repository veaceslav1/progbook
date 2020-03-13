# PHP Install

To install PHP of higher than offered in Ubuntu packages do the following:

## Step 1: Add PHP PPA Repository

```bash
sudo apt-get update
sudo apt -y install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
```

## Step 2: Install PHP 7.4


```bash
sudo apt -y install php7.4

# check installed version
php -v
```

## Step 3: Install additional packages

```bash
sudo apt-get install -y php7.4-{bcmath,bz2,intl,gd,mbstring,mysql,zip,curl}
```

# PHP Settings

Changing between php versions on ubuntu/linux:

### Apache:

```bash
sudo a2dismod php7.3
sudo a2enmod php5.6
sudo service apache2 restart
```

### CLI (Command line):

```bash
sudo update-alternatives --set php /usr/bin/php5.6
sudo update-alternatives --set phar /usr/bin/phar5.6
sudo update-alternatives --set phar.phar /usr/bin/phar.phar5.6 
sudo update-alternatives --set phpize /usr/bin/phpize5.6
sudo update-alternatives --set php-config /usr/bin/php-config5.6
```
