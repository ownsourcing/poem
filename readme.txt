------------
 Overview
------------
 
This example module was written by Bryan Hirsch to serve as an introductory-level exercise in using the Twig theme engine. (Twig is the new default theme engine in Drupal 8 core.) Use the code in this module to learn to develop a .twig file to replace an existing .tpl.php file (.tpl.php is the file format for PHPTemplate, the default theme engine of Drupal core since 4.7).

This example and related exercises will be added to drupalladder.org; check there for the latest versions.

------------
 Instructions for setting up the exercise
------------

If you need more information, most of these brief instructions are explained in more detail below.
 
1) Install and launch Drupal 8 (step-by-step instructions available at drupalladder.org; link via shortened url: onso.us/local-d8)
2) Confirm the Bartik and Seven themes work normally on the site
3) Install the poem module
4) Navigate to the poem page (example.com/poem) and fill out the form; when you submit the form, you'll see the results printed at the top of the page

------------
 Instructions for translating poem-prose.tpl.php files into poem-prose.twig. 
------------
 
1) Locate poem-prose.tpl.php in the poem/template directory
2) Rename poem-prose.tpl.php to poem-prose.twig
3) Clear caches and re-submit the poem form; you will see the first set of differences
2) Open the newly named poem-prose.twig and remove vestiges of PHP; indicate variables with double curly brackets --e.g. $roses becomes {{ roses }}

------------
 Additional details on instructions
------------

2) Confirm the Bartik and Seven themes work normally on the site
3) Install the poem module
4) Navigate to the poem page (example.com/poem) and fill out the form; when you submit the form, you'll see the results printed at the top of the page
 
------------
 Additional resources
------------
 
IRC channel #drupal-twig

------------
 TODO
------------

Add additional details to instructions
  a - Navigate to the modules directory
  b - Using the following command: git clone git://github.com/ownsourcing/poem.git
3) Add the poem module to the /modules directory

Update instructions regarding translation once approach has been finalized by Twig team. 
Latest discussion 2012-12-04
10:26:01 AM JohnAlbin: kay_v: Check the footer section of http://drupalcode.org/sandbox/pixelmord/1750250.git/blob/refs/heads/front-end:/core/themes/stark/templates/comment/comment.html.twig
10:26:12 AM kay_v: JohnAlbin: will do
10:26:31 AM kay_v: much appreciated! (been scratching my scalp to the point of lacerations ...)
10:28:23 AM Fabianx: kay_v: Can also use:
10:28:48 AM Fabianx: {{ 'My string: @var' | t({'@var': var})
10:28:55 AM Fabianx: for more complicated cases.
mikestewart [~mikestewa@pool-108-13-149-180.lsanca.fios.verizon.net] entered the room. (10:29:13 AM)
10:29:25 AM Fabianx: kay_v: Twig also has native i18n support as a "real" filter, but we are not supporting that right now.
10:29:55 AM kay_v: thanks Fabianx - will post a link to Ladder writeup here. It would be great to have someone give it a glance to confirm I've not made a mess of it 
10:31:12 AM GaborHojtsy: JohnAlbin: Fabianx: is it safe to say anything before a "| t(…." is a translatable string?
10:31:28 AM Fabianx: GaborHojtsy: yes
10:31:30 AM GaborHojtsy: JohnAlbin: Fabianx: do you support format_plural() and/or context in any way?
10:31:41 AM Fabianx: GaborHojtsy: 'x' | t(...) is translated to:
10:31:49 AM Fabianx: t('x', ...)
10:31:54 AM Fabianx: ( internally )
10:31:58 AM Fabianx: GaborHojtsy: not yet.
10:32:04 AM Fabianx: GaborHojtsy: I could expose that function though.
10:32:41 AM JohnAlbin: GaborHojtsy: I'm not sure that format_plural() is used in  any D7 .tpl.php templates. (Doesn't mean we shouldn't support it in twig.)
10:33:19 AM Fabianx: We might think to switch to: http://twig.sensiolabs.org/doc/extensions/i18n.html though, but I don't know how that would be compatible with translate.drupal.org.

