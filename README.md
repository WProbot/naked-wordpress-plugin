# Naked WordPress Plugin
Another simple plugin starter for only PHP codes.

````php
<?php

/**
 * Plugin Name: My Plugin
 * Description: Some description about the plugin.
 * Version:     1.0.0
 * Author:      Me
 * Author URI:  https://my-website.com
 * Text Domain: my-plugin
 * Domain Path: /languages
 */

if (!defined('ABSPATH')) {
    exit('No direct script access allowed');
}

if (!class_exists('MY_PLUGIN')) {

    define('MY_PLUGIN_VERSION', '1.0.0');

    define('MY_PLUGIN_PATH', plugin_dir_path(__FILE__));
    define('MY_PLUGIN_URL', plugin_dir_url(__FILE__));

    define('MY_PLUGIN_TEMPLATE_PATH', trailingslashit(get_template_directory()));
    define('MY_PLUGIN_TEMPLATE_URL', trailingslashit(get_template_directory_uri()));

    define('MY_PLUGIN_CHILD_PATH', trailingslashit(get_stylesheet_directory()));
    define('MY_PLUGIN_CHILD_URL', trailingslashit(get_stylesheet_directory_uri()));

    define('MY_PLUGIN_IS_CHILD', MY_PLUGIN_TEMPLATE_PATH != MY_PLUGIN_CHILD_PATH ? true : false);

    class MY_PLUGIN
    {
        function __construct()
        {
          // Do some magic here!
        }
    }

    new MY_PLUGIN;

}
```
