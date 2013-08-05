# Project Boilerplate Guidelines

Basic rules-of-thumb for coding and setup

---

## Installation

1. Download, clone, fork... whatever the cool kids do these days
2. Add project to Codekit
3. Once added, right-click on project and go to 'Project Settings > Apply project defaults from file...'
4. Select the file 'codekit-config.json'

## Usage

As much as possible, try to stick with the following structures

### SASS

* __normalize.scss_
	* Avoid modifying unless a style consistently interferes with desired results

* __variables.scss_
	* All Sass variables

* __typography.scss_
	* Define what links, headers, etc. look like
	* Also try keeping any font related styles and coloring in this doc

* __font-awesome.min.scss_
	* Permits the use of the _font awesome_ icon font
	* Requires that the font files in the _font_ folder also be included

* _screen.css_
	* The previous css files are pulled into this one
	* Global Styles - Buttons, Lists, Clear Float/Fix, Tooltips, etc.
	* Header Styles
	* Footer Styles
	* Main Styles - general layout like wrappers, sidebars, etc.
	* From here on, divide sections by page

### Kits

HTML is written in _.kit_ files

* _partials_ folder for pieces to be included in other files such as header and footer
* _header.kit_ contains the some of the basics. Also if there is a consistent wrapper on most pages, it should open here.
* _footer.kit_ does not close the body or html but should contain typical footer items like nav, copyright, etc.
* _sample.kit_ is an example of what a typical page may look like. Already contains links to common js libraries.

### Javascript
* Vendor plugins intended for the _<head>_ section of the page are stored in the _js/vendor_ folder and are concatenated automatically to the _vendor-min.js_ file by adding their filenames to the _vendor.js_ file. This convention assumes the use of minified plugins.
* Vendor plugins that are to be loaded at the bottom of the page are also stored in the _js/vendor_ folder, but their filenames should be added to the top of the _scripts.js_ file. Again, this convention assumes the use of minfied plugin code.
* _app.js_ is where the Knockout code should be written
* _screen.js_ should contain all self written jQuery code. The "document ready" is already there so no need to add another one.
* The two files are then concatenated and minified. This can be prevented during development to assist in debugging.


## Tool/Software Recommedations

###### [CodeKit](http://incident57.com/codekit/ "CodeKit")
* Compiles, combines, minifies, reloads... Just use it.

###### [MAMP](http://www.mamp.info/en/index.html "MAMP")
* Not required for this boilerplate, but a local server may be needed down the line.

###### [Sublime Text](http://www.sublimetext.com/ "Sublime Text")
* Our text editor of choice.
* Here are some recommended packages to install:
	* [Sublime Package Control](http://wbond.net/sublime_packages/package_control "Sublime Package Control")
	* BracketHighlighter
	* ColorPick
	* Emmet
	* jQuery
	* Markdown Preview
	* Sass
	* SidebarEnhancements
	* Sublime-KnockoutJS-Snippets
	* SublimeCodeIntel
	* SublimeLinter

###### [Versions](http://versionsapp.com/ "Versions")
* Source control used to work with Subversion

###### [Kaleidoscope](http://www.kaleidoscopeapp.com/ "Kaleidoscope")
* Comparison tool


## General Things to follow

##### HTML

1. **Less is more.** Avoid adding elements to HTML when the same can be done with CSS. This prevents cross-browser issues, conflicts when integrating into back-end, and also removes overall clutter.

2. **Avoid ID's.** Classes should be used when there is a need to target something for CSS. Back-end code will sometimes add dynamic ID's to important elements. Sticking with classes prevents conflicts in case that needs to be done.

3. Putting a block-level element inside an inline element may still work in some smarter browsers, but will make others go berserk.

4. **Links vs. Buttons** If clicking on an element will eventually submit user info to the server, use a button or input[type="submit"]. If that element is only meant to bring the user to another page, use an 'a' tag.

5. **Check with Engineers ahead of time.** For any non-static components of a web page, check with the developer to see if there are any requirements or expectations.

##### CSS

1...
