# Magento 2 CloudDocker for Open Source Edition

Inspired by [magento/magento-cloud-docker] https://github.com/magento/magento-cloud-docker

I extracted official Dockerfile files, applied some minor fixes and built a docker-composer.yml capable of running open source edition 

Configured with persistent storage

## Usage

Extract Magento open source to `/app`

Magento command

    docker-compose run --rm cli magento-command

Run cron

    docker-compose run --rm cli run-cron

Run installer

    docker-compose run --rm cli magento-command setup:install --admin-firstname Admin --admin-lastname User [...]

### Optional 

Configure magento to use redis, elasticsearch and varnish if you choose to run the containers

## Build

### nginx

    cd images/nginx/1.9

    docker login

    docker build -t domw/magento2-cloud-nginx:1.9 ./

    docker push domw/magento2-cloud-nginx:1.9

ngingx versions: 1.9

### php-fpm

    cd images/php/7.2-fpm

    docker login

    docker build -t domw/magento2-cloud-php:7.2-fpm ./

    docker push domw/magento2-cloud-php:7.2-fpm

php versions: 7.2, 7.3, 7.4

### php-cli

    cd images/php/7.2-cli

    docker login

    docker build -t domw/magento2-cloud-php:7.2-cli ./

    docker push domw/magento2-cloud-php:7.2-cli

php versions: 7.2, 7.3, 7.4    

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

varnish versions: 4.0, 6.2

### elasticsearch

    cd images/elasticsearch/7.6

    docker login

    docker build -t domw/magento2-cloud-elasticsearch:7.6 ./

    docker push domw/magento2-cloud-elasticsearch:7.6

elasticsearch versions: 1.7, 2.4, 5.2, 6.5, 6.8, 7.5, 7.6
