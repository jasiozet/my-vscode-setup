# How I Use Visual Studio Code?

Disclaimer: I'm not saying this is the best way. I'm even sure there are better ways, if you have improvements *let me know*!

This guide is mainly for me and people that ask me about my setup when pair programming

In all shortcut example **Alt = Option** on Mac

In most examples **Ctrl = Command** on Mac

## Workflow

I use terminal and ```cd``` command to navigate to repository and ```code .``` to launch everything in VSCode.

## VSCode GUI

I prefer Vertical Tabs over horizontal ones (I use Open Editors for that focus on it with ```Ctrl + K, E```), I like having the bar on the left side so the code starts a little bit more in the center of the screen. I have the main bar on the right, usually in File explorer and I hide it (```Ctrl + B```) when I need more space. I have a terminal open (```Ctrl + ` ```) almost all the time and I use it mainly for launching project from the command line and git CLI.

![Screenshot](img/screenshot.png)

## Philosophy

I try to use keyboard as much as possible. Mouse is for the problems I don't know/remember how to solve quickly with keyboard.

Two shorcuts that I recommend are:
* ```Ctrl Shift P``` - Command Pallette, you can do most stuff with it
* ```Ctrl P``` - Search files by name

## Best shortcuts
* ```Alt ⬆️``` / ```Alt ⬇️``` - move the line/selection up/down
* ```Ctrl K  Ctrl C ``` - comment line/selection
* ```Ctrl K  Ctrl U ``` - uncomment line/selection
* ```Alt Shift ⬇️``` - copy line below
* ```Shift Del ``` - delete line
* ```Ctrl L``` - highlight line (can be chained)

## Other useful shortcuts

* ```Ctrl .``` - definition window (still trying to find something better)

## Best extensions

* [Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens) - Never hover over an error/warning again
* [Peacock](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock) - If you are working with a couple of instances of VSCode at the same time this is a life saver, color code them for easier context switching
* [MetaGo](https://marketplace.visualstudio.com/items?itemName=metaseed.metago) - this one is for really mouseless navigation. 

### Metago shortcuts: 
* ```Alt /``` for jumping to any character in the current file. 
* add ```Shift``` if you want to select additionaly 
* ```Alt P``` to select surounding brackets 
* add ```Shift``` for content and
* add ```Ctrl``` for both 
* ```Alt '``` toggle bookmark. 
* ```Alt \``` show all bookmarks
* ```Alt [``` and ```Alt ]``` navigate bookmarks 

## Eyecandy extensions 
I don't rely on them very much but they make life a bit nicer
* [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons)
* [Quiet Light for VSC](https://marketplace.visualstudio.com/items?itemName=onecrayon.theme-quietlight-vsc)
* [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)
* [Todo Tree](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree)

## Fonts

* [Fira Code](https://github.com/tonsky/FiraCode) for text editor

## Settings declutter

```"workbench.startupEditor": "none",
  "editor.minimap.enabled": false,
  "breadcrumbs.enabled": false,
  "workbench.sideBar.location": "right",
  "explorer.openEditors.sortOrder": "alphabetical",
  "explorer.openEditors.minVisible": 1,
  "explorer.openEditors.visible": 1,
  "workbench.editor.showIcons": false, 
  "workbench.editor.tabCloseButton": "off",
  "workbench.editor.showTabs": false,
  "editor.renderLineHighlight": "none",
  "editor.renderWhitespace": "none",
  "editor.inlineSuggest.enabled": true,
  "workbench.activityBar.visible": false,
  "workbench.editor.enablePreview": false, 
```

## What I also personally use:

* [Ionide](https://ionide.io/) for F# my favorite language

## Why not Neovim / Vim / Emacs ?

Simply because VS Code gets extensions / language support the fastest and I'm not good enough at Vim and I find hjkl to be too tricky (why it isn't modernized to ijkl or something?)
