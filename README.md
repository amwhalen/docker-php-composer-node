# docker-php-composer-node

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

Build the image locally from the Dockerfile:
```
sudo docker build -t php-composer-node .
```
