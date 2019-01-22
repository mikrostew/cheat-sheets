# netrw (in vim)

See `:help netrw-quickmap` for reference to all of these commands.

### working with files and directories

    %     # create file
    d     # create directory
    D     # delete file or directory
    R     # rename/move file

    mt    # current browsing directory becomes markfile target
    mf    # mark a file
    mc    # copy marked files to marked-file target directory
    

### navigation

    <CR>  # enter file/dir
    -     # go up one directory
    o     # enter the file/dir in a new horizontal split
    p     # preview the file
    t     # enter the file/dir in a new tab
    v     # enter the file/dir in a new vertical split

### sorting and listing

    gh    # hide/unhide dot files
    r     # reverse sort order
    s     # select sort style: name, time, or file size
    S     # use suffix priority for name sorting

### additions from the vim-vinegar plugin

    .     # pre-populate file at the end of a : command line
    !     # pre-populate file at the end of a ! command line
    y.    # yank an absolute path to the file under the cursor
