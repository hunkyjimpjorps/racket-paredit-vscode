# Strict Paredit for More Languages

Classic, Emacs Paredit-like Structural editing and navigation for Common Lisp, Clojure, Scheme, Racket and Lisp-Flavored Erlang.

<p align="center">
<a href="https://marketplace.visualstudio.com/items?itemName=ailisp.strict-paredit"><img width="128px" height="128px" src="https://github.com/ailisp/strict-paredit-vscode/raw/master/assets/paredit.png" title="Paredit icon"></img></a>
</p>

This is a [Paredit](http://mumble.net/~campbell/emacs/paredit.el) extension for [Visual Studio Code](https://code.visualstudio.com). It is a thin wrapper around [paredit.js](http://robert.kra.hn/projects/paredit-js). You find it inside Code's extension view and on [the Marketplace](https://marketplace.visualstudio.com/items?itemName=ailisp.strict-paredit).


## Commands

Note: You can choose to disable all default key bindings by configuring `paredit.defaultKeyMap` to `none`. (Then you probably also want to register your own shortcuts for the commands you often use. see `ets/keys.json` for example). By default the strict mode map is used. Below commands work in both strict mode and original mode.
If you are new to Paredit, below **shortcut in bond text** is a small but very frequently used set of commands that helps in 95% of the time. I hightly recommend you memorize them to be efficient.

### Navigation

Default keybinding | Action
------------------ | ------
**ctrl+right**     | Forward Sexp
**ctrl+left**      | Backward Sexp
**ctrl+down**      | Forward Down Sexp
**ctrl+up**        | Backward Up Sexp
ctrl+alt+right     | Close List

### Selecting

Default keybinding | Action
------------------ | ------
**ctrl+w**         | Expand Selection
ctrl+shift+w       | Shrink Selection
ctrl+alt+w         | Select Current Top Level Form

### Editing

Default keybinding                | Action
------------------                | ------
**ctrl+alt+.**                    | Slurp Forward
**ctrl+alt+<**                    | Slurp Backward
ctrl+alt+,                        | Barf Forward
ctrl+alt+>                        | Barf Backward
ctrl+alt+s                        | Splice
ctrl+alt+shift+s                  | Split Sexp
ctrl+delete                       | Kill Sexp Forward
ctrl+shift+backspace (on Mac)     | Kill Sexp Forward
ctrl+backspace                    | Kill Sexp Backward
ctrl+alt+down                     | Splice & Kill Forward
**ctrl+alt+up**                   | Splice & Kill Backward
ctrl+alt+9, Ctrl+alt+(            | Wrap Around ()
ctrl+alt+[                        | Wrap Around []
ctrl+alt+{                        | Wrap Around {}
ctrl+alt+i                        | Indent
ctrl+alt+t                        | Transpose

You can also select the sexp with **`ctrl+w`** then wrap around by typing `(`, `[` or `{` and delete it with `backsapce`

## Strict only keybinding
Strict mode keybinding            | Action
----------------------            | ------
backspace                         | Delete Backward or move left if at `)]}`
delete                            | Delete Forward or move right if at `)]}`
shift+backspace (on Mac)          | Delete Forward or move right if at `)]}`
ctrl+alt+backspace                | Force Delete Backward
ctrl+alt+delete                   | Force Delete Forward
alt+shift+backspace (on Mac)      | Force Delete Forward

NB: **Strict mode is enabled by default.** The backspace and delete keys won't let you remove parentheses or brackets so they become unbalanced. To force a delete anyway, use the supplied commands for that. Strict mode can be switched on/off by configuring `paredit.defaultKeyMap` to `strict`/`original`.


### Copying/Yanking

Default keybinding | Action
------------------ | ------
ctrl+alt+c ctrl+right         | Copy Forward Sexp
ctrl+alt+c ctrl+left          | Copy Backward Sexp
ctrl+alt+c ctrl+down          | Copy Forward Down Sexp
ctrl+alt+c ctrl+up            | Copy Backward Up Sexp
ctrl+alt+c ctrl+alt+right     | Copy Close List

### Cutting

Default keybinding | Action
------------------ | ------
ctrl+alt+x ctrl+right         | Cut Forward Sexp
ctrl+alt+x ctrl+left          | Cut Backward Sexp
ctrl+alt+x ctrl+down          | Cut Forward Down Sexp
ctrl+alt+x ctrl+up            | Cut Backward Up Sexp
ctrl+alt+x ctrl+alt+right     | Cut Close List

## Maintainers

This project is forked from https://github.com/BetterThanTomorrow/calva-paredit. Original one is maintained by author Peter Strömberg as part of project calva, https://github.com/BetterThanTomorrow/calva

I made this fork to add support for Racket.  If you've got a S-expression based language that you'd like support for, feel free to ask.

