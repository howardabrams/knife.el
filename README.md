# knife.el

An *completion-oriented* interface to the `knife` CLI through Emacs.
This builds `knife` commands from completing read functions and
executes the results.

Anyone who plays with Chef's `knife` command realizes that, while
flexible, has a dizzying array of options, commands, sub-commands
and sometimes, sub-sub-commands. I figured that I could use the
IDO's `ido-completing-read` function at each step along the way to
build up the command line. Once you've executed it once, it
remembers it, so that calling `M-x knife` again, allows you to
select a previous knife call, or create another.

If you're `knife` command work with the default configuration
file, then you can start a `knife client show` or `knife node
show`, it will automatically populate the list of the available
nodes.

If the command typed ends with a `-c`, it prompts for a knife
configuration file (change the `knife--config-directory` for the
default directory for this).

If the command typed ends with a `-o`, it prompts for a directory
containing the cookbook you want to upload (change the
`knife--repository-directory` for the default directory value for
this).
