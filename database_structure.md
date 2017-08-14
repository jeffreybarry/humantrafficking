
## H2 Database Structure/Construction

This document is focused on the development of the Wordpress site and is intended for team members working on Wordpress infrastructure. Document initially drafted by Brooke Bergentzal at ILiADS 8/17.

We are using two key plugins to create a new post type and show fields:
[Advanced Custom Fields (ACF)](https://www.advancedcustomfields.com/)
[Pods - Custom Content Types and Fields (Pods)](https://pods.io/)

Pods is being used to create new post types and new taxonomies:
Database Entries - used to create the database entry post type and populate fields that are available to all formats (summary description, subject, display text)
Glossary Entries - used to create a new post type to create the site glossary
Format Taxonomy - applied to database entries to determine which fields should be applied to the entry

ACF is being used to extend the Database Entries post type created by Pods. ACF is able to display fields using conditional logic; when a user indicates that they’re inputting video, ACF will display the fields that pertain to that format.

ACF is added to the mix solely for its conditional display logic. Using ACF also means creating theme templates for display instead of using Pods’ built-in template creation--this gives the developer a little more control over display because they’re able to write in PHP instead of limited to the Pods template creator. Alternately, a new post type could be created for each format and output could be controlled through the Pods template creator; were limited Wordpress development experience or help available, that’s the path Brooke would recommend.
