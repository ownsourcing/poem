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
2) Open the newly named poem-prose.twig and remove 

------------
 Additional resources
------------
 
IRC channel #drupal-twig

------------
 TODO
------------

Update instructions regarding translation once approach has been finalized by Twig team.


  a - Navigate to the modules directory
  b - Using the following command: git clone git://github.com/ownsourcing/poem.git
3) Add the poem module to the /modules directory
