txtstrap
========

Twitter Bootstrap for Textpattern.

## Demo

Demo at [http://joshuavaage.com/projects/txtstrap](http://joshuavaage.com/projects/txtstrap): All section use the default.txp page template. There are a handful of fake articles posted for the purpose of having example content. 

### Theme?

This is not a theme per se. It is meant for fresh installs by designers and developers who generally begin a Textpattern project with empty pages and forms.

It does have a few components that a designer will be able to use right off. Namely the responsive scaffolding, a navigation bar, a series of 'content-goes-here' blocks, and a footer. The 'content-goes-here' blocks are set up to illustrate the way in which all div elements will tile throughout your responsive design. They are also meant to be placeholders for calling forms via the txp:output_form tag. Try some out. Develop some to your purpose. Delete the unused. Rearrange the furniture.

## Start Your Designering with Textpattern Forms


### Forms with the prefix *snip_* (snip_breadcrumbs, snip_fixed_navigation, etc…) 

These little pieces are called variously with the txp:output_form tag into the div element of your choice. They each have a minimum purpose and are meant to be the barest of building blocks... common things you might need.

###Forms with the prefix *txtstrap_* (txtstrap_head, txtstrap_default, txtstrap_footer, etc…)

Forms with this prefix are also written for the minimum purpose and that is to render the scafollding for each section. In the default page template _templates/pages/default.txp, there is a txp:if_section conditional and a form to output for the corosponding form (textstrap_default.txp, textstrap_about.txp, textstrap_articles.txp, etc... ). Go forth and thrash...

## Install

1. Drop [/texstrap](https://github.com/whaleen/txtstrap) in the root directory of your Textpattern project.
2. Install Textpattern plugin [cnk_versioning](https://gist.github.com/4128491) and edit the path in it's source to point to [/txtstrap/_templates](https://github.com/whaleen/txtstrap/tree/master/_templates). Follow cnk_versioning's own instructions if you are not already familiar with how it works.
3. Sally forth.


## /textrap directory contents

### [/_templates](https://github.com/whaleen/txtstrap/tree/master/_templates)

* /css (to be ignored)
* [/forms](https://github.com/whaleen/txtstrap/tree/master/_templates/forms)
* [/pages](https://github.com/whaleen/txtstrap/tree/master/_templates/pages)

/pages and /forms are where the templating work starts. Ignore the /css directory as the CSS used in the templates is placed outside of the database in various directories - see [/txtstrap/_templates/txtstrap_head.misc.txp](https://github.com/whaleen/txtstrap/blob/master/_templates/forms/txtstrap_head.misc.txp)

### [/assets](https://github.com/whaleen/txtstrap/tree/master/assets)

* [/bootstrap](https://github.com/whaleen/txtstrap/tree/master/assets/bootstrap)
* [/fitttext](https://github.com/whaleen/txtstrap/tree/master/assets/fittext)
* [/font-awesome](https://github.com/whaleen/txtstrap/tree/master/assets/font-awesome)
* [/headsupgrid](https://github.com/whaleen/txtstrap/tree/master/assets/headsupgrid)
* [/jquery](https://github.com/whaleen/txtstrap/tree/master/assets/jquery)
* [/sharre](https://github.com/whaleen/txtstrap/tree/master/assets/sharre)

All references to these assets are in the the /_templates/forms/head.misc.txp and /_templates/forms/footer.misc.txp forms. Therefore, any changes to the directory structure for your projects will only require updating those paths in order for txtstrap to still work on a drag-and-drop basis.

### [/resources](https://github.com/whaleen/txtstrap/tree/master/resources)

* [/txp-plugins](https://github.com/whaleen/txtstrap/tree/master/resources/txp-plugins)

A collection of plugins which are required by certain Textpattern usage examples. The required plugins are noted prominently in the template code.