Mostly boilerplate code for Wordpress-based site. 

Assets:

- `/wordpress-theme`: KultDesk WordPress theme to be installed in the WordPress instance (not used by docker-compose). Theme constructed using the Skatepark theme by Automattic following this method: https://developer.wordpress.org/themes/block-themes/creating-new-themes-using-the-site-editor/
- `additonal.css`: CSS file available in the Customize view of the Theme (note: it doesn't get exported - see step 2 below)

Recommended development workflow:

1. Change content and look&feel in WP's new theme editor (still beta). Note: this step is ideally done in a local instance. 
2. Change theme version number in style.css (in WordPress admin site via Tools > Theme File Editor).
3. Export theme files (see in link above). 
4. Extract the files and overwrite the content of `/wordpress-theme`. 
5. Push changes to GitHub. Create new release (based on version number in step 2) as needed. 
6. 1) import zipped theme file back to WP so that theme plugin gets updated (Upload Theme) 2) manually copy-paste content of `additonal.css` (see above), 3) delete old version of theme. 
