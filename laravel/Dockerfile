# /Users/medaminebentaieb/Docker_files/Laravel_Docker/laravel/Dockerfile

FROM php:8.2-fpm

# Install system dependencies and PHP extensions
RUN apt-get update && apt-get install -y \
    build-essential \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    zip \
    unzip \
    git \
    supervisor \
    && docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

# Install Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# Set working directory
WORKDIR /var/www

# Copy application source code
COPY src/ /var/www

# Install Laravel dependencies
RUN composer install --optimize-autoloader --no-dev

# Copy Supervisord configuration
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

# Set permissions
RUN chown -R www-data:www-data /var/www

# Expose port 9000 and start Supervisord
CMD ["/usr/bin/supervisord"]
