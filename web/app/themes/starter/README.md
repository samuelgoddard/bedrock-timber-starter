
# SHU Starter Theme

This theme is built on [Timber](https://www.upstatement.com/timber/).

## Installing the Theme

Install this theme as you would any other, and be sure the Timber plugin is activated. But hey, let's break it down into some bullets:

1. Make sure you have installed the plugin for the [Timber Library](https://wordpress.org/plugins/timber-library/), and [Advanced Custom Fields](https://timber.github.io/docs/guides/acf-cookbook/#nav). 
2. Download the zip for this theme (or clone it) and move it to `wp-content/themes` in your WordPress installation. 
4. Activate the theme in Appearance >  Themes.

## What's here?

`static/` is where you can keep your static front-end scripts, styles, or images. In other words, your Sass files, JS files, fonts, and SVGs would live here.

`templates/` contains all of your Twig templates. These pretty much correspond 1 to 1 with the PHP files that respond to the WordPress template hierarchy. At the end of each PHP template, you'll notice a `Timber::render()` function whose first parameter is the Twig file where that data (or `$context`) will be used. Just an FYI.

## Other Resources

* [Timber Wiki](https://github.com/jarednova/timber/wiki)
* [Twig for Timber Cheatsheet](http://notlaura.com/the-twig-for-timber-cheatsheet/)
