# Introduction

The `HTML-ApLo.tmbundle` TextMate2 bundle provides support for a semi-automatic HTML Preview:

![ApLo HTML Preview](https://github.com/gknops/HTML-ApLo.tmbundle/raw/master/ApLo-HTML-Preview.png)

By default it is tied to the `callback.document.did-save` semantic class and the `text.html, source.css and source.js` scopes, so it can update the preview whenever one of these file types is saved.

It requires [*ApLo.tmbundle*](https://github.com/gknops/aplo.tmbundle).

**NOTE**: if the `HTML_APLO_PREVIEW_FILE` variable has to be set in a `.tm_properties` file for the preview to work when JavaScript or CSS files are saved.

**NOTE**: this bundle does NOT replace the standard HTML bundle, you still need that for the language definition etc.


# Installation

Open a terminal window and enter these commands:

	cd ~/Library/Application\ Support/Avian/Bundles
	git clone git://github.com/gknops/HTML-ApLo.tmbundle.git


# .tm_properties variables

To enable this plugin some variables need to be defined in a `.tm_properties` file, either in the project directory, one of it's subdirectories or anywhere else `.tm_properties` files are allowed at.



## HTML\_APLO\_PREVIEW\_FILE

This variable should contain the full path to a HTML file. When set, Saving any HTML, CSS or JavaScript file within the directories governed by the `.tm_properties` file will cause the Preview for the file defined in the variable to be updated.

## HTML\_APLO\_PREVIEW\_NO\_AUTO

By default the bundle will show a preview of any HTML file saved. To suppress this define the `HTML\_APLO\_PREVIEW\_NO\_AUTO` and set it to a non-empty string. For example adding

	HTML_APLO_PREVIEW_NO_AUTO	= "anything"

to the `.tm_properties` file in your home directory will disable HTML preview for any HTML file unless `HTML\_APLO\_PREVIEW\_FILE` is defined.

## HTML\_APLO\_WINDOW\_TITLE

With this optional variable you can control the window title of the preview window. If not set, the window name will default to the name of the project, suffixed by *HTML Preview*.
 