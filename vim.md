# Decided to try some Vim in VsCode

I can't really go full neovim due to bad C# support. VsCode Vim is certainly possible

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