Mostly boilerplate code for Wordpress-based site. 

Assets:

- `/wordpress-theme`: KultDesk WordPress theme to be installed in the WordPress instance (not used by docker-compose). Theme constructed using the Skatepark theme by Automattic following this method: https://developer.wordpress.org/themes/block-themes/creating-new-themes-using-the-site-editor/
- `additonal.css`: CSS file available in the Customize view of the Theme (note: it doesn't get exported - see step 2 below)

Development workflow:

1. Change content and look&feel in WP's new theme editor (still beta). Note: this step is ideally done in a local instance. 
2. Export theme files (see in link above). 
3. Overwrite Copy extracted `/wordpress-theme` folder with files from previous step. 
4. Push changes to GitHub. 
5. Optionally: 1) import zipped theme file back to WP so that theme plugin gets updated (Upload Theme) 2) manually copy-paste content of `additonal.css` (see above), 3) delete old version of theme. 
