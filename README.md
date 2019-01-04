# IAESTE CER Summer App
The official IAESTE CER Summer App build with WordPress + PWA functionality.

Except for WordPress itself, the installation is Composer-driven. This no changes on WordPress files should be made; Plugins and Themes are stated in the `.composer.json`.
There are ways to add WordPress itself as a dependency but until now the community decided against publishing an official Composer package. That's the reasoning behind this approach. 

## Installation
In case you already have an existing WordPress installation, you can skip steps 1 and 4.

1. Get a clean copy of the [latest Wordpress](https://codex.wordpress.org/Installing_WordPress) (`5.0.2` of this writing)
    * Go to the folder where WordPress should be installed
    * `wget https://wordpress.org/latest.tar.gz`
    * Extract WordPress into current directory
    
      `tar -xzvf latest.tar.gz && mv wordpress/* . && rmdir wordpress && rm latest.tar.gz`

2. Install this repository
    * Go to the WordPress root directory
    * `git init`
    * `git remote add origin https://github.com/pzoechner/iaeste-cer-summer-app.git`
    * `git fetch origin`
    * `git checkout -b master --track origin/master`

3. Install required Composer packages
    * `composer update`

4. Initial WordPress setup (setting up database, etc.)
5. Activate the theme `IAESTE CER Summer App` and all plugins

## Plugins
Head over to [Plugins.md](PLUGINS.md) for more information.

## Roadmap

- [x] Add theme repository
- [ ] (many other important things)
- [ ] Add [auto `git pull` and `composer update`](https://gist.github.com/noelboss/3fe13927025b89757f8fb12e9066f2fa) on new `git push`?
