# IAESTE CER Summer App
The official IAESTE CER Summer App build with WordPress + PWA functionality.

This repository is Composer-driven and does not include a WordPress installation. So, no changes on WordPress Core files should be made; Plugins and Themes are required in `composer.json`.
There are ways to add WordPress itself as a dependency but until now the community decided against publishing an official Composer package. That's the reasoning behind this approach.

## Installation
In case you already have an existing WordPress installation, you can skip steps 1 and 4.

1. Get a clean copy of the [latest Wordpress](https://codex.wordpress.org/Installing_WordPress) (`5.0.2` of this writing)
    * Go to the folder where WordPress should be installed
    * `wget https://wordpress.org/latest.tar.gz`
    * Extract WordPress into current directory
    
      `tar -xzvf latest.tar.gz && mv wordpress/* . && rmdir wordpress && rm latest.tar.gz`

2. Install required Composer packages

    * `composer config repositories.wpackagist '{ "type":"composer", "url":"https://wpackagist.org" }'`
    * `composer require pzoechner/iaeste-cer-summer-app`
    * `composer update`

3. Initial WordPress setup (setting up database, etc.)
4. Activate the theme `IAESTE CER Summer App` and all plugins

## Development
To make the included theme git-aware, do the following:

    * Go to the WordPress root directory
    * `cd wp-content/themes/iaeste-cer-summer-app-theme/`
    * `git init`
    * `git remote add origin https://github.com/pzoechner/iaeste-cer-summer-app-theme.git`
    * `git fetch origin`
    * `git checkout -b master --track origin/master`

## Plugins
Head over to [Plugins.md](PLUGINS.md) for more information.

## Roadmap

- [x] Add theme repository
- [x] Add project to Packagist
