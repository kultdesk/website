Mostly boilerplate code for Wordpress-based site. 

Assets:

- `/wordpress-theme`: KultDesk WordPress theme to be installed in the WordPress instance (not used by docker-compose). Theme constructed using the Skatepark theme by Automattic following this method: https://developer.wordpress.org/themes/block-themes/creating-new-themes-using-the-site-editor/
- `additonal.css`: CSS file available in the Customize view of the Theme (note: it doesn't get exported - see step 2 below)

Initial installation steps: 

1. Clone repository.
2. Add nginx config file (see in a previous installation). Note: use `localhost` if you work locally.
3. Add `.env` file with passwords (see in a previous installation). Note: although you could use your own passwords, it's encouraged to use the ones in previous installations.
4. Zip `/wordpress-theme` folder and install and activate as Wordpress theme.
5. Copy-paste content of `additonal.css` into Additional CSS at `[DOMAIN]/wp-admin/customize.php`. Note: the page should be available via Appearance > Customize, but it's hidden in some Wordpress installations (the direct URL works though).
6. You may need to update the Wordpress version (through the admin page). Note: the last known stable Wordpress version for this theme is 6.4.1. 

Recommended development workflow:

1. Change content and look&feel in WP's new theme editor (still beta). Note: this step is ideally done in a local instance. 
2. Change theme version number in style.css (in WordPress admin site via Tools > Theme File Editor).
3. Export theme files (in the side bar of any template open in the editor view). 
4. Extract the files and overwrite the content of `/wordpress-theme`. 
5. Push changes to GitHub. Create new release (based on version number in step 2) as needed. 
6. 1: import zipped theme file back to WP so that theme plugin gets updated (Upload Theme) 2: manually copy-paste content of `additonal.css` (see above), 3: delete old version of theme. 
