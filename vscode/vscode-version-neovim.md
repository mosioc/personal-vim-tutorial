# VSCode Neovim – Complete Keybindings Cheat Sheet

> **Comprehensive guide** for Neovim keybindings inside **VSCode** using the `vscode-neovim` extension.
> Includes editor navigation, code navigation, marks, folds, macros, text objects, explorer integration, and VSCode-specific commands.

## Table of Contents

- [Modes](#modes)
- [Basic Cursor Navigation](#basic-cursor-navigation)
- [Word & Text Navigation (Motions)](#word--text-navigation-motions)
- [Line Navigation & Jumps](#line-navigation--jumps)
- [Editing & Operators](#editing--operators)
- [Text Objects](#text-objects)
- [Visual Mode](#visual-mode)
- [Search & Replace](#search--replace)
- [Marks & Jumps](#marks--jumps)
- [Macros](#macros)
- [Registers & Clipboard](#registers--clipboard)
- [Folds](#folds)
- [Indentation](#indentation)
- [Window & Tab Management](#window--tab-management)
- [Code Navigation](#code-navigation)
- [Code Actions & Refactoring](#code-actions--refactoring)
- [Explorer Navigation](#explorer-navigation)
- [Explorer File Operations](#explorer-file-operations)
- [Hover & Documentation](#hover--documentation)
- [VSCode Integrations](#vscode-integrations)
- [Advanced Tips](#advanced-tips)

## Modes

| Mode         | Keys          | Description                    |
| ------------ | ------------- | ------------------------------ |
| Normal       | `Esc`         | Default command mode           |
| Insert       | `i a o I A O` | Insert text at various points  |
| Visual       | `v`           | Character-wise selection       |
| Visual Line  | `V`           | Line-wise selection            |
| Visual Block | `Ctrl-v`      | Block/column selection         |
| Command      | `:`           | Vim command-line mode          |
| Replace      | `R`           | Overwrite text                 |

**Quick mode switches:**

- `i` - insert before cursor
- `a` - insert after cursor
- `I` - insert at line start
- `A` - insert at line end
- `o` - new line below
- `O` - new line above
- `s` - substitute character
- `S` - substitute line

## Basic Cursor Navigation

| Key                 | Action                                  |
| ------------------- | --------------------------------------- |
| `h j k l`           | Left / Down / Up / Right                |
| `0`                 | Start of line (column 0)                |
| `^`                 | First non-blank character               |
| `$`                 | End of line                             |
| `g_`                | Last non-blank character                |
| `gg`                | First line of file                      |
| `G`                 | Last line of file                       |
| `nG` / `:n`         | Go to line n                            |
| `H`                 | Top of screen (High)                    |
| `M`                 | Middle of screen                        |
| `L`                 | Bottom of screen (Low)                  |
| `Ctrl-d`            | Half-page down                          |
| `Ctrl-u`            | Half-page up                            |
| `Ctrl-f`            | Full page forward                       |
| `Ctrl-b`            | Full page backward                      |
| `Ctrl-e`            | Scroll down (cursor stays)              |
| `Ctrl-y`            | Scroll up (cursor stays)                |
| `zz`                | Center cursor on screen                 |
| `zt`                | Cursor to top of screen                 |
| `zb`                | Cursor to bottom of screen              |

## Word & Text Navigation (Motions)

| Key                   | Action                                |
| --------------------- | ------------------------------------- |
| `w`                   | Next word start                       |
| `W`                   | Next WORD start (whitespace-delimited)|
| `b`                   | Previous word start                   |
| `B`                   | Previous WORD start                   |
| `e`                   | Next word end                         |
| `E`                   | Next WORD end                         |
| `ge`                  | Previous word end                     |
| `gE`                  | Previous WORD end                     |
| `f<char>`             | Find character forward on line        |
| `F<char>`             | Find character backward on line       |
| `t<char>`             | Till (before) character forward       |
| `T<char>`             | Till (after) character backward       |
| `;`                   | Repeat last f/F/t/T forward           |
| `,`                   | Repeat last f/F/t/T backward          |
| `%`                   | Jump to matching bracket/paren        |
| `[{` / `]}`           | Jump to previous/next `{`             |
| `[(` / `])`           | Jump to previous/next `(`             |
| `g%`                  | Backward match for `%`                |

## Line Navigation & Jumps

| Key                 | Action                              |
| ------------------- | ----------------------------------- |
| `+` / `Enter`       | First non-blank of next line        |
| `-`                 | First non-blank of previous line    |
| `_`                 | First non-blank of current line     |
| `nG`                | Go to line n                        |
| `gg=G`              | Auto-indent entire file             |
| `Ctrl-o`            | Jump to previous location           |
| `Ctrl-i` / `Tab`    | Jump to next location               |
| `g;`                | Go to previous edit location        |
| `g,`                | Go to next edit location            |
| `'.`                | Jump to last edit line              |
| `` `. ``            | Jump to exact last edit position    |

## Editing & Operators

| Key                | Action                                    |
| ------------------ | ----------------------------------------- |
| `x`                | Delete character under cursor             |
| `X`                | Delete character before cursor            |
| `dd`               | Delete (cut) line                         |
| `D`                | Delete to end of line                     |
| `d0`               | Delete to start of line                   |
| `dw`               | Delete word                               |
| `de`               | Delete to end of word                     |
| `db`               | Delete to start of word                   |
| `d$`               | Delete to end of line                     |
| `d^`               | Delete to first non-blank                 |
| `dG`               | Delete to end of file                     |
| `dgg`              | Delete to start of file                   |
| `cc`               | Change (replace) entire line              |
| `C`                | Change to end of line                     |
| `cw`               | Change word                               |
| `ciw`              | Change inner word                         |
| `ci"` / `ci'`      | Change inside quotes                      |
| `ci{` / `ci(`      | Change inside braces/parens               |
| `s`                | Substitute character                      |
| `S`                | Substitute line                           |
| `r<char>`          | Replace single character                  |
| `R`                | Enter replace mode                        |
| `~`                | Toggle case of character                  |
| `g~w`              | Toggle case of word                       |
| `guw`              | Lowercase word                            |
| `gUw`              | Uppercase word                            |
| `gu$`              | Lowercase to end of line                  |
| `gU$`              | Uppercase to end of line                  |
| `J`                | Join line below with current              |
| `gJ`               | Join without space                        |
| `u`                | Undo                                      |
| `Ctrl-r`           | Redo                                      |
| `U`                | Undo all changes on line                  |
| `.`                | Repeat last change                        |
| `@:`               | Repeat last command                       |
| `p`                | Paste after cursor/line                   |
| `P`                | Paste before cursor/line                  |
| `gp`               | Paste and move cursor after              |
| `gP`               | Paste before and move cursor after       |

## Text Objects

**Syntax:** `<operator><a/i><object>`

- `a` = "a" (around - includes delimiters)
- `i` = "inner" (inside - excludes delimiters)

| Text Object | Description              | Example Usage    |
| ----------- | ------------------------ | ---------------- |
| `w`         | word                     | `ciw` `daw`      |
| `W`         | WORD                     | `ciW` `daW`      |
| `s`         | sentence                 | `das` `cis`      |
| `p`         | paragraph                | `dap` `yip`      |
| `"` `'` `` ` `` | quoted text          | `ci"` `da'` `di`` ` `` |
| `(` `)` `b` | parentheses              | `ci(` `da)` `dib`|
| `{` `}` `B` | braces                   | `ci{` `da}` `diB`|
| `[` `]`     | brackets                 | `ci[` `da]`      |
| `<` `>`     | angle brackets           | `ci<` `da>`      |
| `t`         | tag (HTML/XML)           | `cit` `dat`      |

**Common combinations:**

- `diw` - delete inner word
- `daw` - delete a word (with space)
- `ci"` - change inside quotes
- `da{` - delete around braces
- `di<` - delete inside less-than
- `yit` - yank inside tag
- `vip` - visual select paragraph
- etc.

## Visual Mode

| Key          | Action                           |
| ------------ | -------------------------------- |
| `v`          | Character-wise visual            |
| `V`          | Line-wise visual                 |
| `Ctrl-v`     | Block visual                     |
| `gv`         | Reselect last visual selection   |
| `o`          | Move to other end of selection   |
| `O`          | Move to other corner (block)     |
| `aw` / `iw`  | Select a word / inner word       |
| `ab` / `ib`  | Select a block / inner block     |
| `aB` / `iB`  | Select a {} block                |
| `at` / `it`  | Select a tag / inner tag         |
| `y`          | Yank selection                   |
| `d`          | Delete selection                 |
| `c`          | Change selection                 |
| `~`          | Toggle case                      |
| `u`          | Lowercase                        |
| `U`          | Uppercase                        |
| `>`          | Indent right                     |
| `<`          | Indent left                      |
| `=`          | Auto-indent                      |
| `J`          | Join selected lines              |
| `gJ`         | Join without space               |
| `:normal i//`| Insert `//` at start (block)     |

## Search & Replace

| Key              | Action                              |
| ---------------- | ----------------------------------- |
| `/pattern`       | Search forward                      |
| `?pattern`       | Search backward                     |
| `n`              | Next match (same direction)         |
| `N`              | Previous match (opposite direction) |
| `*`              | Search word under cursor (forward)  |
| `#`              | Search word under cursor (backward) |
| `g*`             | Search partial word forward         |
| `g#`             | Search partial word backward        |
| `:noh`           | Clear search highlights             |
| `:%s/old/new/g`  | Replace all in file                 |
| `:%s/old/new/gc` | Replace all with confirmation       |
| `:s/old/new/g`   | Replace all in current line         |
| `:'<,'>s/old/new/g` | Replace in visual selection      |
| `:%s/\<old\>/new/g` | Replace whole words only         |
| `&`              | Repeat last substitute              |
| `g&`             | Repeat last substitute on all lines |

**Search options:**

- `/pattern\c` - case insensitive
- `/pattern\C` - case sensitive
- `/pattern/e` - cursor at end of match

## Marks & Jumps

**Marks** are bookmarks in your file(s).

| Key           | Action                            |
| ------------- | --------------------------------- |
| `m{a-z}`      | Set local mark (lowercase)        |
| `m{A-Z}`      | Set global mark (uppercase)       |
| `` `{mark} `` | Jump to mark (exact position)     |
| `'{mark}`     | Jump to mark (first non-blank)    |
| `` `. ``      | Jump to last edit position        |
| `'.`          | Jump to last edit line            |
| `` `` ``      | Jump to position before last jump |
| `''`          | Jump to line before last jump     |
| `` `[ ``      | Jump to start of last change      |
| `` `] ``      | Jump to end of last change        |
| `` `< ``      | Jump to start of last visual      |
| `` `> ``      | Jump to end of last visual        |
| `:marks`      | List all marks                    |
| `:delmarks a` | Delete mark a                     |
| `:delmarks!`  | Delete all local marks            |

**Special marks:**

- `` `. `` - last edit
- `` `^ `` - last insert position
- `` `[ `` `] `` - last change boundaries
- `` `< `` `> `` - last visual selection

**Jump list:**

- `Ctrl-o` - go back in jump list
- `Ctrl-i` - go forward in jump list
- `:jumps` - show jump list

## Macros

**Record and replay sequences of commands.**

| Key              | Action                           |
| ---------------- | -------------------------------- |
| `q{a-z}`         | Start recording to register      |
| `q`              | Stop recording                   |
| `@{a-z}`         | Execute macro from register      |
| `@@`             | Repeat last macro                |
| `10@a`           | Execute macro 10 times           |
| `:normal @a`     | Execute macro on all lines       |
| `:'<,'>normal @a`| Execute on visual selection      |
| `qA`             | Append to existing macro a       |
| `:let @a='...'`  | Edit macro directly              |
| `:reg a`         | View macro contents              |

**Example workflow:**

1. `qa` - start recording to register 'a'
2. (perform edits)
3. `q` - stop recording
4. `@a` - replay macro
5. `100@a` - replay 100 times

## Registers & Clipboard

**Registers** store yanked/deleted text.

| Key               | Action                            |
| ----------------- | --------------------------------- |
| `"ayy`            | Yank line to register a           |
| `"ap`             | Paste from register a             |
| `"Ayy`            | Append yank to register a         |
| `"+y`             | Yank to system clipboard          |
| `"+p`             | Paste from system clipboard       |
| `"*y`             | Yank to selection clipboard       |
| `"_d`             | Delete to black hole (no yank)    |
| `"0p`             | Paste last yank (not delete)      |
| `"1p`             | Paste last delete                 |
| `:reg`            | Show all registers                |
| `:reg abc`        | Show specific registers           |
| `Ctrl-r {reg}`    | Paste register in insert mode     |
| `Ctrl-r +`        | Paste clipboard in insert mode    |

**Special registers:**

- `"` - unnamed (last yank/delete)
- `0` - last yank
- `1-9` - last deletes (1=most recent)
- `+` - system clipboard
- `*` - selection clipboard
- `_` - black hole
- `%` - current filename
- `/` - last search pattern

## Folds

**Code folding** for better navigation.

| Key          | Action                          |
| ------------ | ------------------------------- |
| `zc`         | Close fold under cursor         |
| `zo`         | Open fold under cursor          |
| `za`         | Toggle fold under cursor        |
| `zC`         | Close all folds under cursor    |
| `zO`         | Open all folds under cursor     |
| `zA`         | Toggle all folds under cursor   |
| `zM`         | Close all folds in file         |
| `zR`         | Open all folds in file          |
| `zm`         | Fold more (increase foldlevel)  |
| `zr`         | Fold less (decrease foldlevel)  |
| `zj`         | Move to next fold               |
| `zk`         | Move to previous fold           |
| `[z`         | Move to start of current fold   |
| `]z`         | Move to end of current fold     |
| `zf`         | Create fold (in visual mode)    |
| `zd`         | Delete fold under cursor        |
| `zE`         | Delete all folds                |
| `zv`         | Open folds to reveal cursor     |

**VSCode-specific:**

- `zc` / `zo` work with VSCode's native folding
- Uses VSCode's fold detection (indent, syntax, etc.)

## Indentation

| Key               | Action                          |
| ----------------- | ------------------------------- |
| `>>`              | Indent line                     |
| `<<`              | Dedent line                     |
| `>`               | Indent in visual mode           |
| `<`               | Dedent in visual mode           |
| `=`               | Auto-indent (motion/visual)     |
| `==`              | Auto-indent current line        |
| `gg=G`            | Auto-indent entire file         |
| `=i{`             | Auto-indent inside braces       |
| `=a{`             | Auto-indent around braces       |
| `5>>`             | Indent 5 lines                  |
| `>%`              | Indent to matching bracket      |
| `.`               | Repeat indent                   |
| `Ctrl-t`          | Indent in insert mode           |
| `Ctrl-d`          | Dedent in insert mode           |

## Window & Tab Management

| Key                     | Action                             |
| ----------------------- | ---------------------------------- |
| `Ctrl-w s`              | Horizontal split                   |
| `Ctrl-w v`              | Vertical split                     |
| `Ctrl-w n`              | New horizontal split               |
| `Ctrl-w q`              | Close window                       |
| `Ctrl-w o`              | Close other windows                |
| `Ctrl-w h/j/k/l`        | Navigate to left/down/up/right     |
| `Ctrl-w H/J/K/L`        | Move window to left/down/up/right  |
| `Ctrl-w =`              | Equalize window sizes              |
| `Ctrl-w _`              | Maximize height                    |
| `Ctrl-w \|` (Ctrl-w pipeline)              | Maximize width                     |
| `Ctrl-w +`              | Increase height                    |
| `Ctrl-w -`              | Decrease height                    |
| `Ctrl-w >`              | Increase width                     |
| `Ctrl-w <`              | Decrease width                     |
| `Ctrl-w r`              | Rotate windows                     |
| `Ctrl-w x`              | Exchange windows                   |
| `Ctrl-w T`              | Move to new tab                    |

**Tabs:**

| Key            | Action              |
| -------------- | ------------------- |
| `:tabnew`      | New tab             |
| `gt` / `Ctrl-PgDn` | Next tab        |
| `gT` / `Ctrl-PgUp` | Previous tab    |
| `{n}gt`        | Go to tab n         |
| `:tabclose`    | Close tab           |
| `:tabonly`     | Close other tabs    |

**VSCode-specific:**

| Key            | Action                      |
| -------------- | --------------------------- |
| `Ctrl-1..9`    | Focus editor group 1-9      |
| `Ctrl-\\`      | Split editor right          |
| `Ctrl-k Ctrl-\\` | Split editor down         |
| `Ctrl-w`       | Close editor                |

## Code Navigation

| Key            | VSCode Action                    |
| -------------- | -------------------------------- |
| `gd`           | Go to definition                 |
| `gD`           | Peek definition                  |
| `gi`           | Go to implementation             |
| `gy`           | Go to type definition            |
| `gr`           | Go to references                 |
| `gf`           | Go to file under cursor          |
| `gF`           | Go to file:line under cursor     |
| `gO`           | Go to symbol in file             |
| `Ctrl-]`       | Go to definition (alternative)   |
| `Ctrl-t`       | Go back (pop tag stack)          |
| `Ctrl-w gd`    | Open definition in split         |
| `Ctrl-w gf`    | Open file in split               |
| `[d`           | Go to previous diagnostic        |
| `]d`           | Go to next diagnostic            |
| `[g`           | Previous change (git)            |
| `]g`           | Next change (git)                |
| `[[`           | Previous section/function        |
| `]]`           | Next section/function            |
| `[{`           | Previous unmatched `{`           |
| `]}`           | Next unmatched `}`               |
| `[(`           | Previous unmatched `(`           |
| `])`           | Next unmatched `)`               |

## Code Actions & Refactoring

| Key                | VSCode Action                  |
| ------------------ | ------------------------------ |
| `Ctrl-.`           | Quick fix / code actions       |
| `Shift-Alt-F`      | Format document                |
| `=` (visual)       | Format selection               |
| `Ctrl-Shift-O`     | Go to symbol in file           |
| `Ctrl-T`           | Go to symbol in workspace      |
| `F2`               | Rename symbol                  |
| `Shift-F12`        | Find all references            |
| `Alt-F12`          | Peek definition                |
| `Ctrl-K Ctrl-I`    | Show hover                     |
| `Ctrl-Space`       | Trigger suggest                |
| `Ctrl-Shift-Space` | Trigger parameter hints        |
| `Ctrl-/`           | Toggle line comment            |
| `Shift-Alt-A`      | Toggle block comment           |
| `Ctrl-K Ctrl-C`    | Add line comment               |
| `Ctrl-K Ctrl-U`    | Remove line comment            |

## Explorer Navigation

> Works in Explorer, File Trees, Quick Open, Command Palette

| Key                 | Action                      |
| ------------------- | --------------------------- |
| `j` / `k`           | Move down / up              |
| `h` / `l`           | Collapse / expand folder    |
| `gg`                | First item                  |
| `G`                 | Last item                   |
| `Enter` / `o`       | Open file                   |
| `Ctrl-d`            | Page down                   |
| `Ctrl-u`            | Page up                     |
| `Ctrl-f`            | Page forward                |
| `Ctrl-b`            | Page backward               |
| `/`                 | Start filter/search         |
| `Esc`               | Clear filter / exit focus   |
| `zo` / `zc`         | Expand / collapse folder    |
| `zO` / `zC`         | Expand/collapse recursively |
| `zM`                | Collapse all                |
| `zR`                | Expand all                  |

## Explorer File Operations

| Key | Action                   |
| --- | ------------------------ |
| `a`   | New file                 |
| `A`   | New folder               |
| `r`   | Rename file/folder       |
| `d`   | Delete file/folder       |
| `x`   | Cut file/folder          |
| `y`   | Copy file/folder         |
| `p`   | Paste file/folder        |
| `v`   | Open file to the side    |
| `s`   | Open file in split       |
| `R`   | Refresh explorer         |
| `C`   | Copy path                |
| `Y`   | Copy relative path       |
| `/`   | Search in folder         |

## Hover & Documentation

| Key                 | Action                          |
| ------------------- | ------------------------------- |
| `K`                 | Show hover / documentation      |
| `gh`                | Show hover (alternative)        |
| `Esc`               | Close hover                     |
| `j` / `k`           | Scroll hover down / up          |
| `h` / `l`           | Scroll hover left / right       |
| `Ctrl-f`            | Page down in hover              |
| `Ctrl-b`            | Page up in hover                |
| `Ctrl-d`            | Half page down                  |
| `Ctrl-u`            | Half page up                    |
| `Tab`               | Focus next element              |
| `Shift-Tab`         | Focus previous element          |
| `gg` / `G`          | Top / bottom of hover           |

## VSCode Integrations

| Key                 | Action                          |
| ------------------- | ------------------------------- |
| `Ctrl-p`            | Quick open file                 |
| `Ctrl-Shift-p`      | Command palette                 |
| `Ctrl-Shift-f`      | Search in files                 |
| `Ctrl-Shift-h`      | Replace in files                |
| `Ctrl-Shift-e`      | Focus explorer                  |
| `Ctrl-Shift-g`      | Focus source control            |
| `Ctrl-Shift-d`      | Focus debug                     |
| `Ctrl-Shift-x`      | Focus extensions                |
| `Ctrl-b`            | Toggle sidebar                  |
| `Ctrl-j`            | Toggle panel                    |
| `` Ctrl-` ``        | Toggle terminal                 |
| `Ctrl-Shift-n`      | New window                      |
| `Ctrl-Shift-w`      | Close window                    |
| `Ctrl-k v`          | Open markdown preview           |
| `Ctrl-k z`          | Toggle zen mode                 |
| `F11`               | Toggle fullscreen               |
| `Alt-Up/Down`       | Move line up/down               |
| `Shift-Alt-Up/Down` | Copy line up/down               |
| `Ctrl-Shift-L`      | Select all occurrences          |
| `Ctrl-d`            | Add selection to next find      |
| `Ctrl-k Ctrl-d`     | Skip selection                  |
| `Ctrl-u`            | Undo last cursor operation      |
| `Ctrl-Shift-[/]`    | Fold/unfold region              |
| `Ctrl-k Ctrl-0`     | Fold all                        |
| `Ctrl-k Ctrl-j`     | Unfold all                      |

## Advanced Tips

### Combining Operators with Motions

**Format:** `<operator><count><motion>`

Examples:

- `d3w` - delete 3 words
- `c2j` - change current and 2 lines below
- `y5k` - yank current and 5 lines above
- `>3j` - indent current and 3 lines below
- `gU2w` - uppercase 2 words
- `=i{` - auto-indent inside braces

### Repeat Commands

- `.` - repeat last change
- `@:` - repeat last Ex command
- `@@` - repeat last macro
- `&` - repeat last substitute
- `;` - repeat last f/F/t/T

### Multiple Cursors (Visual Block)

1. `Ctrl-v` - start visual block
2. Select area with `j/k/h/l`
3. `I` - insert before block
4. Type your text
5. `Esc` - apply to all lines

### Search and Replace Tricks

- `:%s//replacement/g` - replace last search
- `:&&` - repeat last substitute with same flags
- `:'<,'>s/\%Vfoo/bar/g` - only in visual selection
- `:%s/foo/bar/gn` - count matches without replacing

### Working with Multiple Files

- `:buffers` or `:ls` - list open buffers
- `:b <name>` - switch to buffer by name/number
- `:bn` / `:bp` - next/previous buffer
- `:bd` - close buffer
- `:ball` - open all buffers in windows

### Global Commands

- `:g/pattern/d` - delete all lines matching pattern
- `:g!/pattern/d` or `:v/pattern/d` - delete non-matching
- `:g/TODO/yank A` - yank all TODO lines to register a
- `:g/^$/d` - delete all empty lines

### Number Increment/Decrement

- `Ctrl-a` - increment number under cursor
- `Ctrl-x` - decrement number under cursor
- `g Ctrl-a` - increment in visual block (sequential)

### Custom Commands via VSCode

Map VSCode commands in your settings:

```json
{
  "vim.normalModeKeyBindings": [
    {
      "before": ["<leader>", "f", "f"],
      "commands": ["workbench.action.quickOpen"]
    }
  ]
}
```

## Quick Reference Card

**Most Used Commands:**

- `hjkl` - move cursor
- `w/b` - word forward/back
- `0/$` - line start/end
- `gg/G` - file start/end
- `i/a/o` - insert mode
- `v/V` - visual mode
- `d/c/y` - delete/change/yank
- `p/P` - paste
- `u/Ctrl-r` - undo/redo
- `.` - repeat
- `/` `n` - search
- `*/#` - search word
- `gd` - go to definition
- `K` - hover docs
- `Ctrl-p` - quick open
- `Ctrl-.` - quick fix

**Pro Tips:**

1. Use text objects: `ci"`, `da{`, `yit`
2. Set marks for quick navigation: `ma`, `` `a ``
3. Record macros for repetitive tasks: `qa...q @a`
4. Use registers for multiple clipboards: `"ayy "ap`
5. Master visual block mode for column editing
6. Combine motions with counts: `3w`, `5j`, `2f.`
7. Use `Ctrl-o/i` to navigate jump history
8. Remember `.` repeats, `;` repeats f/t motions

> **Learn more:** [Vim Tips Wiki](https://vim.fandom.com/wiki/) | [VSCode Neovim Extension](https://github.com/vscode-neovim/vscode-neovim)
