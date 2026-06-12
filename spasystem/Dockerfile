FROM php:8.2-apache

# Install and enable the mysqli extension required by your database connection
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# Enable Apache rewrite module (useful for routing/clean URLs)
RUN a2enmod rewrite

# Copy all project files into the Apache web server directory
COPY . /var/www/html/

# Set the correct permissions for the web server
RUN chown -R www-data:www-data /var/www/html/

# Expose port 80 for Render to route traffic
EXPOSE 80