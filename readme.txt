=== Better WordPress Minify ===
Contributors: OddOneOut
Donate link: http://betterwp.net/wordpress-plugins/bwp-minify/
Tags: CSS, javascript, JS, minify, minification, optimization, optimize
Requires at least: 2.8
Tested up to: 3.3
Stable tag: 1.0.10

Allows you to minify your CSS and JS files for faster page loading for visitors.

== Description ==

Allows you to minify your CSS and JS files for faster page loading for visitors. This plugin uses the PHP library [Minify](http://code.google.com/p/minify/) and relies on WordPress's enqueueing system rather than the output buffer (will not break your website in most cases). This plugin is very customizable and easy to use.

**Some Features**

* Uses the enqueueing system of WordPress which improves compatibility with other plugins and themes
* Allows you to customize all minify strings
* Offers various way to add a cache buster to your minify string
* Gives you total control over how this plugin minifies your scripts
* Supports script localization (`wp_localize_script()`)
* Supports RTL stylesheets
* Supports media-specific stylesheets (e.g. 'screen', 'print', etc.)
* Supports conditional stylesheets (e.g. `<!--[if lt IE 7]>`)
* Provides hooks for further customization
* WordPress Multi-site compatible (not tested with WPMU)

**Languages**

* English (default)
* Romanian (ro_RO) - Thanks to [Luke Tyler, International Calling Cards](http://www.enjoyprepaid.com)!

Please [help translate](http://betterwp.net/wordpress-tips/create-pot-file-using-poedit/) this plugin!

**Important Notes**

The cache folder must be writable, please visit [Plugin's Official Page](http://betterwp.net/wordpress-plugins/bwp-minify/) for more information!

**Get in touch**

* I'm available at [BetterWP.net](http://betterwp.net) and you can also follow me on [Twitter](http://twitter.com/0dd0ne0ut).
* Check out [latest WordPress Tips and Ideas](http://feeds.feedburner.com/BetterWPnet) from BetterWP.net.

== Installation ==

1. Upload the `bwp-minify` folder to the `/wp-content/plugins/` directory
2. Activate the plugin through the Plugins menu in WordPress. After activation, you should see a menu of this plugin under Settings.
3. Configure the plugin, optionally choose a minify URL (ony recommended if you are experienced with URL and server paths), and modify Minify's `config.php` as you please. Please read [here](http://betterwp.net/wordpress-plugins/bwp-minify/#customization) for more information.
4. Make sure the `cache` folder is writable, by `CHMOD` it to either `755` or `777`, depending on which one will work for you.
5. Enjoy!

== Frequently Asked Questions ==

[Check plugin news and ask questions](http://betterwp.net/topic/bwp-minify/).

== Screenshots ==

1. Changing the Minify URL, now one can have a shorter and nicer URL ;)

== Changelog ==

= 1.0.10 =
* Fixed two possible PHP notices when using root-relative paths as Minify URL. Thanks to [Marcus](http://marcuspope.com/)!
* Fixed wrongly closed HTML `<link>` tags.
* Fixed a bug that breaks the dynamic JS file enqueued by Mingle plugin.
* Fixed an incompatibility issue with WP Download Monitor.
* Fixed an incompatibility issue with Geo-Mashup, thanks to JeremyCherfas for reporting!
* Added support for the new script localization function introduced in WordPress 3.3. Thanks to **workshopshed** for reporting!
* Added Romanian translation, thanks to Luke Tyler!

= 1.0.9 =
* Fixed a possible PHP warning about an argument not being an array.

= 1.0.8 =
* Hot fix for 1.0.7, which resolves the broken CSS issues for the wp-login page when you install WordPress in a sub-directory.

= 1.0.7 =
* Hot fix for 1.0.6, which resolves some compatibility issues with certain plugins.

= 1.0.6 =
* Added four more hooks for theme developers to fully control how scripts and styles should be enqueued and minified.
* Changed the Min URL hook a bit so themes can actually filter it.
* Added support for plugins or themes that try to enqueue and print script using the `wp_footer` action instead of the `init` action. Plugins like 'Jetpack by WordPress.com' should be working correctly now.
* Other improvements made to the positioning of styles and scripts.

**Enjoy BWP Minify!**

= 1.0.5 =
* Added support for theme developers who would like to integreate BWP Minify into their themes 
	* Added a new hook added for `min` path.
	* Added new hooks to allow theme developers to only minify certain media files (see [this section](http://betterwp.net/wordpress-plugins/bwp-minify/#allowed-handles) for more details).
	* Some bug fixes.
* A lot of improvements have been made to catch styles and scripts printed using `wp_print_scripts` and `wp_print_styles`.
* The base (`b`) parameter has been removed from the minify string to add support for non-standard WordPress installation (`wp-content` has been moved or renamed.) Thanks to [Lee Powell](http://twitter.com/leepowell) for bug reports and patches!
* Fixed a bug that makes BWP Minify fail to determine the cache directory in a sub-folder installation of Multi-site.
* Fixed a possible incompatibility issue with Easy Fancybox, thanks to Bob for reporting!
* Minor bug fixes for login and signup pages.

= 1.0.4 =
* Fixed an incompatibility issue with media files' uppercase letters.
* Fixed a minor undefined offset notice, thanks to Torsten!

= 1.0.3 =
* Fixed a compatibility issue with dynamically generated media files, thanks to naimer!
* Not really a changelog, but [a small snippet](http://betterwp.net/wordpress-plugins/bwp-minify/#positioning-your-scripts) for users who want to exclude CSS files has been posted.

= 1.0.2 =
* Fixed a compatibility issue with other plugins loading styles and scripts on a separate .php page. Thanks to larry!
* Also fixed a possible bug in 1.0.1

= 1.0.1 =
* The plugin should now detect cache folder correctly for users who install WordPress in a sub-directory.

= 1.0.0 =
* Initial Release.

== Upgrade Notice ==

= 1.0.0 =
* Enjoy the plugin!