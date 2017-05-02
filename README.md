# WP Requirements Check

Simple drop-in class to check minimum PHP and WordPress version requirements in your plugin.

## Usage

1. Run `composer require wearerequired/openinbound-wordpress`
2. In your main plugin file, instantiate the class using something like this:

```php
$requirements_check = new WP_Requirements_Check( array(
	'title' => 'My awesome plugin',
	'php'   => '6.0',
	'wp'    => '4.7',
	'file'  => __FILE__,
) );

if ( $requirements_check->passes() ) {
	// Proceed.
}
```

## Credits

Thanks to Mark Jaquith for his [grunt-wp-plugin](https://github.com/markjaquith/grunt-wp-plugin) template which contains similar code.