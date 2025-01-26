# docker/php/Dockerfile
FROM php:8.2-fpm

# Install system dependencies
RUN apt-get update && apt-get install -y  \
    wget\
    git \
    unzip \
    libicu-dev \
    libzip-dev \
    libxml2-dev \
    libpq-dev \
    && docker-php-ext-install \
        intl \
        pdo_mysql \
        zip

# Install Composer
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

# Install Symfony CLI (optional)
RUN wget https://get.symfony.com/cli/installer -O - | bash \
    && ls -la /root/.symfony5/bin \
    && mv /root/.symfony5/bin/symfony /usr/local/bin/symfony

# Copy custom php.ini settings if needed
COPY docker/php/php.ini /usr/local/etc/php/conf.d/php.ini

WORKDIR /var/www/html

