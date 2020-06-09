# Magento 2 CloudDocker

WIP

## Build

### nginx

    cd images/nginx/1.9

    docker login

    docker build -t domw/magento2-cloud-nginx:1.9 ./

    docker push domw/magento2-cloud-nginx:1.9

### php-fpm

    cd images/php/7.2-fpm

    docker login

    docker build -t domw/magento2-cloud-php:7.2-fpm ./

    docker push domw/magento2-cloud-php:7.2-fpm

### php-cli

    cd images/php/7.2-cli

    docker login

    docker build -t domw/magento2-cloud-php:7.2-cli ./

    docker push domw/magento2-cloud-php:7.2-cli

### tls

    cd images/tls

    docker login

    docker build -t domw/magento2-cloud-tls:latest ./

    docker push domw/magento2-cloud-tls:latest

### varnish

    cd images/varnish/6.2

    docker login

    docker build -t domw/magento2-cloud-varnish:6.2 ./

    docker push domw/magento2-cloud-varnish:6.2

## Usage

Extract Magento open source to `/app`

Magento command

    docker-compose run --rm deploy magento-command

