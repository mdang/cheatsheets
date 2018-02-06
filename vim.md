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
`gt` | switch to next tab
`gT` | switch to previous tab

Note: 
Add the following to `~.vimrc` for the following shortcuts which are easier to remember than above:

```
map  <C-l> :tabn<CR>
map  <C-h> :tabp<CR>
map  <C-n> :tabnew<CR>
```

Command | Description
--- | ---
`Ctrl` + `l` | switch to next tab
`Ctrl` + `h` | switch to previous tab