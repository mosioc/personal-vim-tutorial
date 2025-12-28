# Personal Vim Tutorial

Welcome to your personal Vim tutorial repository! This repository contains comprehensive resources to help you master Vim, from basic commands to advanced features.

## 📚 Table of Contents

1. [Getting Started](#getting-started)
2. [Core Concepts](#core-concepts)
3. [Essential Commands](#essential-commands)
4. [Advanced Operations](#advanced-operations)
5. [Power User Tips](#power-user-tips)
6. [Cheat Sheets](#cheat-sheets)

## 🚀 Getting Started

Vim is a highly configurable text editor built to enable efficient text editing. It's an improved version of the Vi editor distributed with most UNIX systems.

### Basic Modes
- **Normal Mode**: Default mode for navigation and commands
- **Insert Mode**: For typing text
- **Visual Mode**: For selecting text
- **Command Mode**: For executing commands

## 💡 Core Concepts

### Mode Switching
- `Esc` or `Ctrl-[`: Return to Normal Mode
- `i`: Enter Insert Mode
- `I`: Enter Insert Mode at start of line
- `a`: Enter Insert Mode after cursor
- `A`: Enter Insert Mode at end of line
- `o`: Open new line below
- `O`: Open new line above
- `v`: Enter Visual Mode
- `V`: Enter Visual Line Mode
- `:`: Enter Command Mode

### Basic Navigation
- `h`, `j`, `k`, `l`: Move cursor left, down, up, right
- `w`: Move to next word
- `b`: Move to previous word
- `0`: Move to start of line
- `$`: Move to end of line
- `^`: Move to first non-blank character

## 📖 Essential Commands

### File Operations
- `:q` - Quit current buffer
- `:q!` - Force quit without saving
- `:w` - Save current file
- `:wq` - Save and quit
- `:e <filename>` - Open new file
- `:Ex` - Open file explorer

### Text Manipulation
- `d` - Delete
- `D` - Delete from cursor to end of line
- `y` - Yank (copy)
- `Y` - Yank entire line
- `p` - Paste below cursor
- `P` - Paste above cursor
- `u` - Undo
- `Ctrl-r` - Redo
- `x` - Delete character under cursor
- `r` - Replace single character
- `~` - Toggle case of character

### Search and Navigation
- `/pattern` - Search forward
- `?pattern` - Search backward
- `n` - Next search result
- `N` - Previous search result
- `*` - Search word under cursor
- `f<char>` - Find character forward
- `F<char>` - Find character backward
- `;` - Repeat last find forward
- `,` - Repeat last find backward

### Word Navigation
- `w` - Next word start
- `W` - Next WORD start (including punctuation)
- `b` - Previous word start
- `B` - Previous WORD start
- `e` - End of word
- `E` - End of WORD
- `ge` - End of previous word
- `gE` - End of previous WORD

## 🔥 Advanced Operations

### Buffers and Windows
- `:ls` - List buffers
- `:bn` - Next buffer
- `:bp` - Previous buffer
- `Ctrl-w s` - Split window horizontally
- `Ctrl-w v` - Split window vertically
- `Ctrl-w w` - Switch between windows
- `Ctrl-w h/j/k/l` - Move to window

### Marks and Jumps
- `ma` - Set mark 'a'
- `'a` - Jump to mark 'a'
- `:marks` - List all marks
- `Ctrl-o` - Go back in jump list
- `Ctrl-i` - Go forward in jump list

---
> => Operator = what to do  
> => Motion / Text Object = where to do it

### Operatos 
| Operator | Name                 |
| -------- | -------------------- |
| `d`      | delete               |
| `c`      | change               |
| `y`      | yank                 |
| `>`      | shift right          |
| `<`      | shift left           |
| `=`      | indent               |
| `g~`     | toggle case          |
| `gu`     | lowercase            |
| `gU`     | uppercase            |
| `!`      | filter               |
| `zf`     | fold                 |
| `gq`     | format text          |
| `gw`     | format (keep cursor) |
| `~`      | toggle case (visual) |

### Text Objects (Motions)
> [operator] + [text object]    
> [operator] + (`i` | `a`)    
- operator + `iw` - Inside word
- operator + `i"` - Inside quotes
- operator + `i(` - Inside parentheses
- operator + `i{` - Inside braces
- operator + `aw` - Around word
- operator + `a"` - Around quotes
- operator + `a(` - Around parentheses
- operator + `a{` - Around braces

### Search and Replace
- `:s/old/new` - Replace first occurrence
- `:s/old/new/g` - Replace all occurrences
- `:%s/old/new/g` - Replace in entire file
- `:%s/old/new/gc` - Replace with confirmation

### Registers
- `"ay` - Yank to register 'a'
- `"ap` - Paste from register 'a'
- `:reg` - Show registers
- `"+y` - Yank to system clipboard
- `"+p` - Paste from system clipboard

## 💪 Power User Tips

### Batch Processing
```vim
:args **/*.[ch]           " Load all C source and header files
:argdo %s/foo/bar/ge | update  " Replace 'foo' with 'bar' in all files
```

### Quick Window Management
- `Ctrl-w =` - Make all windows equal width/height
- `Ctrl-w _` - Maximize current window height
- `Ctrl-w |` - Maximize current window width
- `Ctrl-w r` - Rotate windows
- `Ctrl-w x` - Exchange current window with next

### Advanced Marks
- `'` - Jump to line of mark
- `` ` `` - Jump to exact position of mark
- `[` and `]` - Start and end of last changed/yanked text
- `<` and `>` - Start and end of last visual selection
- `.` - Position of last change

### Clipboard Integration
- `"+y` - Yank to system clipboard
- `"+p` - Paste from system clipboard
- `:set clipboard=unnamed` - Use system clipboard by default

### Quick File Operations
- `:saveas <file>` - Save as new file
- `:w <file>` - Save copy to new file
- `:e!` - Reload current file
- `:cd <dir>` - Change directory
- `:pwd` - Print working directory

## 📋 Command Examples

### Combining Commands with Numbers
- `d7j` - Delete from current line to 7 lines below (same as `7dj`)
- `d2w` - Delete two next words (same as `2dw`)
- `3D` - Delete 3 lines
- `de` - Delete current word to end
- `d%` - Delete until first matching bracket/parenthesis
- `3u` - Undo 3 last changes
- `4Ctrl-r` - Redo 4 last changes
- `3cw` - Change 3 words and enter Insert Mode
- `2rm` - Replace 2 'm' characters with current character
- `4x` - Delete 4 characters
- `y5w` - Yank 5 words
- `3p` - Paste 3 times
- `5.` - Repeat last command 5 times

### Line Commands
- `dd` - Delete current line
- `cc` - Replace current line and enter Insert Mode
- `yy` - Copy current line
- `4dd` - Delete 4 lines
- `3cc` - Change 3 lines and enter Insert Mode
- `5yy` - Yank 5 lines
- `3pp` - Paste 3 times

### Indentation
- `>>` - Indent to right
- `<<` - Indent to left
- `4>>` - 4 indentations to right
- `2<<` - 2 indentations to left

### Text Objects
- `diw` - Delete inside word
- `dip` - Delete inside paragraph
- `da(` - Delete around parentheses
- `yip` - Yank inside paragraph
- `yi(` - Yank inside parentheses
- `di"` - Delete inside double quotes
- `ca[` - Change around brackets

### Registers
- `"ayy` - Yank current line into register 'a'
- `"byiw` - Yank current word into register 'b'
- `"add` - Delete current line and store in register 'a'
- `"bx` - Delete character under cursor and store in register 'b'
- `"ap` - Paste contents of register 'a' after cursor
- `"bP` - Paste contents of register 'b' before cursor
- `"Ayy` - Yank current line and append to register 'a'

## 🎯 Cheat Sheets

### Quick Reference
![Vim Cheatsheet](Cheat%20Sheets/Vim-Cheatsheet-2-Final-Draft.png)

### Visual Guides
- [Vim Cheatsheet Final Draft](Cheat%20Sheets/Vim-Cheatsheet-2-Final-Draft.png)
- [Vim Cheat Sheet for Programmers](Cheat%20Sheets/vim_cheat_sheet_for_programmers_screen.pdf)
- [Ultimate VIM Keyboard Shortcuts](Cheat%20Sheets/Ultimate%20VIM%20Keyboard%20Shrotcuts.pdf)

### Specialized Guides
![Buffers, Windows and Tabs](Cheat%20Sheets/Buffers%2C%20Windows%20and%20Tabs.png)

- [Buffers, Windows and Tabs Guide](Cheat%20Sheets/Buffers%2C%20Windows%20and%20Tabs.png)
- [Windows Keyboard Shortcuts](Cheat%20Sheets/keyboard-shortcuts-windows.pdf)

### Additional Visual References
![Vim Cheat Sheet Light](Cheat%20Sheets/cheatsheetLight.png)

![Vim Cheat Sheet by Sysxplore](Cheat%20Sheets/Vim%20Cheet%20Sheet%20-%20by%20Sysxplore.jpg)

## 📝 Practice Tips

1. Start with basic navigation and mode switching
2. Practice common commands daily
3. Use Vim's built-in tutorial: `vimtutor`
4. Gradually incorporate more advanced features
5. Customize your `.vimrc` as you learn

## 🔗 Additional Resources

### Dotfiles
The [dotfiles](dotfiles-public/) directory contains a comprehensive set of configuration files for various tools:

- **Neovim Configuration**: Modern Vim setup with LazyVim
- **Shell Configurations**: 
  - Fish shell setup for macOS & Linux
  - PowerShell setup for Windows
- **Git Configuration**: Optimized git settings
- **Terminal Setup**: Various terminal configurations and themes

### Configuration Examples
The dotfiles include:
- Modern Neovim setup with LazyVim
- Terminal configurations (kitty, wezterm, alacritty, iterm2)
- Shell customizations (Fish, PowerShell)
- Git workflow optimizations
- Various development tool configurations

## 🎓 Learning Path

1. **Beginner**
   - Basic navigation
   - Mode switching
   - Simple editing commands

2. **Intermediate**
   - Advanced navigation
   - Text objects
   - Buffers and windows

3. **Advanced**
   - Macros
   - Registers
   - Advanced search and replace
   - Custom mappings


Remember: Vim mastery comes with practice. Don't try to learn everything at once. Focus on incorporating new commands into your workflow gradually. 

