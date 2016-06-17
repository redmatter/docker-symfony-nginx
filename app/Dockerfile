FROM php:7-fpm-alpine

ADD www /var/www/html

RUN ( \
    # This is intended to be a production-ready image, so remove app_dev.php and config.php.
    # When running in dev mode, these can be re-mounted back in.
    rm -f /var/www/html/web/app_dev.php /var/www/html/web/config.php && \

    # Give ownership of the cache, logs and sessions directories to www-data, so it can write to them
    chown -R www-data:www-data /var/www/html/var/cache /var/www/html/var/logs /var/www/html/var/sessions \
)

VOLUME [ "/var/www/html/var/cache", "/var/www/html/var/logs", "/var/www/html/var/sessions" ]