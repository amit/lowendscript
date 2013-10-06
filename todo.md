Start
	service php5-mysql start

Update `wp-config.php` with 

	define('FS_METHOD', 'direct');
	/* Multisite */
	define('WP_ALLOW_MULTISITE', true);

Fix permissions

	chown -R www-data:www-data <multisite_path>/public

Install Network from Tools menu

Install nginx helper plugin for network

[Extra reading](http://wpmu.org/wordpress-multisite-wordpress-nginx/)