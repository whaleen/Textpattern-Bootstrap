txtstrap
========

Twitter Bootstrap for Textpattern.

## Demo

Demo at [http://joshuavaage.com/projects/txtstrap](http://joshuavaage.com/projects/txtstrap): All section using the default.txp page template. There are a handful of fake articles posted for the purpose of having example content. 

### Theme?

This is not a theme per se. It is meant for fresh installs by designers and developers who generally begin a Textpattern project with empty pages and forms.

It does have a few components that a Textpattern designer will be able to use right off. Namely, responsive scaffolding, a navigation bar, a series of 'content-goes-here' blocks, and a footer. The 'content-goes-here' blocks are set up to illustrate the way in which all div elements will tile throughout your responsive design. They are also meant to be placeholders for calling forms via the txp:output_form tag. Try some out. Develop some to your purpose. Delete the unused.

### Forms with the prefix *snip* (snip_breadcrumbs, snip_fixed_navigation, etc…) 

These little pieces are called variously with the txp:output_form tag into the div element of your choice. They each have a minimum purpose and are meant to be the barest of building blocks.

###forms with the prefix *txtstrap* (txtstrap_head, txtstrap_default, txtstrap_footer, etc…)

Forms with this prefix are more geared toward the structural future of your design and as such are also written for the minimum purpose.

## Install

1. Drop [/texstrap](https://github.com/whaleen/txtstrap) in the root directory of your Textpattern project.
2. Install Textpattern plugin [cnk_versioning](https://gist.github.com/4128491) and edit the path in it's source to point to [/txtstrap/_templates](https://github.com/whaleen/txtstrap/tree/master/_templates). Follow cnk_versioning's own instructions if you are not already familiar with it.
3. 


## /textrap directories explained

### /_templates

* /css
* /forms
* /pages

Textpattern templates are made up of pages, forms, and css*, all of which can essentially be thought of as files and can be edited as such from within this _templates folder using your favorite editor. This wouldn't be possible with the Textpattern plugin cnk_versioning. Textpattern pages, forms, and css are stored in the database and are meant to be editable from the Textpattern admin interface. This is not conducive to coding in your own familiar environment, hence the necessity to use cnk_versioning. It bridges the gap between the default database storage of said 'files' and the external 'file' system we are using here in /_templates.

* All references to stylesheets in the template files are references to external css files (bootsrap.css, font-awesome.css, etc…). Only pages and forms will be "synced" with cnk_versioning to the database where they are available to Textpattern for producing your views.

### /assets

* /bootstrap
* /font-awesome
* /headsupgrid
* /jquery
* /prettify

All references to these assets are in the the /_templates/forms/head.misc.txp and /_templates/forms/footer.misc.txp forms. Therefore, any changes to the directory structure for your projects will only require updating those paths in order for txtstrap to still work on a  drag-and-drop basis.

### /resources

* /txp-plugins

A collection of plugins which are required by certain Textpattern usage examples. For instance, the Textpattern plugin mem_self_register gives us a tag which allows us to put a sign-up form in a page. The required plugins are noted in the template code.