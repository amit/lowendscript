Get php-fpm to listen on the correct host/port. In `/etc/php5/fpm/pool.d/www.conf` change the following line from:

	listen = /var/run/php5-fpm.sock

To:

	listen = 127.0.0.1:9000

Restart php-fpm with `sudo /etc/init.d/php5-fpm restart` and everything should work normally again.

[Credit](http://wildlyinaccurate.com/solving-502-bad-gateway-with-nginx-php-fpm)

Then run 

	sudo apt-get install php5-mysql

Update `wp-config.php` with 

	define('FS_METHOD', 'direct');
	/* Multisite */
	define('WP_ALLOW_MULTISITE', true);

Install Network from Tools menu

[Extra reading](http://wpmu.org/wordpress-multisite-wordpress-nginx/)