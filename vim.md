# Deprecated: Decided to try some Vim in VsCode

I tried to go neovim but C# support is a bit complicated and I feel like with some updates I might loose stability of my env. VsCode Vim is certainly possible

[VsCode vim extension](https://github.com/VSCodeVim/Vim)

[Some good shortcuts source](https://gist.github.com/nikolovlazar/1174876ab2769c52ac9fc1534c557d70)

## Vim Settings
```
  "vim.useSystemClipboard": true,
```

## Shortcuts I found really helpful
```
  {
    "key": "tab",
    "command": "workbench.action.nextEditorInGroup",
    "when": "(vim.mode == 'Normal' || vim.mode == 'Visual') && (editorTextFocus || !inputFocus)"
  },
  {
    "key": "shift-tab",
    "command": "workbench.action.previousEditorInGroup",
    "when": "(vim.mode == 'Normal' || vim.mode == 'Visual') && (editorTextFocus || !inputFocus)"
  },
  {
    "key": "space g d",
    "command": "editor.action.revealDefinition",
    "when": "vim.mode == 'Normal' && editorTextFocus"
  },
  {
    "key": "space g r",
    "command": "editor.action.goToReferences",
    "when": "vim.mode == 'Normal' && editorTextFocus"
  },
  {
    "key": "space g i",
    "command": "editor.action.goToImplementation",
    "when": "vim.mode == 'Normal' && editorTextFocus"
  },
```

## Shortcuts to keep previous functionality I relied on

```
  {
    "key": "shift+meta+g",
    "command": "-editor.action.previousMatchFindAction",
  },
  {
    "key": "shift+cmd+g",
    "command": "-workbench.action.terminal.findPrevious",
    "when": "terminalFindFocused && terminalHasBeenCreated || terminalFindFocused && terminalProcessSupported || terminalFocusInAny && terminalHasBeenCreated || terminalFocusInAny && terminalProcessSupported"
  },
  {
    "key": "shift+cmd+g",
    "command": "-workbench.action.terminal.openDetectedLink",
    "when": "accessibleViewIsShown && terminalHasBeenCreated && accessibleViewCurrentProviderId == 'terminal'"
  },
  {
    "key": "shift+cmd+g",
    "command": "workbench.view.scm",
    "when": "workbench.scm.active"
  },
  {
    "key": "ctrl+shift+g",
    "command": "-workbench.view.scm",
    "when": "workbench.scm.active"
  },
```