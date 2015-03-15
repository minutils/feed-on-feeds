# Introduction #

The code checked into the trunk right now is alpha quality.  When I think it's stable enough, I'll make a formal release called "Feed on Feeds 0.5".  For now I guess we can call it "Feed on Feeds 0.4999..."

# What seems to work #

This version has been fairly well tested on Firefox 1.5 and Safari 2.0.  It is installed on a Linux host with PHP 5.1 and MySQL 5.0.  PHP 4.3.2 or greater should work, and MySQL 4 should also be fine.  On my server I have two users, one (me!) with about 300 subscribed feeds and another with just a handful.  Performance is acceptable.

Favicons can be turned on in the prefs, and work pretty well thanks to SimplePie's detection and caching.  Time zone is also now set as a pref.

Private feeds (https and/or authenticated) work, as long as your server has the cURL extension.

For security, I've audited every query and put in place some code to make sure that query parameters are all escaped and are of the expected types.  I also added some code to try to undo any damage caused by register\_globals, if it happens to be on.  I've made sure every page that should require a log in does, implemented a hashed password scheme, and generally checked over all the code for security problems.  As far as I know, it's clean.

Tagging has now reached a minimally useful state.  You can tag and untag items and feeds, and view items by tag, and even just the new items in a particular tag.

# What is definitely broken #

## IE ##

I have given up on IE6 completely.  IE7 mostly works.  Mostly.

## Wii ##

I can't read my feeds very well on the Wii browser!  This must be fixed!  It would be nice if FoF had a workaround for the Wii browser's lack of tabs, as well.

# What is half done #

KeyboardNavigation.