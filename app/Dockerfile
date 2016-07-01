FROM php:7-fpm-alpine

ADD www /var/www/html

# Give ownership of the cache, logs and sessions directories to www-data, so it can write to them
RUN chown -R www-data:www-data /var/www/html/var/cache /var/www/html/var/logs /var/www/html/var/sessions

VOLUME [ "/var/www/html/var/cache", "/var/www/html/var/logs", "/var/www/html/var/sessions" ]