# tmux

Default prefix: C-b (`CTRL` + `b`)

### Windows

Command | Description
--- | ---
prefix +  `c` | create new window
prefix + `n` | cycle to next window
prefix + `p` | cycle to previous window

### Panes

Command | Description
--- | ---
prefix + `%` | split vertically
prefix + `"` | split horizontally
prefix + `<arrow>` | switch pane
prefix + `d` | close pane
prefix + `z` | toggle full screen pane
prefix + `C-<arrow key>` | resize pane in direction of arrow

### Sessions

Command | Description
--- | ---
prefix + `d` | detach current session
prefix + `D` | choose session to detach
`tmux ls` | see list of active sessions
`tmux attach -t <number>` | attach open session
