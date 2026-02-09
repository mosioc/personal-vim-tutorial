# VSCode Neovim – Complete Keybindings Cheat Sheet

> **Scope**: Neovim keybindings inside **VSCode** using the `vscode-neovim` extension.
> Includes **editor navigation, code navigation, explorer/list navigation, file manipulation, hover widgets, and VSCode integrations**.

---

## Table of Contents

* [Modes](#modes)
* [Basic Cursor Navigation](#basic-cursor-navigation)
* [Word & Text Navigation](#word--text-navigation)
* [Editing & Operators](#editing--operators)
* [Visual Mode](#visual-mode)
* [Search & Replace](#search--replace)
* [Registers & Clipboard](#registers--clipboard)
* [Window & Tab Management](#window--tab-management)
* [Code Navigation Bindings](#code-navigation-bindings)
* [Explorer / List Navigation Bindings](#explorer--list-navigation-bindings)
* [Explorer File Manipulation Bindings](#explorer-file-manipulation-bindings)
* [Hover Widget Manipulation Bindings](#hover-widget-manipulation-bindings)
* [Quick VSCode Integrations](#quick-vscode-integrations)

---

## Modes

| Mode         | Keys          | Description          |
| ------------ | ------------- | -------------------- |
| Normal       | `Esc`         | Default command mode |
| Insert       | `i a o I A O` | Insert text          |
| Visual       | `v`           | Character selection  |
| Visual Line  | `V`           | Line selection       |
| Visual Block | `Ctrl-v`      | Column selection     |
| Command      | `:`           | Vim command-line     |

---

## Basic Cursor Navigation

| Key                 | Action                             |
| ------------------- | ---------------------------------- |
| `h j k l`           | Left / Down / Up / Right           |
| `0` / `^` / `$`     | Line start / first non-blank / end |
| `gg` / `G`          | First / last line                  |
| `H M L`             | Top (High) / middle / bottom (Low) of screen    |
| `Ctrl-d` / `Ctrl-u` | Half-page down / up                |
| `Ctrl-f` / `Ctrl-b` | Full page down / up                |
| `%`                 | Jump to matching bracket           |
| `Ctrl-o` / `Ctrl-i` | Jump backward / forward            |

---

## Word & Text Navigation

| Key                   | Action                            |
| --------------------- | --------------------------------- |
| `w` / `W`             | Next word / WORD                  |
| `b` / `B`             | Previous word / WORD              |
| `e` / `E`             | End of word / WORD                |
| `ge` / `gE`           | End of previous word              |
| `f<char>` / `F<char>` | Find character forward / backward |
| `t<char>` / `T<char>` | Till character forward / backward |
| `;` / `,`             | Repeat last f/t                   |

---

## Editing & Operators

| Key                | Action                              |
| ------------------ | ----------------------------------- |
| `x` / `X`          | Delete character                    |
| `dd` / `D`         | Delete line / to end of line        |
| `cc` / `C`         | Change line / to end                |
| `dw` / `de` / `d$` | Delete word / to end of word / line |
| `yw` / `yy`        | Yank word / line                    |
| `p` / `P`          | Paste after / before                |
| `u` / `Ctrl-r`     | Undo / Redo                         |
| `.`                | Repeat last change                  |

---

## Visual Mode

| Key          | Action                           |
| ------------ | -------------------------------- |
| `v V Ctrl-v` | Visual modes                     |
| `y d c`      | Yank / delete / change selection |
| `>` / `<`    | Indent / dedent                  |
| `=`          | Auto-indent                      |
| `o`          | Swap selection end               |
| `~ u U`      | Toggle / lower / upper case      |

---

## Search & Replace

| Key          | Action                   |
| ------------ | ------------------------ |
| `/pattern`   | Search forward           |
| `?pattern`   | Search backward          |
| `n` / `N`    | Next / previous match    |
| `*` / `#`    | Search word under cursor |
| `:s/a/b`     | Replace first occurrence |
| `:%s/a/b/gc` | Replace all with confirm |
| `:noh`       | Clear highlights         |

---

## Registers & Clipboard

| Key           | Action                        |
| ------------- | ----------------------------- |
| `"ayy`        | Yank line to register `a`     |
| `"ap`         | Paste from register `a`       |
| `"+y` / `"+p` | System clipboard yank / paste |
| `"_d`         | Delete without yanking        |
| `:reg`        | Show registers                |

---

## Window & Tab Management

| Key                     | Action                      |
| ----------------------- | --------------------------- |
| `Ctrl-w s` / `Ctrl-w v` | Horizontal / vertical split |
| `Ctrl-w h j k l`        | Move between windows        |
| `Ctrl-w =`              | Equalize sizes              |
| `Ctrl-w q`              | Close window                |
| `gt` / `gT`             | Next / previous tab         |
| `Ctrl-1..9`             | Focus editor group (VSCode) |
| `Ctrl-\\`               | Split editor (VSCode)       |

---

## Code Navigation Bindings

| Key         | VSCode Action         |
| ----------- | --------------------- |
| `gd`        | Go to definition      |
| `gD`        | Peek definition       |
| `gi`        | Go to implementation  |
| `gr`        | Go to references      |
| `gf`        | Go to file            |
| `gO`        | Go to symbol in file  |
| `K` / `gh`  | Show hover            |
| `Ctrl-w gd` | Open definition aside |

---

## Explorer / List Navigation Bindings

> Works in **Explorer, Quick Open, Command Palette, Reference Peek**

| Key                 | Action            |
| ------------------- | ----------------- |
| `j` / `k`           | Move down / up    |
| `h` / `l`           | Collapse / expand |
| `gg` / `G`          | First / last item |
| `o` / `Enter`       | Open item         |
| `Ctrl-d` / `Ctrl-u` | Page down / up    |
| `zo` / `zc`         | Expand / collapse |
| `/`                 | Filter list       |
| `Esc`               | Exit list focus   |

---

## Explorer File Manipulation Bindings

| Key | Action           |
| --- | ---------------- |
| `a` | New file         |
| `A` | New folder       |
| `r` | Rename           |
| `d` | Delete           |
| `y` | Copy             |
| `x` | Cut              |
| `p` | Paste            |
| `v` | Open to side     |
| `R` | Refresh explorer |

---

## Hover Widget Manipulation Bindings

| Key                 | Action                        |
| ------------------- | ----------------------------- |
| `K`                 | Show hover                    |
| `Esc`               | Close hover                   |
| `j` / `k`           | Scroll hover                  |
| `h` / `l`           | Horizontal scroll             |
| `Ctrl-f` / `Ctrl-b` | Page down / up                |
| `Tab` / `Shift-Tab` | Focus next / previous element |

---

## Quick VSCode Integrations

| Key            | Action                 |
| -------------- | ---------------------- |
| `Ctrl-p`       | Quick open file        |
| `Ctrl-Shift-p` | Command palette        |
| `Ctrl-.`       | Code actions           |
| `Ctrl-/`       | Toggle comment         |
| `Alt-Up/Down`  | Move line up/down      |
| `Ctrl-Shift-L` | Select all occurrences |

---

> **Tip**: Most VSCode commands can be mapped inside Neovim using `vscode.call()` or `vscode.action()` for a fully Vim-centric workflow.
