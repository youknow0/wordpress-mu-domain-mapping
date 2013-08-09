wordpress-mu-domain-mapping
===========================

A patched Version of the Plugin Wordpress MU Domain Mapping that allows blogs to be served over HTTP while having the administration backend encrypted over HTTPS

Note that this plugin is not as well tested as the original version. I only know that it works quite well for my configuration. Your mileage may vary and it might break everything. Please only use this version if you really know what you are doing.

Usage
-----

1. Go through the usual install process of a Wordpress network with domain mapping. These steps are well documented at https://wordpress.org/plugins/wordpress-mu-domain-mapping/installation/
1. Edit your wp-config.php to force admin SSL. Replace example.org with the domain of your administration backend.
	if(!empty($_SERVER['HTTP_HOST']) && $_SERVER['HTTP_HOST'] == 'example.org') {
		define('FORCE_SSL_ADMIN', true);
	}
1. In the Domain mapping settings leave everything but "Redirect administration pages to site’s original domain" unchecked

