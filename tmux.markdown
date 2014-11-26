# tmux

## command line

| description | command |
|:----------- |:------- |
| show sessions | tmux ls |

## within tmux

| description | key binding | full command |
|:----------- |:------------- |:------------ |
| rename session | &lt;C-b&gt; $ | &lt;C-b&gt; :rename-session [-t current-name] [new-name] |
| detach current session | &lt;C-b&gt; d | &lt;C-b&gt; :detach |
| detach other session | &lt;C-b&gt; D | &lt;C-b&gt; :detach -t target-client |
| select session | &lt;C-b&gt; s | |

