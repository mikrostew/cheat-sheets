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

    $ tmux list-keys
           lsk

key bindings:

    <C-b> ?     # list key bindings

