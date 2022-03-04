# Reel Radio migration log

**Migration from `dev1` to `moondog4` was performed on Feb 18, 2022**

Cloned site respository to `/export/web/reelradio` on new production machine: `moondog4`.

Copied over apache2 config files, and symlinked to `sites-enabled`.

**PROBLEM**: Apache2 config not working when copied straight from `dev1` development machine.

- The `000-default.conf` default configuration file is somehow overriding the main site
- We need this file for the `certbot` stuff later on, however removing the `000-default.conf` file makes the site behave how we want
- We manually created a certificate with `certbot`, and copied over the old `000-default.conf` files, then added the SSL config to the `100-reelradio.conf` file 
- We discovered a server alias in the `100-reelradio.conf` file that was conflicting with the apache2 server, so we were able to fix the problem

Next, we initialized MySQL and copied over the tables from `dev1`.

Next, phpMyAdmin was installed on the new machine, and the latest user table was exported from the old site, and imported into the new site via phpMyAdmin.

Once the site was up, we installed Composer and installed PHP dependencies, and setup the `.env` file with secrets on the production machine.

The latest comments from the original machine were copied to the new production machine.

Then, to get exhibits up and running, we had to modify the play script to point to the new machine. 
There is no longer a reason to redirect the users to the m3 machine to play the exhibit, because m4 will now take care of everything.

**PROBLEM**: We were running into an error where the PHP file to play the exhibits would not exec correctly.

- The solution was to disable cgi scripts in the play directory to reenable the `play.php` file to run.
- Then, the `play.php` script needed to be modified to point to the right port on the streaming engine, Wowza

Finally, since all users have cookies stored in their browsers, a notice was posted to log out and relogin.

To complete the migration, DNS entries were changed to point to the new production server.

New site is up! 
