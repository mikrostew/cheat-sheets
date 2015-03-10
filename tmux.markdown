# tmux

## sessions

### list sessions

    $ tmux list-sessions
           ls

### new session

    $ tmux new-session [-s session-name]
           new

### attach session

    $ tmux attach-session [-t target-session]
           attach
           at
           a

key bindings:

    <C-b> s     # interactively select session

### rename session

    $ tmux rename-session [-t target-session] new-name
           rename

key bindings:

    <C-b> $     # interactive rename

### detach client

    $ tmux detach-client [-t target-client]
           detach

key bindings:

    <C-b> d     # detach current client
    <C-b> D     # detach other client

### kill session

    $ tmux kill-session [-t target-session]


## key bindings

### list bindings

    $ tmux list-keys [-t key-table]
           lsk

`key-table` is one of: `vi-edit`, `emacs-edit`, `vi-choice`, `emacs-choice`, `vi-copy`, or `emacs-copy`

key bindings:

    <C-b> ?     # list key bindings

## panes

### splits

    <C-b> %     # vertical split
    <C-b> "     # horizontal split

### layout

    :select-layout
    <C-b> {space}   # cycle through available layouts
    <C-b> <M-1>     # even-horizonal layout
    <C-b> <M-2>     # even-vertical layout
    <C-b> <M-3>     # main-horizontal layout
    <C-b> <M-4>     # main-vertical layout
    <C-b> <M-5>     # tiled layout

### break pane into new window

    $ tmux break-pane [-t target-pane]
           breakp

### join pane to window

    $ tmux join-pane [-s src-pane] [-t dst-pane]
           joinp

