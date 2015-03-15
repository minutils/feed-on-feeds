Before installing, make sure you understand all the caveats listed in TrunkStatus.

## Get code ##

```
$ cd /WEB/ROOT
$ svn checkout http://feed-on-feeds.googlecode.com/svn/trunk/ feed-on-feeds
```

## Create fof-config.php ##

```
$ cd feed-on-feeds
$ cp fof-config-sample.php fof-config.php
$ nano fof-config.php # or your favorite $EDITOR
```

Change these settings to match how MySQL is configured on your web server:

```
// Database connection information.  Host, username, password, database name.

define('FOF_DB_HOST', "host.example.com");
define('FOF_DB_USER', "username");
define('FOF_DB_PASS', "password");
define('FOF_DB_DBNAME', "database");
```

## Run install.php ##

Navigate to http://example.com/feed-on-feeds/install.php in your browser

Compatibility with your PHP installation will be checked, database tables will be created, and a local 'cache' directory will be created.  You will be prompted to create a password for the 'admin' user.

## Done! ##

Navigate to http://example.com/feed-on-feeds/, login, and start subscribing or creating users!