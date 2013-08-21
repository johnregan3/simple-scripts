Simple Header & Footer Scripts
=================

An easy-to-use WordPress Plugin to add custom scripts (like Google Analytics) to your website's Header and/or Footer.  Great for Administrators who don't want to store their custom scripts in a theme's options.  These fields will remain even if the theme is changed.

**Features**

- No configuration needed, just enter your JavaScript(s).
- Scripts print after enqueued scripts (like jQuery) are rendered
- Simple interface built on WordPress UI
- Virtually no impact on site performance
- Uses no JavaScript files or complicated database queries
- Generates no files
- Extremely lightweight (~8KB)
- Thorough Documentation

### Installation

Install Simple Header & Footer Scripts just as you would any other WP Plugin:

1.  [Download Simple Header & Footer Scripts](http://wordpress.org/plugins/simple-custom-css/ "Download Simple Header & Footer Scripts") from WordPress.org.

2.  Unzip the .zip file.

3.  Upload the Plugin folder (simple-header-footer-scripts/) to the wp-content/plugins folder.

4. Go to [Plugins Admin Panel](http://codex.wordpress.org/Administration_Panels#Plugins "Plugins Admin Panel") and find the newly uploaded Plugin, "Simple Custom CSS" in the list.

5. Click "Activate Plugin."

[More help installing Plugins](http://codex.wordpress.org/Managing_Plugins#Installing_Plugins "WordPress Codex: Installing Plugins")

### Use

1.  Navigate to Tools > Header/Footer Scripts

2.  Enter in valid JavaScript/jQuery

3.  Click "Update Scripts"

4.  View your changes in the Front End of your website

### requently Asked Questions

Find more help at the [Simple Custom CSS Wiki](https://github.com/johnregan3/simple-custom-css/wiki "Simple Custom CSS Wiki")

#### Will this Plugin work on my WordPress.com website?

Sorry, this plugin is available for use only on self-hosted (WordPress.org) websites.

####Why aren't my scripts working?

It's important to note that this plugin simply prints your scripts into your posts/pages; it does nothing to modify or execute the scripts.

If you're having problems, first check the source of your page in the browser.  Ensure that the scripts are printing into the header/footer as you have entered them.  ***If the scripts are being printed into the page, the plugin is functioning correctly.***

Unfortunately, if they are being printed but still not working, there is an error with your script, or perhaps in the order in which they are being loaded into the page.  ***The author is ready and willing to help users and fix problems with this plugin, but because this is a free plugin, the author is unable devote the time to help debugging JavaScript errors.***  You may need to seek help with the scripts in places like [Stack Overflow](http://stackoverflow.com, "Stack Overflow")

### Help

[Simple Header & Footer Scripts Wiki](https://github.com/johnregan3/simple-header-footer-scripts/wiki "Simple Header & Footer Scripts Wiki")

[Support Forum](http://wordpress.org/support/plugin/simple-header-footer-scripts "Support Forum")

###Changelog

***1.0***
* Inital Release
