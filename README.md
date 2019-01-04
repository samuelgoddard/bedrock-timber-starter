# Bedrock + Nanobox + Timber Starter

The project uses/requires the following:

* PHP >= 7.1
* MySQL >= 5.0.15
* [Composer](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx) as a dependency manager
* [Roots Bedrock](https://roots.io/bedrock/) as a modern WordPress boilerplate
* [WordPress Packagist](https://wpackagist.org/) for composer based plugin management
* [Sass](http://sass-lang.com/) for stylesheet preprocessing
* [Nanobox](https://nanobox.io/) for local development
* [Git Flow](https://nvie.com/posts/a-successful-git-branching-model/) as a branching model
* [Timber](https://github.com/timber/timber) for Twig based WordPress templating
* [Timber Library](https://wordpress.org/plugins/timber-library/) and [ACF](https://en-gb.wordpress.org/plugins/advanced-custom-fields/) plugins (installed by composer out the box)

## Fresh Installation

1. Clone the repo:
```bash
git clone git@github.com:samuelgoddard/bedrock-timber-starter.git
```

2. Install the Nanobox CLI tool. You will need a (free) [account](https://dashboard.nanobox.io/users/register).

3. Init Git Flow
```bash
git flow init 
```

4. Add local DNS alias
```bash
nanobox dns add local bedrock.wordpress.localdev
```

5. Start the server, first time installation will run `composer install`:

```bash
nanobox run php-server
```

6. Duplicate / rename the `.env.example` file and update environment variables within it. Nanobox database details can be found by running `nanobox info local`:
<pre>
<b>DB_NAME</b> - Database name
<b>DB_USER</b> - Database user
<b>DB_PASSWORD</b> - Database password
<b>DB_HOST</b> - Database host
<b>WP_ENV</b> - Set to environment (<em>development</em>, <em>staging</em>, <em>production</em>)
<b>WP_HOME</b> - Full URL to WordPress home (<em>http://bedrock.wordpress.localdev</em>)
<b>WP_SITEURL</b> - Full URL to WordPress including subdirectory (<em>http://bedrock.wordpress.localdev/wp</em>)
<b>AUTH_KEY</b>, <b>SECURE_AUTH_KEY</b>, <b>LOGGED_IN_KEY</b>, <b>NONCE_KEY</b>, <b>AUTH_SALT</b>, <b>SECURE_AUTH_SALT</b>, <b>LOGGED_IN_SALT</b>, <b>NONCE_SALT</b>
</pre>

You can cut and paste salts from the [Roots WordPress Salt Generator](https://roots.io/salts.html).

7. Set your site vhost document root to `web/` (`/path/to/site/current/web/` if using deploys). This is done out of the box locally within the `boxfile.yml`

8. Access WP admin at `http://bedrock.wordpress.localdev/wp/wp-admin` and follow the instructions to install. Or grab the current database from XXX (add database storage details)

9. Activate the 'Bedrock Timber Starter' theme in `Appearance > Themes`

10. Theme files are stored in a different location to normal by Bedrock - `web/app/themes/starter`

## Plugin Management
Plugin management is done via composer and [WordPress Packagist](https://wpackagist.org/). We install the [Timber Library](https://wordpress.org/plugins/timber-library/) and [ACF](https://en-gb.wordpress.org/plugins/advanced-custom-fields/) plugins by default, these are set as 'mu-plugins', essentially plugins that users have no control of disabling / enabling in the backend. Config can be found in the `composer.json` file.

## Deploys

One deployment requirement:

`composer install` must be run as part of the deploy process.

## Useful Documentation

* WordPress Codex - [https://codex.wordpress.org/](https://codex.wordpress.org/)
* Bedrock documentation - [https://roots.io/bedrock/docs/](https://roots.io/bedrock/docs/).
* Timber documentation - [https://timber.github.io/docs/guides/acf-cookbook/#nav](https://timber.github.io/docs/guides/acf-cookbook/#nav).
* Timber ACF Cookbook - [https://timber.github.io/docs/guides/acf-cookbook/](https://timber.github.io/docs/guides/acf-cookbook/#nav)

