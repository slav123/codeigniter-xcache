#CodeIgniter-xcache
==================

##XCache driver CodeIgniter

Here is a missing [XCache](http://xcache.lighttpd.net/) driver for [CodeIgniter Caching Class](http://ellislab.com/codeigniter/user-guide/libraries/caching.html). All You need to do is to modify __/system/libraries/Cache/Cache.php__ library and add additional Cache driver to drivers list:

	protected $valid_drivers = array('cache_apc', 'cache_file', 'cache_memcached', 'cache_dummy', 'cache_xcache');

Then you need to upload Cache_xcache.php file, to this directory: __/system/libraries/Cache/drivers/__

##Usage
Load cache drivers as usually:


	$this->load->driver('cache', array('adapter' => 'xcache'));
and use as it

	$this->cache->save('my_variable', array(0=>'data', 1=>'other data'));

	print_r($this->cache->get('my_variable'));

Due to XCache limitations You can’t store objects in cache, but you can serialize them before saving :)

##Support
To read more about XCache Caching functions please check out [XCache API docs](http://xcache.lighttpd.net/wiki/XcacheApi#Cacher)

If you have any questions or comments, please leave them here (github) or visit this page:

[www.spidersoft.com.au/projects/xcache-driver-codeigniter](http://www.spidersoft.com.au/projects/xcache-driver-codeigniter/)