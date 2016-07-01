sample-project
==============

Sample Symfony project.

This is intended to be a skeleton which is forked and modified to implement your own application.

Configuration Checker
------
If you want to view the [Configuration Checker](http://symfony.com/doc/current/book/installation.html#checking-symfony-application-configuration-and-setup),
you'll need to `touch web/config.php` then `composer install` to reinstate the file from Symfony, then modify the file
to remove this section:

```
if (!in_array(@$_SERVER['REMOTE_ADDR'], array(
    '127.0.0.1',
    '::1',
))) {
    header('HTTP/1.0 403 Forbidden');
    exit('This script is only accessible from localhost.');
}
```

This allows the file to be accessible when running in Docker.
