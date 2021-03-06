# anna_themify_base_child

This is a very basic child theme - the files are almost universal. So you can use them as a starting point for any child theme for *WordPress*. 

## style.css

In order to use the files as child of another *mother theme* edit style.css:

~~~~
/*
 Theme Name:   GIVE YOUR CHILD THEME A NAME HERE
 Theme URI:    https://wordpress.org/themes/themify-base/
 Description:  DESCRIBE YOUR THEME IN A FEW WORDS HERE.
 Author:       ENTER YOUR NAME HERE
 Author URI:   http://YOURWEBSITE-HERE.OK
 Template:     NAME-OF-THE-MOTHER-THEME
 Version:      0.0
 License:      ADD A LICENCE. 
 License URI:  http://LICENCE.DK
 Tags:         TAG1, TAG2, TAG3
 Text Domain:  CHILD-OF-MOTHER-THEME
*/
~~~~

## functions.php

Is the brain behind your theme. Here you can do all sorts of stuff. But in a child theme the most important thing must be to add the mother theme styles:

~~~~
/* add stylesheets */
add_action( 'wp_enqueue_scripts', 'theme_enqueue_styles' );

function theme_enqueue_styles() {
    wp_enqueue_style( 'Mother Stylesheet', get_template_directory_uri() . '/style.css' );
	// add whatever scripts and stylesheets needed
}
~~~~

In the function you can add scripts via *wp_enqueue_script()*

## index.php and all other files

If you want to modify a file, you have to copy the original file from the mother theme folder to the child theme folder. In the child theme folder you can edit the file. Should the mothertheme update all files, the files in the child theme folder remain the same. You may want to change functionality in e.g.:

* index.php - display the blog
* single.php - display single posts
* page.php - display a page

## screenshot.png

You may want to have a nice image of your design in Appearance / Themes. Add a screendump of your theme or similar here. The screenshot for the *twentyfifteen* and the most recent versions of the standard *WordPress* theme is *800x660 px*.

## Read on

Goto: [Codex page on child themes](https://codex.wordpress.org/Child_Themes).
