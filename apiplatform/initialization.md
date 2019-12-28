# Api Platform initalization

This document describes the methods to start building an api based on symfony and api-platform in linux.

## Initiating a symfony api project

  ```bash
  # Create a new Symfony Flex project
  composer create-project symfony/skeleton bookshop-api
  # Enter the project folder
  cd bookshop-api
  # Install the API Platform's server component in this skeleton
  composer req api
  ```
Then, create the database and its schema:

  ```bash
  bin/console doctrine:database:create
  bin/console doctrine:schema:create
  ```

And start the built-in PHP server:

  ```bash
  # Built-in PHP server
  php -S 127.0.0.1:8000 -t public
  ```
# Tutorials

[API Platform: Serious RESTful APIs](https://symfonycasts.com/screencast/api-platform)

[API Platform Part 2: Security](https://symfonycasts.com/screencast/api-platform-security)
