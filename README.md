# Personal Vim Tutorial

Welcome to your personal Vim tutorial repository! This repository contains comprehensive resources to help you master Vim, from basic commands to advanced features.

> [For NeoVim in VS Code go here](./vscode/vscode-version-neovim.md).

## Table of Contents

1. [Getting Started](#getting-started)
2. [Core Concepts](#core-concepts)
3. [Essential Commands](#essential-commands)
4. [Advanced Operations](#advanced-operations)
5. [Power User Tips](#power-user-tips)
6. [Cheat Sheets](#cheat-sheets)

## Getting Started

Vim is a highly configurable text editor built to enable efficient text editing. It's an improved version of the Vi editor distributed with most UNIX systems.

### Basic Modes

* **Normal Mode**: Default mode for navigation and commands
* **Insert Mode**: For typing text
* **Visual Mode**: For selecting text
* **Command Mode**: For executing commands

## Core Concepts

### Mode Switching

* `Esc` or `Ctrl-[`: Return to Normal Mode
* `i`: Enter Insert Mode
* `I`: Insert at beginning of line
* `a`: Insert after cursor
* `A`: Insert at end of line
* `o`: Open new line below
* `O`: Open new line above
* `v`: Enter Visual Mode
* `V`: Enter Visual Line Mode
* `:`: Enter Command Mode

### Navigation

#### Basic Movement

* `h`, `j`, `k`, `l`: Move cursor left, down, up, right
* `0`: Start of line
* `^`: First non-blank character of line
* `$`: End of line
* `gg`: First line of file
* `G`: Last line of file

#### Word & Text Navigation

* `w` / `W`: Start of next word / WORD
* `b` / `B`: Start of previous word / WORD
* `e` / `E`: End of word / WORD
* `ge` / `gE`: End of previous word / WORD

#### Screen Navigation

* `H`, `M`, `L`: Top, middle, bottom of screen
* `Ctrl-f`: Forward one screen (scroll)
* `Ctrl-b`: Backward one screen
* `Ctrl-d`: Forward half screen
* `Ctrl-u`: Backward half screen

#### Character & Search Navigation

* `f<char>` / `F<char>`: Move to next/previous occurrence in line
* `t<char>` / `T<char>`: Move before previous/next occurrence in line
* `;` / `,`: Repeat last f/t movement forward/backward
* `%`: Jump to matching bracket, parenthesis, or brace

## Essential Commands

### File Operations

* `:q` - Quit
* `:q!` - Force quit without saving
* `:w` - Save file
* `:wq` - Save and quit
* `:e <filename>` - Open file
* `:Ex` - File explorer
* `:saveas <file>` - Save as new file
* `:w <file>` - Save copy to new file
* `:e!` - Reload file
* `:cd <dir>` - Change directory
* `:pwd` - Print working directory

### Text Manipulation

* `x` - Delete character under cursor
* `r` - Replace single character
* `~` - Toggle case of character or selection
* `d` / `D` - Delete / Delete to end of line
* `y` / `Y` - Yank (copy) / Yank (copy) entire line
* `p` / `P` - Paste below/above cursor
* `u` - Undo
* `Ctrl-r` - Redo

### Search & Replace

* `/pattern` - Search forward
* `?pattern` - Search backward
* `n` / `N` - Next / Previous search result
* `*` / `#` - Search word under cursor forward / backward
* `:s/old/new/` - Replace first occurrence
* `:s/old/new/g` - Replace all occurrences in line
* `:%s/old/new/g` - Replace in entire file
* `:%s/old/new/gc` - Replace with confirmation

### Registers & Clipboard

* `"ay` / `"ap` - Yank / Paste to/from register 'a'
* `:reg` - Show registers
* `"+y` / `"+p` - Yank / Paste to/from system clipboard
* `:set clipboard=unnamed` - Use system clipboard by default

## Advanced Operations

### Buffers & Windows

* `:ls` - List buffers
* `:bn` / `:bp` - Next / Previous buffer
* `Ctrl-w s` / `Ctrl-w v` - Split window horizontally / vertically
* `Ctrl-w w` - Switch between windows
* `Ctrl-w h/j/k/l` - Move to window (left, up, bottom and right)
* `Ctrl-w =` - Equalize window sizes
* `Ctrl-w _` / `Ctrl-w |` - Maximize current window height / width
* `Ctrl-w r` - Rotate windows
* `Ctrl-w x` - Exchange current window with next

### Marks & Jumps

* `ma` - Set mark 'a'
* `'a` - Jump to line of mark 'a'
* `` `a `` - Jump to exact position of mark 'a'
* `:marks` - List all marks
* `Ctrl-o` / `Ctrl-i` - Back / Forward in jump list
* `[` / `]` - Start / end of last changed or yanked text
* `<` / `>` - Start / end of last visual selection
* `.` - Repeat last change

### Operators & Text Objects

#### Operators

| Operator | Action               |
| -------- | -------------------- |
| `d`      | Delete               |
| `c`      | Change               |
| `y`      | Yank                 |
| `>`      | Shift right          |
| `<`      | Shift left           |
| `=`      | Indent               |
| `g~`     | Toggle case          |
| `gu`     | Lowercase            |
| `gU`     | Uppercase            |
| `!`      | Filter               |
| `zf`     | Fold                 |
| `gq`     | Format text          |
| `gw`     | Format (keep cursor) |
| `~`      | Toggle case (visual) |

#### Text Objects

* [operator] + [text object] or [operator] + (`i`|`a`)
* [operator] + `iw` / `aw` - Inside / Around word
* [operator] + `i"` / `a"` - Inside / Around quotes
* [operator] + `i(` / `a(` - Inside / Around parentheses
* [operator] + `i{` / `a{` - Inside / Around braces

## Power User Tips

### Batch Processing

```vim
:args **/*.[ch]           " Load all C source and header files
:argdo %s/foo/bar/ge | update  " Replace 'foo' with 'bar' in all files
```

### Quick File Operations

* `:saveas <file>` - Save as new file
* `:w <file>` - Save copy to new file
* `:e!` - Reload current file
* `:cd <dir>` - Change directory
* `:pwd` - Print working directory

## Command Examples

### Combining Commands with Numbers

* `d7j` / `7dj` - Delete from current line to 7 lines below
* `d2w` / `2dw` - Delete the next 2 words
* `3D` - Delete 3 lines (from cursor to end of line)
* `de` - Delete current word to the end
* `d%` - Delete from cursor to matching bracket/parenthesis
* `3u` - Undo last 3 changes
* `4Ctrl-r` - Redo last 4 changes
* `3cw` - Change next 3 words and enter Insert Mode
* `2rm` - Replace next 2 'm' characters with the current character
* `4x` - Delete 4 characters under cursor
* `y5w` - Yank next 5 words
* `3p` - Paste 3 times
* `5.` - Repeat last command 5 times
* `10j` - Move down 10 lines
* `6k` - Move up 6 lines
* `5>>` - Indent next 5 lines to the right
* `3<<` - Indent next 3 lines to the left

### Line Commands

* `dd` - Delete current line
* `cc` - Change current line and enter Insert Mode
* `yy` - Yank (copy) current line
* `4dd` - Delete 4 consecutive lines
* `3cc` - Change 3 consecutive lines
* `5yy` - Yank 5 lines
* `3pp` - Paste yanked lines 3 times
* `D` - Delete from cursor to end of line
* `C` - Change from cursor to end of line and enter Insert Mode

### Indentation

* `>>` - Indent current line right
* `<<` - Indent current line left
* `4>>` - Indent next 4 lines to the right
* `2<<` - Indent next 2 lines to the left
* `>` + motion - Indent text covered by motion
* `<` + motion - Dedent text covered by motion
* `=` + motion - Auto-indent text covered by motion

### Text Objects

* `diw` - Delete inside current word
* `dip` - Delete inside paragraph
* `da(` - Delete around parentheses
* `yip` - Yank inside paragraph
* `yi(` - Yank inside parentheses
* `di"` - Delete inside double quotes
* `ca[` - Change around brackets and enter Insert Mode
* `di{` - Delete inside braces
* `da"` - Delete around quotes
* `ciw` - Change inside word
* `ci(` - Change inside parentheses

### Registers

* `"ayy` - Yank current line into register 'a'
* `"byiw` - Yank current word into register 'b'
* `"add` - Delete current line into register 'a'
* `"bx` - Delete character under cursor into register 'b'
* `"ap` - Paste contents of register 'a' after cursor
* `"bP` - Paste contents of register 'b' before cursor
* `"Ayy` - Append current line to register 'a'
* `"0y` - Yank last inserted text into register '0'
* `"+y` - Yank to system clipboard
* `"+p` - Paste from system clipboard

## Cheat Sheets

### Quick Reference

![Vim Cheatsheet](Cheat%20Sheets/Vim-Cheatsheet-2-Final-Draft.png)

### Visual Guides

* [Vim Cheatsheet Final Draft](Cheat%20Sheets/Vim-Cheatsheet-2-Final-Draft.png)

* [Vim Cheat Sheet for Programmers](Cheat%20Sheets/vim_cheat_sheet_for_programmers_screen.pdf)
* [Ultimate VIM Keyboard Shortcuts](Cheat%20Sheets/Ultimate%20VIM%20Keyboard%20Shrotcuts.pdf)

### Specialized Guides

![Buffers, Windows and Tabs](Cheat%20Sheets/Buffers%2C%20Windows%20and%20Tabs.png)

* [Buffers, Windows and Tabs Guide](Cheat%20Sheets/Buffers%2C%20Windows%20and%20Tabs.png)
* [Windows Keyboard Shortcuts](Cheat%20Sheets/keyboard-shortcuts-windows.pdf)

### Additional Visual References

![Vim Cheat Sheet Light](Cheat%20Sheets/cheatsheetLight.png)

![Vim Cheat Sheet by Sysxplore](Cheat%20Sheets/Vim%20Cheet%20Sheet%20-%20by%20Sysxplore.jpg)

## Practice Tips

1. Start with basic navigation and mode switching
2. Practice common commands daily
3. Use Vim's built-in tutorial: `vimtutor`
4. Gradually incorporate more advanced features
5. Customize your `.vimrc` as you learn

## 🔗 Additional Resources

### Dotfiles

The [dotfiles](dotfiles-public/) directory contains a comprehensive set of configuration files for various tools:

* **Neovim Configuration**: Modern Vim setup with LazyVim
* **Shell Configurations**:
  * Fish shell setup for macOS & Linux
  * PowerShell setup for Windows
* **Git Configuration**: Optimized git settings
* **Terminal Setup**: Various terminal configurations and themes

### Configuration Examples

The dotfiles include:

* Modern Neovim setup with LazyVim
* Terminal configurations (kitty, wezterm, alacritty, iterm2)
* Shell customizations (Fish, PowerShell)
* Git workflow optimizations
* Various development tool configurations

## Learning Path

1. **Beginner**
   * Basic navigation
   * Mode switching
   * Simple editing commands

2. **Intermediate**
   * Advanced navigation
   * Text objects
   * Buffers and windows

3. **Advanced**
   * Macros
   * Registers
   * Advanced search and replace
   * Custom mappings

Remember: Vim mastery comes with practice. Don't try to learn everything at once. Focus on incorporating new commands into your workflow gradually.
