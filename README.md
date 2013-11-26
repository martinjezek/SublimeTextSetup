# Sublime Text 2 - Setup

A few thoughts how to set up Sublime Text editor.

## Projects

Basic settings for a new project. 

`d:/develop/project/`

- [project.sublime-project][project.sublime-project]

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

- [Soda Theme - Package Control][SodaThemeGitPackageControl]
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

[project.sublime-project]: https://raw.github.com/martinjezek/SublimeTextSetup/master/projects/project.sublime-project
[ConsoleLog.sublime-snippet]: https://raw.github.com/martinjezek/SublimeTextSetup/master/snippets/ConsoleLog.sublime-snippet
[PackageControl]: https://sublime.wbond.net/
[PackageControlInstall]: https://sublime.wbond.net/installation
[SyncedSideBarPackageControl]: https://sublime.wbond.net/packages/SyncedSideBar
[SyncedSideBarGit]: https://github.com/sobstel/SyncedSideBar
[SodaThemeGitPackageControl]: https://sublime.wbond.net/packages/Theme%20-%20Soda
[SodaThemeGit]: https://github.com/buymeasoda/soda-theme/
[SodaThemeSyntaxHighlightingGit]: http://buymeasoda.github.com/soda-theme/extras/colour-schemes.zip