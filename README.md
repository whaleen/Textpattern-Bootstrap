txtstrap
========

Textpattern on Twitter Bootstrap, or the other way around.


## Install

1. Install [Textpattern](http://textpattern.com/).
2. Drop [/texstrap](https://github.com/whaleen/txtstrap) in the root directory of your Textpattern project.
3. Install Textpattern plugin [cnk_versioning](https://gist.github.com/4128491) and edit it's source to point to [/txtstrap/_templates](https://github.com/whaleen/txtstrap/tree/master/_templates) 



## /textrap directories explained

### /_templates

Textpattern templates are made up of pages, forms, and css*, all of which can essentially be thought of as files and can be edited as such from within this _templates folder using your favorite editor. This wouldn't be possible with the Textpattern plugin cnk_versioning. Textpattern pages, forms, and css in default Textpattern installations are stored in the database and are meant to be editable from the Textpattern admin interface which is not conducive to coding in your own familiar environment, hence the necessity to use cnk_versioning which bridges the gap between the default database storage of said 'files' and the external 'file' system we are using here in /_templates.

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

The only mandatory plugin for using txtstrap as it is out of the box is cnk_versioning.