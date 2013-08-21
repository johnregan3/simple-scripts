=== Simple Scripts ===
Contributors: johnregan3
Donate Link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=BAG2XC69ZYADQ
Tags: custom scripts, custom, scripts, javascript, google, analytics, google analytics, header, footer
Requires at least: 3.0.1
Tested up to: 3.6
Stable tag: trunk
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Add Custom Scripts (like Google Analytics) to your WordPress site without any hassles.

== Description ==

An easy-to-use WordPress Plugin to add custom scripts (like Google Analytics) to your website's header and/or footer.  Great for Administrators who don't want to store their custom scripts in a theme's options.  These fields will remain even if the theme is changed.

**Features**

- No configuration needed, just enter your JavaScript(s).
- Scripts print after enqueued scripts (like jQuery) are rendered
- Simple interface built on WordPress UI
- Virtually no impact on site performance
- Uses no JavaScript files or complicated database queries
- Generates no files
- Extremely lightweight (~8KB)
- Thorough Documentation

== Installation ==

Install Simple Scripts just as you would any other WP Plugin:

1.  [Download Simple Scripts](http://wordpress.org/plugins/simple-scripts/ "Download Simple Scripts") from WordPress.org.

2.  Unzip the .zip file.

3.  Upload the Plugin folder (simple-scripts/) to the wp-content/plugins folder.

4. Go to [Plugins Admin Panel](http://codex.wordpress.org/Administration_Panels#Plugins "Plugins Admin Panel") and find the newly uploaded Plugin, "Simple Scripts" in the list.

5. Click "Activate Plugin."

[More help installing Plugins](http://codex.wordpress.org/Managing_Plugins#Installing_Plugins "WordPress Codex: Installing Plugins")

== Frequently Asked Questions ==

Find more help at the [Simple Scripts Wiki](https://github.com/johnregan3/simple-scripts/wiki "Simple Scripts Wiki")

= Will this Plugin work on my WordPress.com website? =

Sorry, this plugin is available for use only on self-hosted (WordPress.org) websites.

= How do I install Google Analytics on my website? =

First of all, you'll need to set up a [Google Analytics](http://www.google.com/analytics/ "Google Analytics") account to get a [tracking code](https://support.google.com/analytics/answer/1008080?hl=en).

Then, you'll paste that tracking code into the plugin's Footer Scripts textarea.  it will look something like this:

    var _gaq = _gaq || [];
    _gaq.push(['_setAccount', 'UA-XXXXX-Y']);
    _gaq.push(['_trackPageview']);
    (function() {
    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
    })();

Remember, don't include the &lt;script&gt;&lt;/script&gt; tags.  They're already printed into the page by Simple Scripts.

Now, you're done!

= Can I use this to print CSS into my header? =

Unfortunatley, because it prints your scripts between &lt;script&gt;&lt;/script&gt; tags, your CSS will not display corretly.  However, it is recommended that you use the [Simple Custom CSS Plugin](http://wordpress.org/plugins/simple-custom-css "Simple Custom CSS Plugin") for adding CSS to your website.

= Why aren't my scripts working? =

It's important to note that this plugin simply prints your scripts into your posts/pages; it does nothing to modify or execute the scripts.

***If the scripts are being printed into the page, the plugin is functioning correctly.***  If you're having problems, first check the source of your page in the browser.  Ensure that the scripts are printing into the header/footer as you have entered them.  Unfortunately, if they are being printed but still not working, there is an error within the script, or perhaps in the order in which they are being loaded into the page.

The author is ready and willing to help users and fix problems with this plugin, but ***because this is a free plugin, the author is unable to help debug JavaScript errors.***  You may need to seek help with the scripts in places like the [WordPress Support Forums](http://wordpress.org/support/ "WordPress Support Forums) or [Stack Overflow](http://stackoverflow.com, "Stack Overflow").

= Why is my website broken/blank? =

This is most likely an issue with the javascript, not the plugin.  Ensure you have closed all of your brackets and parentheses and used semicolons where appropriate.  Keep in mind that the easiest way to get your site back online is to delete the javascript you've entered into the Simple Scripts textareas.

= I'm having problems with jQuery.  What's going on? =

To prevent compatibility problems, [WordPress natively sets jQuery to noConflict() mode](http://codex.wordpress.org/Function_Reference/wp_enqueue_script#jQuery_noConflict_Wrappers).  This means that the '$' doesn't work, unless you specifically enable it.  Here, you have two options:

Simply use 'jQuery()' where you would use '$()'.

Or, wrap your jQuery like so:

    (function($) {
    // Inside of this function, $() will work as an alias for jQuery()
    // and other libraries also using $ will not be accessible under this shortcut
    })(jQuery);

Also, if your script isn't running, you may need to wrap your script in a jQuery(document).ready function.

== Screenshots ==

1. The Simple Scripts Administration Screen

== Changelog ==

= 1.0 =
* Inital Release

== Upgrade Notice ==

= 1.0 =
Inital Release
