VIM: Vim uses command mode and edit  (or insert) mode ( pressing i and esc to exit)

To save files you type in command mode `:w` or `:w` Namefile if it isn't named

`:q` to exit.

`:wq!` vim exits, saves and doesn't prompt before exiting. THE ORDER IS IMPORTANT!

We use the keys h (left) j (down) k (up) l (right) to move as arrow keys

In terms of words: `w` moves to the start of next word; `e` moves to the end of the word; and `b` moves to beginning of the word.

Moving within the text is not limited to individual keys; you can combine movement keys with a number. For example, `3w` is the same as pressing `w`  three times.

You can insert text multiple times.For example, an underline of a header might consist of 30 -s.

With `30i` (then we type) `-` Esc, output is 30 times ---.

In text that is structured with parentheses or brackets, ( or { or [, use % to jump to the matching parenthesis or bracket.

To find and move to the next (or previous) occurrence of a character, use `f` and `F`, e.g. `fo` finds next o.

You can combine `f` with a number. For example, you can find 3rd occurrence of 'q' with `3fq`

To reach the beginning of a line, press `0`

For the end of a line, there's `$`

Find the next occurrence of the word under cursor with `*`, and the previous with `#`

`gg` takes you to the beginning of the file; `G` to the end

To insert text into a new line, press `o` or `O`

`x` and `X` delete the character under the cursor and to the left of the cursor, respectively

When you need to replace only one character under your cursor, without changing to insert mode, use `r`.

`d` is the delete command. You can combine it with movement, e.g. `dw` deletes the first word on the right side of the cursor. It also copies the content, so that you can paste it with `p` to another location

To repeat the previous command,  press . (dot)

Also don't PANIC! If you make a mistake, press `u` for undo and `ctrl+R` for redo

If you have a problem, type `:help`

VIM SHORTCUTS (no : before letters)
```bash
g -> bottom of the file

gg -> top of the file

To jump directly to a specific line, give its line number along with G

/ -> search example: /ubuntu it would search for the word ubuntu on the file, using the n letter it skips to the next finding N to the previous.

esc + u -> undo changes

dd -> delete line

```

NANO SHORTCUTS:
```bash
ctrl +k -> cut a line
ctrl +u -> paste the line
```
