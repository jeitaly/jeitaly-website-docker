# Use the official PHP 8.3.15 image with Apache
FROM php:8.3.15-apache

# Install necessary extensions for WordPress
RUN apt-get update && apt-get install -y \
    libjpeg-dev \
    libpng-dev \
    libfreetype6-dev \
    libzip-dev \
    zip \
    && docker-php-ext-configure gd \
    --with-freetype=/usr/include/ \
    --with-jpeg=/usr/include/ \
    && docker-php-ext-install gd mysqli zip \
    && a2enmod rewrite

# Set the working directory
WORKDIR /var/www/html

# Update permissions
RUN chown -R www-data:www-data /var/www/html \
    && chmod -R 755 /var/www/html

# Enable old mysqli auth
RUN docker-php-ext-install mysqli