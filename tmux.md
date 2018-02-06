# tmux

Default prefix: C-b (`CTRL` + `b`)

### Windows

Command | Description
--- | ---
prefix +  `c` | Create new window
prefix + `n` | Cycle to next window
prefix + `p` | Cycle to previous window

### Panes

Command | Description
--- | ---
prefix + `%` | Split vertically
prefix + `"` | Split horizontally
prefix + `<arrow>` | Switch pane
prefix + `d` | Close pane
prefix + `z` | Toggle full screen pane
prefix + `C-<arrow key>` | Resize pane in direction of arrow

### Sessions

Command | Description
--- | ---
prefix + `d` | Detach current session
prefix + `D` | Choose session to detach
`tmux ls` | See list of active sessions
`tmux attach -t <number>` | Attach open session
