# docker-php-composer-node

To run a PHP docroot on local port 8999 (http://localhost:8999):
```
sudo docker run \
    -d \
    --restart=always \
    -v /path/to/my/php/docroot:/var/www/html \
    -p 8999:80 \
    --name "php-composer-node" \
    php-composer-node
```

Or to use it interactively:

```
sudo docker run \
    -it \
    --name "php-composer-node" \
    --entrypoint /bin/bash \
    php-composer-node
```

Build the image locally:
```
sudo docker build -t php-composer-node .
```