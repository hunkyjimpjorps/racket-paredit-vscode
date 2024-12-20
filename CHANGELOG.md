## 0.3.0 - 0.3.4
Features:
- Forked to add more supported languages

## 0.2.0
Features:
- fork rename to "strict paredit"
- Strict mode map as default
- Emacs paredit like backward and forward sexp navigation, go up when backward from first or forward from last sexp
- Emacs paredit like delete `)` become move left or right
- Close parens in strict mode, unbalancing via type made impossible
- work on commonlisp mode

## 0.1.17
Features:
- Strict mode as default keybinding, prohibiting deletiion of matched parens and brackets

## 0.1.11
Features;
- Copy and cut commands for each navigation command

## 0.1.4
Features;
- Shrink selection
- Activate on other lisps than Clojure

Fixes:
- Indent ragne now works

## 0.1.1
Features:
- Ability to toggle paredit on and off

Improvements:
- Automatically indents after edits

Fixes:
- Indenting

## 0.1.0
Added the following Navigation commands:
- Expand Selection
- Close List
- Select Defn

Added the following Editing commands:
- Slurp Forward
- Slurp Backward
- Barf Forward
- Barf Backward
- Splice
- Split Sexp
- Kill Sexp Forward
- Kill Sexp Backward
- Splice & Kill Forward
- Splice & Kill Backward
- Wrap Around ()
- Wrap Around []
- Wrap Around {}
- Indent
- Transpose

## 0.0.1
Initial
- Forward Sexp
- Backward Sexp
- Forward Down Sexp
- Backward Up Sexp