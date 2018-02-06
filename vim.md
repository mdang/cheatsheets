# vim

### Exiting

Command | Description
--- | ---
`:wq`, `:x`, `ZZ` | write (save) file, exit
`:w` | write (save) file, but don't exit
`:q` | quit
`:q!` | force quit without saving

### Cursor Movement

Command | Description
--- | ---
`h` | move cursor left
`j` | move cursor up
`k` | move cursor down
`l` | move cursor right
`H` | move cursor to top of screen
`M` | move cursor to middle of screen
`L` | move cursor to bottom of screen
`w` | move forward to start of word
`W` | move forward to start of word (can contain punctuation)
`e` | move forward to end of word
`E` | move forward to end of word (can contain punctuation)
`b` | move backward to start of word
`B` | move backward to start of word (can contain punctuation)
`%` | move to matching character (default supported pairs: '()', '{}', '[]')
`0` | move to start of line
`^` | move to first non-blank character of line
`$` | move to end of line
`gg` | go to first line of document
`G` | go to last line of document
`5G` | go to line 5
`Ctrl` + `f` | move forward one full screen
`Ctrl` + `b` | move back one full screen
`Ctrl` + `d` | move forward 1/2 screen
`Ctrl` + `u` | move back 1/2 screen 

### Inserting

Command | Description
--- | ---
`i` | insert before cursor
`I` | insert at beginning of line
`a` | append at end of cursor
`A` | append at end of line
`o` | append (start a new line) below cursor
`O` | append (start a new line) above cursor
`ea` | append at end of word
`Esc` | escape insert mode

### Editing

Command | Description
--- | ---
`r` | replace single character
`cc` | replace entire line
`cw` | change to end of word
`c$` | change to end of line
`u` | undo
`Ctrl` + `r` | redo
`.` | repeat last command 

### Cut and Paste

Command | Description
--- | ---
`yy` | yank (copy) a line
`2yy` | yank (copy) two lines
`y$` | yank (copy) to end of line
`dd` | delete (cut) a line
`2dd` | delete (cut) two lines
`d$` | delete (cut) to end of line
`x` | delete (cut) character
`p` | paste after cursor
`P` | paste before cursor

### Visual Mode 

Command | Description
--- | ---
`v` | starts visual mode
`V` | starts line visual mode
`Ctrl` + `v` | starts block visual mode 
`o` | move to other end of selection
`aw` | select word
`ab` | select block with ()
`aB` | select block with {}
`ib` | select inner block with ()
`iB` | select inner block with {}
`Esc` | escape visual mode

### Visual Mode Commands

Command | Description
--- | ---
`>` | tab right
`<` | tab left
`y` | yank (copy) selected text
`d` | delete selected text

### Search and Replace

Command | Description
--- | ---
`/` | search for pattern
`n` | jump to next result
`N` | jump to previous result
`:%s/old/new/g` | replace all **old** with **new** in file

### Search in Multiple Files

Command | Description
--- | ---
`:vimgrep /foo/ **/*` | search for pattern in multiple files
:cn | jump to next result
:cp | jump to previous match

## NERDTree

Command | Description
--- | ---
`o` | open 
`t` | open file or directory in new tab
`i` | open file or directory split
`C` | change tree root to the selected directory
`u` | move tree root up one directory
`R` | refresh current root
`I` | toggle hidden file visibility
`Ctrl` + `ww` | switch between panes in a window
`:ls` | list buffers
`:bn` | switch to next buffer 
`:bp` | switch to previous buffer
`:bp 2` | switch to buffer #2

> Add the following to `~/.vimrc` to toggle NERDTree file explorer:

```
map <C-e> :NERDTreeToggle<CR>
```

Command | Description
--- | ---
`Ctrl` + `e` | toggle NERDTree file explorer

> Note: In Vim, [buffers act more like tabs](https://stackoverflow.com/questions/102384/using-vims-tabs-like-buffers) and tabs act more like a collection of these buffers. 

Command | Description
--- | ---
`gt` | switch to next tab
`gT` | switch to previous tab
 
> Add the following to `~.vimrc` for the following shortcuts which are easier to remember than above:

```
map  <C-l> :bn<CR>
map  <C-h> :bp<CR>
```

Command | Description
--- | ---
`Ctrl` + `l` | switch to next buffer
`Ctrl` + `h` | switch to previous buffer

## CtrlP

Fuzzy finder, find and jump to files quickly

Command | Description
--- | ---
`Ctrl` + `p` | bring up search

## vim-commenter

Command | Description
--- | ---
`gcc` | comment/uncomment [count] lines
`gc<motion>` | comment/uncomment lines that motion goes over
`<Visual>gc` | comment/uncomment the selected lines

## vim-multiple-cursors

Multiple selection style from Sublime

Command | Description
--- | ---
`Ctrl` + `n` | Press to select each occurance on the page, then press `v` to go back to normal mode and continue editing

## Tagbar

Class outline viewer for Vim

Command | Description
--- | ---
`:TagbarToggle` | toggle class outline

## Emmet 

Usage: [docs](https://raw.githubusercontent.com/mattn/emmet-vim/master/TUTORIAL)

Command | Description
--- | ---
`Ctrl` + `y` + `,` | Enter in prompt (e.g. li*3) and hit this sequence
`Ctrl` + `y` + `n` | Go to the next editable area 
