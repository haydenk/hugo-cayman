+++
title = "Vim: Essential Commands for Productivity"
date = 2024-02-01T09:30:00Z
draft = false
tags = ["vim", "editor", "productivity"]
slug = "vim-productivity"
+++

Vim's learning curve is steep, but the productivity gains are worth it.
<!--more-->

## Why Vim?

- **Speed**: Navigate and edit without touching the mouse
- **Efficiency**: Powerful commands for text manipulation
- **Availability**: Installed on virtually every Unix system
- **Customizable**: Extensive plugin ecosystem

## Essential Commands

### Navigation
- `h j k l` - Left, down, up, right
- `w` - Next word
- `b` - Previous word
- `gg` - Top of file
- `G` - Bottom of file
- `0` - Start of line
- `$` - End of line

### Editing
- `i` - Insert mode
- `a` - Append after cursor
- `o` - New line below
- `dd` - Delete line
- `yy` - Copy line
- `p` - Paste
- `u` - Undo
- `Ctrl-r` - Redo

### Search and Replace
```vim
/pattern     " Search forward
?pattern     " Search backward
n            " Next match
N            " Previous match
:%s/old/new/g " Replace all
```

### Visual Mode
- `v` - Character selection
- `V` - Line selection
- `Ctrl-v` - Block selection

## Power Combos

- `ciw` - Change inside word
- `di"` - Delete inside quotes
- `>G` - Indent from here to end
- `.` - Repeat last change

## Configuration

Basic `.vimrc`:

```vim
syntax on
set number
set relativenumber
set tabstop=2
set shiftwidth=2
set expandtab
set autoindent
```

Practice daily and Vim becomes second nature!
