# docker-php-composer-node

This Dockerfile specifies a Docker container with developer tools useful for Drupal, WordPress, and PHP development.
This container is best utilized for CI purposes.

Tools installed:

* PHP
* Apache
* Composer
* Node
* Drush
* WP-CLI
* Node
* NPM
* Yarn
* Fabric
* Mkdocs


# Example Local Usage

Normally this container would be run in a CI environment, but it's also possible to use it for local development.

To run a PHP docroot on local port 8999 (http://localhost:8999):
```
sudo docker run \
    -d \
    --restart=always \
    -v /path/to/my/php/docroot:/var/www/html \
    -p 8999:80 \
    --name "php-composer-node" \
    awhalen/docker-php-composer-node:latest
```

Or to use it interactively:
```
sudo docker run \
    -it \
    --name "php-composer-node" \
    --entrypoint /bin/bash \
    awhalen/docker-php-composer-node:latest
```


# Build Commands

Build the image locally from the Dockerfile:
```
sudo docker build -t php-composer-node .
```

Test the image:
```
sudo docker run -it php-composer-node /test.sh
```
