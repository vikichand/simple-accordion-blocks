=== Simple Accordion Blocks ===
Contributors: vikichand
Author URI: https://vikash.ch/
Donate Link: https://vikash.ch/
Tags: accordion, accordions, gutenberg, blocks, responsive
Requires at least: 5.4
Tested up to: 5.7.2
Requires PHP: 5.6
Stable tag: 1.1.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Gutenberg block for creating responsive accordion drop-downs.

== Description ==

Simple Accordion Blocks is a simple plugin that adds a Gutenberg block for adding accordion drop-downs to your pages.

The accordions should blend seamlessly with your theme. However, you may want to add custom styles to your theme.

= Features =

* Adds a Gutenberg block for adding accordions to your site.
* Supports multiple accordions with individual settings for each accordion item.
* Fully responsive.
* Support for item IDs and direct links.
* Accessible (for users requiring tabbed keyboard navigation control).

= Optional Features =

* Open individual accordion items by default.
* Disable auto closing of accordion items.
* Manually close items by clicking the title again.
* Scroll page to title when it's clicked open (including setting a scroll offset position).
* Set the HTML heading tag for the title element (h1–h4, button).
* Set defaults to be applied to all new accordion items or reset a specific accordion item to the defaults.
* Supports adding custom block styles using `wp.blocks.registerBlockStyle`.

= Output =

The plugin will ultimately output following HTML (simplified for this example):

    <div class="wp-block-vc-accordion-item v-accordion__item js-accordion-item" data-initially-open="false" data-click-to-close="true" data-auto-close="true" data-scroll="false" data-scroll-offset="0">
        <h2 id="at-1612" class="v-accordion__title js-accordion-controller" tabindex="0" role="button" aria-controls="av-1612" aria-expanded="false">
            Title with H2 tag
        </h2>
        <div id="av-1612" class="v-accordion__content" style="display:none" aria-hidden="true">
            <p>Content</p>
        </div>
    </div>

= Custom CSS =

You can use the following CSS classes to customize the look of the accordion.

    .v-accordion__item {} /* The accordion item container */
    .v-accordion__item.is-open {} /* is-open is added to open accordion items */
    .v-accordion__item.is-read {} /* is-read is added to accordion items that have been opened at least once */
    .v-accordion__title {} /* An accordion item title */
    .v-accordion__title--button {} /* An accordion item title that is using a `<button>` tag */
    .v-accordion__title:hover {} /* To modify the style when hovering over an accordion item title */
    .v-accordion__title:focus {} /* To modify the style when an accordion item title currently has broswer focus */
    .v-accordion__content {} /* An accordion item content container */

== Installation ==
1. Upload the 'simple-accordion-blocks' folder to the '/wp-content/plugins/' directory.
2. Activate the plugin through the Plugins menu in WordPress.
3. Add the accordions to your content.

== Frequently Asked Questions ==

= Can I change all my existing accordion items to the defaults? =

No. It is not possible to change all your accordion item's settings (within the same page or across multiple pages) to the defaults.

Although I would like to offer this feature, based on my research it would require a significant amount of development time that I am unable to devote to a free plugin. If you are a developer and would be interested in helping implement a feature like that, please let me know.

= Why isn't the JavaScript file loading on my site? =

This is most likely caused by a poorly coded theme. This plugin makes use of the `wp_footer()` function to load the JavaScript file and it's dependancy (jQuery). Check your theme to ensure that the `wp_footer()` function is being called right before the closing `</body>` tag in your theme's footer.php file.

= Issues/Suggestions =

For bug reports or feature requests or if you'd like to contribute to the plugin you can check everything out on [Github](https://github.com/vikichand/#/).

== Screenshots ==

1. Accordion block settings sidebar
2. Accordion block in the editor

== Changelog ==
= 1.0.0 =
* ALL NEW plugin to support the new WordPress Gutenberg editor.

= 1.1.0 =
* Tested ready for WordPress 5.7.0+

== Upgrade Notice ==

= 1.1.0 =
* Tested ready for WordPress 5.7.0+