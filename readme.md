# PHP Logs

3 ways:
- Inline (stdout)
- Log files
- Frameworks', 3rd party log libraries

In `php.ini`
- Turn on `log_errors`
- Turn off `display_errors`, so that errors would to into log files instead of appearing inline on screen
- Set `error_log` to 
	- either `syslog` - typically on Linux: `/var/log/syslog`
	- or a _specific file path_ - default on Linux: `/var/log/{server}/error.log`
	- in Windows: `C:\xampp\apache\logs\error.log`. You can easily display the last logs by `tail -f .\error.log`.

After editing the `php.ini`, you can use `<?php php_info(); ?>` and check `error_log` to see the path of the log file.

Other useful log functions in PHP:
- `error_reporting(E_ALL)` or whatever other level.
- `error_log(msg, type, dest, ...)` to make a error.

In PHP: Turn on the error display to the max:
```php
<?php 

ini_set('display_errors', 1);
ini_set('display_startup_errors', 1);
error_reporting(E_ALL);
```

Refs:

- https://rollbar.com/guides/where-are-php-errors-logged/
- https://www.loggly.com/ultimate-guide/php-logging-basics/  


- https://www.youtube.com/watch?v=5VtU-HK9PCw
- https://www.youtube.com/watch?v=4uMDw5q8Scs

# Monolog

- https://logtail.com/tutorials/how-to-start-logging-with-monolog/
- https://silex.symfony.com/doc/2.0/providers/monolog.html
- https://www.youtube.com/watch?v=cePgCwNoGF8
	- https://github.com/Seldaek/monolog

1. `composer require monolog/monolog`
2. Do as in `index.php`

# In Frameworks

- WP: 
	- https://github.com/atabegruslan/WP_CRUD/blob/master/README.md#turn-off-warnings
	- https://github.com/atabegruslan/WP_CRUD/blob/master/README.md#logging
- Laravel: https://github.com/Ruslan-Aliyev/Laravel8_Newest_Notes#logging

