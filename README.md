# Sublime Text 2 - Setup

A few thoughts how to set up Sublime Text editor.

## Projects

Basic settings for a new project. 

`d:/develop/project/`

- [.sublime-project][.sublime-project]

## Snippets

Snippets are smart templates that will insert text for you and adapt it to their context.

`c:/Users/Martin/AppData/Roaming/Sublime Text 2/Packages/User/`

- [ConsoleLog.sublime-snippet][ConsoleLog.sublime-snippet]

## Package Control

The Sublime Text package control manager that makes it exceedingly simple to find, install and keep packages up-to-date.

- [Package Control][PackageControl]
- [Package Control - Install][PackageControlInstall]

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

Install Node.js:

- `d:/nodejs/`

Install JSHint via NPM:

- `$ npm install jshint -g`

Install JSHint Gutter:

- `Ctrl+Shift+P`
- `Package Control: Install Package`
- `JSHint Gutter`
- `c:/Users/Martin/AppData/Roaming/Sublime Text 2/Packages/JSHint Gutter/JSHint.sublime-settings`

```javascript
{
  // Path to your Node.js
  "node_path": "/d/nodejs/node.exe",

  // Automatically lint on edit (Sublime Text 3 only).
  "lint_on_edit": false,

  // Automatically lint when a file is saved.
  "lint_on_save": true
}
```
How to use:

- `Right Click > JSHint > ...`
- `Ctrl+Alt+J` Lint Code
- `Ctrl+Alt+C` Clear

Your own .jshintrc options:

The plugin looks for a [.jshintrc][.jshintrc] file in the same directory as the source file you're linting and, or one located recursively up one directory, all the way until the filesystem root. As well, it uses those options along the default ones.

See the documentation at jshint.com and a few [examples here][.jshintrc-examples].


[.sublime-project]: https://raw.github.com/martinjezek/SublimeTextSetup/master/project/.sublime-project
[ConsoleLog.sublime-snippet]: https://raw.github.com/martinjezek/SublimeTextSetup/master/snippets/ConsoleLog.sublime-snippet
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