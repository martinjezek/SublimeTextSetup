# Sublime Text 2 - Setup

> A few thoughts how to set up Sublime Text editor.

## Package Control

The Sublime Text package control manager that makes it exceedingly simple to find, install and keep packages up-to-date.

- [Package Control][PackageControl]
- [Package Control - Install][PackageControlInstall]

Install:

- Open `Sublime Text 2`. The console is accessed via `View > Show Console` menu.
- Once open, paste the `Python code` and hit enter.

```python
import urllib2,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')
```

How to use:

- `Ctrl+Shift+P`
- `Package Control`

## Synced Side Bar

Plugin to sync project sidebar (folder view) with currently active file.

- [Synced Side Bar - Package Control][SyncedSideBarPackageControl]
- [Synced Side Bar - GitHub][SyncedSideBarGit]

Install:

- `Ctrl+Shift+P`
- `Package Control: Install Package`
- `SyncedSideBar`

How to use:

- `Ctrl+Shift+P`
- `Side Bar: Enable/Disable Syncing`

## Soda Theme

Dark and light custom UI themes for Sublime Text.

- [Soda Theme - Package Control][SodaThemePackageControl]
- [Soda Theme - GitHub][SodaThemeGit]

Install:

- `Ctrl+Shift+P`
- `Package Control: Install Package`
- `Theme - Soda`
- `Sublime Text 2 > Preferences > Settings - User` 
- `c:/Users/Martin/AppData/Roaming/Sublime Text 2/Packages/User/Preferences.sublime-settings`
- `Extend Object settings`

```javascript
{
	"color_scheme": "Packages/User/Monokai Soda.tmTheme",
	"font_size": 11.0,
	"ignored_packages":
	[
		"Vintage"
	],
	"reveal-on-activate": true,
	"soda_classic_tabs": false,
	"soda_folder_icons": false,
	"theme": "Soda Dark.sublime-theme"
}
```

Syntax Highlighting Colour Schemes.

- [Soda Theme - Package Control][SodaThemeSyntaxHighlightingGit]

Install:

- `Unzip`
- `Copy new themes to Packages/User`
- `c:/Users/Martin/AppData/Roaming/Sublime Text 2/Packages/User/`
- `Apply the new theme Preferences > Color Scheme > User > Monokai Soda`

## JSHint

Plugin allowing you to check your JavaScript code for nasty errors, coding conventions and other goodies via Node.js. It relies on JSHint, a fork of JSLint. 

- [Node.js][node.js]
- [JSHint - Install][node-npm-jshint]
- [JSHint Gutter - Package Control][JSHintGutterPackageControl]
- [JSHint Gutter - GitHub][JSHintGutterGit]

Install Node.js to default path:

- `C:/Program Files/nodejs/`

Install JSHint via NPM:

- `$ npm install jshint -g`

Install JSHint Gutter:

- `Ctrl+Shift+P`
- `Package Control: Install Package`
- `JSHint Gutter`
- `c:/Users/Martin/AppData/Roaming/Sublime Text 2/Packages/JSHint Gutter/JSHint.sublime-settings`

```javascript
{
  // Simply using `node` without specifying a path sometimes doesn't work :(
  // https://github.com/victorporof/Sublime-JSHint#oh-noez-command-not-found
  // http://nodejs.org/#download
  "node_path": {
    "windows": "C:/Program Files/nodejs/node.exe",
    "linux": "/usr/bin/nodejs",
    "osx": "/usr/local/bin/node"
  },

  // Automatically lint on edit (Sublime Text 3 only).
  "lint_on_edit": false,

  // Configurable duration before re-linting.
  "lint_on_edit_timeout": 1,

  // Automatically lint when a file is loaded.
  "lint_on_load": true,

  // Automatically lint when a file is saved.
  "lint_on_save": true,

  // Highlight problematic regions when selected.
  "highlight_selected_regions": true,

  // Log the settings passed to JSHint from `.jshintrc`.
  "print_diagnostics": true
}
```
How to use:

- `Right Click > JSHint > ...`
- `Ctrl+Alt+J` Lint Code
- `Ctrl+Alt+C` Clear

Your own .jshintrc options:

The plugin looks for a [.jshintrc][.jshintrc] file in the same directory as the source file you're linting and, or one located recursively up one directory, all the way until the filesystem root. As well, it uses those options along the default ones.

See the documentation at jshint.com and a few [examples here][.jshintrc-examples].

## EditorConfig

EditorConfig helps developers define and maintain consistent coding styles between different editors and IDEs. The EditorConfig project consists of a file format for defining coding styles and a collection of text editor plugins that enable editors to read the file format and adhere to defined styles. EditorConfig files are easily readable and they work nicely with version control systems.

- [EditorConfig][EditorConfig]
- [EditorConfig - Package Control][EditorConfigPackageControl]
- [EditorConfig - GitHub][EditorConfigGit]

Install:

- `Ctrl+Shift+P`
- `Package Control: Install Package`
- `EditorConfig`
- `d:/code/myproject/`
- add file `.editorconfig`

```
# EditorConfig helps developers define and maintain consistent
# coding styles between different editors and IDEs
# editorconfig.org

root = true

[*]
indent_style = space
indent_size = 4

end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

[*.md]
trim_trailing_whitespace = false

[{package.json,bower.json}]
indent_size = 2
```

## Line Endings Unify

Line Endings Unify tool change files endings (Mac,Unix,Windows) to Unix (aka \n).

- [Line Endings Unify - Package Control][LineEndingsPackageControl]
- [Line Endings Unify - GitHub][LineEndingsGit]

Install:

- `Ctrl+Shift+P`
- `Package Control: Install Package`
- `Line Endings Unify`

How to use:

- `Ctrl+Shift+P`
- `Line Endings Unify`
- Input comma separeted file extensions which you want to change line endings `js,html,php`
- Execute the script

[PackageControl]: https://sublime.wbond.net/
[PackageControlInstall]: https://sublime.wbond.net/installation
[SyncedSideBarPackageControl]: https://sublime.wbond.net/packages/SyncedSideBar
[SyncedSideBarGit]: https://github.com/sobstel/SyncedSideBar
[SodaThemePackageControl]: https://sublime.wbond.net/packages/Theme%20-%20Soda
[SodaThemeGit]: https://github.com/buymeasoda/soda-theme/
[SodaThemeSyntaxHighlightingGit]: http://buymeasoda.github.com/soda-theme/extras/colour-schemes.zip
[node.js]: http://nodejs.org/
[node-npm-jshint]: http://www.jshint.com/install/
[JSHintGutterPackageControl]: https://sublime.wbond.net/packages/JSHint%20Gutter
[JSHintGutterGit]: https://github.com/victorporof/Sublime-JSHint
[.jshintrc]: https://github.com/victorporof/Sublime-JSHint#using-your-own-jshintrc-options
[.jshintrc-examples]: https://github.com/jshint/jshint/blob/master/examples/.jshintrc
[EditorConfig]: http://editorconfig.org/
[EditorConfigPackageControl]: https://sublime.wbond.net/packages/EditorConfig
[EditorConfigGit]: https://github.com/sindresorhus/editorconfig-sublime
[LineEndingsPackageControl]: https://sublime.wbond.net/packages/Line%20Endings%20Unify
[LineEndingsGit]: https://github.com/vontio/sublime-line-endings-unify