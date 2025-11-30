# Dance

## Dance itself
[Extension on github](https://github.com/71/dance)
This one is really cool, I like it a lot

```json
  "dance.modes": {
    "": {
      "hiddenSelectionsIndicatorsDecoration": {
        "after": {
          "color": "$list.warningForeground"
        },
        "backgroundColor": "$inputValidation.warningBackground",
        "borderColor": "$inputValidation.warningBorder",
        "borderStyle": "solid",
        "borderWidth": "1px",
        "isWholeLine": true
      }
    },
    "input": {
      "cursorStyle": "underline-thin"
    },
    "insert": {
      "onLeaveMode": [
        [
          ".selections.save",
          {
            "register": " insert"
          }
        ]
      ]
    },
    "select": {},
    "normal": {
      "lineNumbers": "inherit",
      "decorations": {
        "applyTo": "main",
        "backgroundColor": 
        // "$editor.hoverHighlightBackground",
        // "$list.activeSelectionBackground",
        "$editor.activeSelectionBackground",
        "isWholeLine": false
      },
      "onEnterMode": [
        [
          ".selections.restore",
          {
            "register": " ^",
            "try": true
          }
        ]
      ],
      "onLeaveMode": [
        [
          ".selections.save",
          {
            "register": " ^",
            "style": {
              "borderColor": "$editor.selectionBackground",
              "borderStyle": "solid",
              "borderWidth": "2px",
              "borderRadius": "1px"
            },
            "until": [
              [
                "mode-did-change",
                {
                  "include": "normal"
                }
              ],
              [
                "selections-did-change"
              ]
            ]
          }
        ]
      ]
    }
  },
  "dance.menus": {
    "object": {
      "title": "Select object...",
      "items": {
        "b()": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "\\((?#inner)\\)"
            }
          ],
          "text": "parenthesis block"
        },
        "B{}": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "\\{(?#inner)\\}"
            }
          ],
          "text": "braces block"
        },
        "r[]": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "\\[(?#inner)\\]"
            }
          ],
          "text": "brackets block"
        },
        "a<>": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "<(?#inner)>"
            }
          ],
          "text": "angle block"
        },
        "Q\"": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "(?#noescape)\"(?#inner)(?#noescape)\""
            }
          ],
          "text": "double quote string"
        },
        "q'": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "(?#noescape)'(?#inner)(?#noescape)'"
            }
          ],
          "text": "single quote string"
        },
        "g`": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "(?#noescape)`(?#inner)(?#noescape)`"
            }
          ],
          "text": "grave quote string"
        },
        "w": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "[\\p{L}_\\d]+(?<after>[^\\S\\n]+)"
            }
          ],
          "text": "word"
        },
        "W": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "[\\S]+(?<after>[^\\S\\n]+)"
            }
          ],
          "text": "WORD"
        },
        "s": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "(?#predefined=sentence)"
            }
          ],
          "text": "sentence"
        },
        "p": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "(?#predefined=paragraph)"
            }
          ],
          "text": "paragraph"
        },
        " ": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "(?<before>[\\s]+)[^\\S\\n]+(?<after>[\\s]+)"
            }
          ],
          "text": "whitespaces"
        },
        "i": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "(?#predefined=indent)"
            }
          ],
          "text": "indent"
        },
        "n": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "(?#singleline)-?[\\d_]+(\\.[0-9]+)?([eE]\\d+)?"
            }
          ],
          "text": "number"
        },
        "u": {
          "command": "dance.seek.object",
          "args": [
            {
              "input": "(?#predefined=argument)"
            }
          ],
          "text": "argument"
        },
        "c": {
          "command": "dance.seek.object",
          "text": "custom object desc"
        }
      }
    },
    "goto": {
      "title": "Go...",
      "items": {
        "h": {
          "text": "to line start",
          "command": "dance.select.lineStart"
        },
        "l": {
          "text": "to line end",
          "command": "dance.select.lineEnd"
        },
        "i": {
          "text": "to implementation",
          "command": "editor.action.goToImplementation",
        },
        "gk": {
          "text": "to first line",
          "command": "dance.select.lineStart",
          "args": [
            {
              "count": 1
            }
          ]
        },
        "j": {
          "text": "to last line",
          "command": "dance.select.lastLine"
        },
        "e": {
          "text": "to last char of last line",
          "command": "dance.select.lineEnd",
          "args": [
            {
              "count": 2147483647
            }
          ]
        },
        "t": {
          "text": "to first displayed line",
          "command": "dance.select.firstVisibleLine"
        },
        "c": {
          "text": "to middle displayed line",
          "command": "dance.select.middleVisibleLine"
        },
        "b": {
          "text": "to last displayed line",
          "command": "dance.select.lastVisibleLine"
        },
        "a": {
          "text": "to last buffer",
          "command": "workbench.action.openPreviousRecentlyUsedEditorInGroup"
        },
        "A": {
          "text": "to last buffer...",
          "command": "workbench.action.quickOpenPreviousRecentlyUsedEditorInGroup"
        },
        "p": {
          "text": "to previous buffer",
          "command": "workbench.action.previousEditor"
        },
        "n": {
          "text": "to next buffer",
          "command": "workbench.action.nextEditor"
        },
        "f": {
          "text": "to file whose name is selected",
          "command": "dance.selections.open"
        },
        "d": {
          "text": "to definition",
          "command": "editor.action.revealDefinition"
        },
        "r": {
          "text": "to references",
          "command": "editor.action.goToReferences"
        },
        ".": {
          "text": "to last buffer modification position",
          "command": "dance.selections.restore",
          "args": [
            {
              "register": " insert"
            }
          ]
        }
      }
    },
    "view": {
      "title": "View",
      "items": {
        "vc": {
          "text": "center cursor vertically",
          "command": "dance.view.line",
          "args": [
            {
              "at": "center"
            }
          ]
        },
        "t": {
          "text": "cursor on top",
          "command": "dance.view.line",
          "args": [
            {
              "at": "top"
            }
          ]
        },
        "b": {
          "text": "cursor on bottom",
          "command": "dance.view.line",
          "args": [
            {
              "at": "bottom"
            }
          ]
        },
        "j": {
          "text": "scroll down",
          "command": "editorScroll",
          "args": [
            {
              "to": "down",
              "by": "line",
              "revealCursor": true
            }
          ]
        },
        "k": {
          "text": "scroll up",
          "command": "editorScroll",
          "args": [
            {
              "to": "up",
              "by": "line",
              "revealCursor": true
            }
          ]
        }
      }
    },
    "vscIntegration": {
      "title": "Select action",
      "items": {
        "d": {
          "text": "debug",
          "command": "workbench.debug.action.focusVariablesView"
        },
        "c": {
          "text": "command palette",
          "command": "workbench.action.showCommands"
        },
        "f": {
          "text": "go to file",
          "command": "workbench.action.quickOpen"
        },
        "e": {
          "text": "explorer",
          "command": "workbench.explorer.fileView.focus"
        },
        "g": {
          "text": "git",
          "command": "workbench.view.scm"
        },
        "x": {
          "text": "extensions",
          "command": "workbench.view.extensions"
        },
        "s": {
          "text": "sql",
          "command": "sqlite.explorer.focus"
        },
        "b": {
          "text": "build and debug",
          "command": "workbench.action.debug.start"
        },
        "t": {
          "text": "tests",
          "command": "workbench.view.testing.focus"
        },
      }
    }
  }
```