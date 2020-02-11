# IAESTE CER Summer App
The official IAESTE CER Summer App built with WordPress + PWA functionality.

This repository is Composer-driven and does not include a WordPress installation. Plugins and Themes are required and updated via the `composer.json`.
There are ways to add WordPress itself as a dependency but until now the community decided against publishing an official Composer package. That's the reasoning behind following this approach.

## Installation
In case you already have an existing WordPress installation, you can skip step 1.

1. Get a clean copy of the [latest Wordpress](https://codex.wordpress.org/Installing_WordPress) (`5.0.2` of this writing)
    * Go to the folder where WordPress should be installed
    * `wget https://wordpress.org/latest.tar.gz`
    * Extract WordPress into current directory
    
      `tar -xzvf latest.tar.gz && mv wordpress/* . && rmdir wordpress && rm latest.tar.gz`

2. Install Composer package in root of WordPress installation

    * `echo {} > composer.json`
    * `composer config repositories.wpackagist '{ "type":"composer", "url":"https://wpackagist.org" }'`
    * `composer require pzoechner/iaeste-cer-summer-app`

3. Initial WordPress setup (setting up database, etc.)
4. Activate the theme `IAESTE CER Summer App` and all plugins
5. Import the Plugin configuration from the JSON files in [/data](https://github.com/pzoechner/iaeste-cer-summer-app/blob/master/data/).


## Development
To make the included [theme](https://github.com/pzoechner/iaeste-cer-summer-app-theme) git-aware, do the following:

* Go to the WordPress root directory
* `cd wp-content/themes/iaeste-cer-summer-app-theme/`
* `git init`
* `rm -r * && rm .gitignore`
* `git remote add origin https://github.com/pzoechner/iaeste-cer-summer-app-theme.git`
* `git pull origin master`

This is pretty ugly. Please update if you know of a better way.

## How to contribute
First, get to know Wordpress and read about [Custom Post Types](https://codex.wordpress.org/Post_Types#Custom_Post_Types). Another helpful resource is the [WordPress Template Hierachy](https://wphierarchy.com/).

In case you haven't contributed to an Open Source project before, please quickly read through [this guide](https://github.com/firstcontributions/first-contributions) to get an idea of how to clone projects and send PRs (pull requests).

## Plugins
Head over to [Plugins.md](docs/PLUGINS.md) for more information.


## Roadmap

- [x] Add theme repository
- [x] Add project to Packagist

