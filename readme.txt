=== TransDeluxe ===
Tags: translator, multilanguage, automatic translator, google translations, babelfish, promt, free translations, multilingual
Author: TransDeluxe
Contributors:
Donate link:
Requires at least: 2.3
Tested up to: 3.0.1
Stable Tag: 1.3.3

Automatically translates your blog in 48 different languages!

== Description ==

TransDeluxe automatically translates your blog in the following 48 different languages:
Italian, Korean, Chinese (Simplified), Portuguese, English, German, French, Spanish, Japanese, 
Arabic, Russian, Greek, Dutch, Bulgarian, Czech, Croatian, Danish, Finnish, Hindi, Polish, Romanian, 
Swedish, Norwegian, Catalan, Filipino, Hebrew, Indonesian, Latvian, Lithuanian, Serbian, Slovak, 
Slovenian, Ukrainian, Vietnamese,Albanian,Estonian,Galician,Maltese,Thai,Turkish,Hungarian.

The number of available translations will depend on your blog language and the translation engine you will chose to use.
Main features:

* **Four different translation engines**: Google Translation Engine, Babel Fish, Promt, FreeTranslations
* **Search Engine Optimized**: it uses the permalinks by adding the language code at the beginning of all your URI. 
	For example the english version on www.domain.com/mycategory/mypost will be automatically transformed in 
	www.domain.com/en/mycategory/mypost 
* **Fast Caching System**: new fast, smart, optimized, self-cleaning and built-in caching system. Drastically reduction of the risk of temporarily ban from translation engines. 
* **Fully configurable layout**: you can easily customize the appearance of the translation bar by choosing between a TABLE 
	or DIV layout for the flags bar and by selecting the number of translations to make available to your visitors 
* **No database modifications**: TransDeluxe is not intrusive. It doesn't create or alter any table on your database: this feature permits to obtain better performances.

**TransDeluxe is one of the first real (and free) traffic boosters for your blog!**
It can help you to reach a lot of new users and consequently to strongly increase your popularity: if you derive some benefits and if you want to support the development, 
please consider to support me with a donation.

For the latest information and changelog visit the website

http://www.transdeluxe.com


== Installation ==

1. 	Upload the folder "transdeluxe" to the "wp-content/plugins" directory.
2. 	Activate the plugin through the 'Plugins' menu in WordPress. 
3.	From the main menu choose "Options->TransDeluxe" and select your blog language and your preferred configuration options then select "Update Options".

== Configuration ==

If your theme is widged-enabled, just choose "Presentation->Widgets" from the administration main menu
and drag the "TransDeluxe" widget on the preferred position on your sidebar.
If your theme is not widgetized, just add the following php code (usually to the sidebar.php file):  

<?php if(function_exists("gltr_build_flags_bar")) { gltr_build_flags_bar(); } ?>

After this simple operation, a bar containing the flags that represents all the available translations 
for your language will appear on your blog.

== Changelog ==

= 1.3.3 =
* This is the first release of TransDeluxe.

== Frequently Asked Questions ==

= The full translation process takes a lot of time. Why? =

In order to prevent from banning by the translation services, only a translation request every 5 minutes will be allowed. This will permit to fully translate
your blog whithout any interruption; this message will completely disappear when all the pages of your blog will be cached.
Remember that this message will also appear if you're currently being banned by the translation engine: this could happen if for example your blog shares the
same ip address with other blogs using older versions of TransDeluxe.

= When I click on a flag I'm just redirected to Google Translation Services =

Don't worry: this is just a TEMPORARY redirect which will disappear when the page will be cached and saved on your server: in fact, in order to avoid banning issues, the plugin translates and caches a page every 5 minutes

= "This page has not been translated yet. The translation process could take a while: please come back later." message when trying to access a translated page =

Upgrade to 1.0.8 or later. Starting from 1.0.8, a browser asking for a not yet translated page will be warned and redirected in 5 seconds to the translation service 
page in order to provide a temporary "backup translation service". Obviously, when the page is translated and saved on your cache directory, this redirection 
will disappear and the translated and cleaned page will be served by your blog. Starting from version 1.2.9, this message has been removed

= When clicking on a translation flag the page doesn't translate =

This could be due to a change of the permalinks structure of your blog, to a conflict with another plugin or to a custom 
.htaccess file which doesn't permit TransDeluxe to add its custom permalink rules. Try to refresh the TransDeluxe 
rewrite rules just pressing the "Update Options" button from the TransDeluxe admin page. If the problem persists, 
try also to deactivate all the other existing plugins and check your .htaccess file and comment out all the non-standard rewrite rules. 
If you discover a conflicting plugin please contact us.

= The translated page has a bad/broken layout =

This is due to the translation engine action. I cannot do anything in order to prevent this problems :-)
I suggest you to try all the translation engines in order to choose the best one for your blog layout

= I've just changed my permalinks structure or just upgraded Wordpress to a newer version and TransDeluxe doesn't translate anymore =

Everytime the permalinks structure of your blog changes, the custom rules previously added by TransDeluxe are overriden.
To solve the problem you must just refresh the TransDeluxe Options ("Update Options" button) on the administrative area.

= I've removed one or more available translations but the search engines continue to try to index the corresponding urls =

When you remove one or more translations, the plugin will begin to return a 404 Not Found for all the corresponding translated pages.
In order to notify a search engine that one or more urls are not available anymore you should add a deny rule on your robots.txt file.
For example if you decide to remove the German translation you should modify your robots.txt as follows:
User-agent: *
[....]
Disallow: /de/*

= How can I discover if my blog is currently banned by the translation engine? =

Go to the TransDeluxe admin page. If your blog has been temporarily banned, a warning message will appear inside the "Translation engine connection" section.

= I've just removed the plugin. How to fix all the SEO issues related to the translated pages which are not jet available? =
Put a rewrite rule like this on your .htaccess:
RedirectMatch 301 ^/(it|ko|zh-CN|zh-TW|pt|en|de|fr|es|ja|ar|ru|el|nl|zh|zt|no|bg|cs|hr|da|fi|hi|pl|ro|sv|ca|tl|iw|id|lv|lt|sr|sk|sl|uk|vi|sq|et|gl|mt|th|tr|hu|be|ga|is|mk|ms|fa)/(.*)$ http://www.mysite.com/$2

