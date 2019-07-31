# `i3tools` - Stuff for making `i3` more tolerable.

## `i3tag` - Dynamic workspaces for `i3`.

`i3tag` provides dynamic workspaces for `i3`, à la `wmii`.

To use it, you'll want to use key bindings like the following in your `i3`
configuration:

    bindsym $mod+t exec i3tag switch
    bindsym $mod+1 exec i3tag switch 1
    bindsym $mod+2 exec i3tag switch 2
    bindsym $mod+3 exec i3tag switch 3
    bindsym $mod+4 exec i3tag switch 4
    bindsym $mod+5 exec i3tag switch 5
    bindsym $mod+6 exec i3tag switch 6
    bindsym $mod+7 exec i3tag switch 7
    bindsym $mod+8 exec i3tag switch 8
    bindsym $mod+9 exec i3tag switch 9

    bindsym $mod+Shift+t exec i3tag move
    bindsym $mod+Shift+1 exec i3tag move 1
    bindsym $mod+Shift+2 exec i3tag move 2
    bindsym $mod+Shift+3 exec i3tag move 3
    bindsym $mod+Shift+4 exec i3tag move 4
    bindsym $mod+Shift+5 exec i3tag move 5
    bindsym $mod+Shift+6 exec i3tag move 6
    bindsym $mod+Shift+7 exec i3tag move 7
    bindsym $mod+Shift+8 exec i3tag move 8
    bindsym $mod+Shift+9 exec i3tag move 9

`i3tag switch <workspace>` will look for an existing workspace whose name
begins with the prefix `<workspace>:`, and focus that workspace.  If none is
found, then a workspace named `<workspace>` will be created and focused.

Without a workspace argument, `i3tag switch` will prompt (using `rofi`) for
a workspace to switch to. The `move` variant of the commands are analogous, but
move the currently focused container to the workspace, instead of focusing it.

This allows behavior almost identical to the default `$mod[-Shift]-t` and
`$mod[-Shift]-<N>` from `wmii`.
