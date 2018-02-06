# tmux

Default prefix: C-b (`CTRL` + `b`)

### Windows

Action | Command
--- | ---
Create new window | prefix +  `c`
Cycle to next window | prefix + `n`
Cycle to previous window | prefix + `p`

### Panes

Action | Command
--- | ---
Split vertically | prefix + `%`
Split horizontally | prefix + `"`
Switch pane | prefix + `<arrow>`
Close pane | prefix + `d`
Toggle full screen pane | prefix + `z`
Resize pane in direction of arrow | prefix + `C-<arrow key>`

### Sessions

Action | Command
--- | ---
Detach current session | prefix + `d`
Choose a session to detach | prefix + `D`

- To see a list of active sessions: `tmux ls`
- To attach an open session: `tmux attach -t <number>`