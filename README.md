addons-source [![Build Status](https://travis-ci.org/gramps-project/addons-source.svg?branch=master)](https://travis-ci.org/gramps-project/addons-source)
=============

Source code of contributed Third-party addons for the Gramps genealogy program.

To develop your own addon:

* https://gramps-project.org/wiki/index.php?title=Addons_development

Usage
=====

Use `make.py` for Gramps addons.

Clone both this repository and the addon repository if you intend to rebuild the addon

https://github.com/gramps-project/addons

Once you use the comands below the version number will be incremented and the resulting
files will be in the second addon repository to be commited.

Examples:
* Creates the initial addon-source directories for the addon.
```
python3 make.py gramps50 init AddonDirectory
```

* Creates the initial empty `AddonDirectory/po/fr-local.po` file for the addon.
```
python3 make.py gramps50 init AddonDirectory fr
```

* Updates `AddonDirectory/po/fr-local.po` with the latest translations.
```
python3 make.py gramps50 update AddonDirectory fr
```

* Build `../download/AddonDirectory.addon.tgz`
```
python3 make.py gramps50 build AddonDirectory
```

* Create or update the listing entry for your addon
```
python3 make.py gramps50 listing AddonDirectory
```

Valid command summary
=====================

* **clean** - Removes unnecessary files(template.pot/ locale etc) from the addon

* **init** - Get all of the strings from the addon and create template.po

* **update** - Updates the template.po file

* **compile** [subcomand: **all**] - Compiles the template.po file into 

* **build**  [subcomand: **all**] - Builds the addon for release

* **manifest-check** - Checks if all files are correct in addon release file?

* **unlist** - Unlist the addon from the listing

* **fix**  - If the listing shows a repeated addon entry, fix it

* **check** - Checks if the addon listing matches the addon download version or if missing from the listing

* **listing** [subcomand: **all**] - Builds/Creates a listing for the addon in each supported language

* **as-needed** [no other parameters] - Builds/Lists/Cleans only out of date addons in one step


