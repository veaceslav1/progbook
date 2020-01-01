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
