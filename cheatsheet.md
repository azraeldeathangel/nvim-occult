### Modes Reference
- `[Esc]` — Exit insert/visual/replace mode to return to normal mode
- `:` — Enters command-line mode (while in normal mode)

#### File Operations
```plaintext
:w            = Save file
:wq           = Save and quit
:wq!          = Force save and quit (read-only files)
:w <file>     = Save as <file>
:q            = Quit current file
:q!           = Force quit without saving
:qa!          = Quit all without saving
```

#### Undo / Redo
```plaintext
u             = Undo last change
U             = Undo all changes on the current line
Ctrl + r      = Redo last undo
```

#### Delete / Copy / Paste (Operators)
**Delete (d)** + Motion
```plaintext
x             = Delete character under cursor
dw            = Delete word from cursor
d$            = Delete to end of line
dd            = Delete current line
dX            = Delete X lines (e.g. d5)
```

**Copy (y)** + Motion
```plaintext
yw            = Yank word
yaw           = Yank word under cursor (with whitespace)
yy            = Yank current line
v + motion + y = Visual select and yank
```

**Paste (p)**
```plaintext
p             = Paste after cursor
P             = Paste before cursor
vp            = Paste what was visually selected
```

**Copy Entire File**
```plaintext
ggVGy         = Yank everything (top to bottom)
```

#### Insert / Append
```plaintext
i             = Insert before cursor
a             = Insert after cursor
o             = Insert on a new line below
O             = Insert on a new line above
```

#### Change / Replace
**Change (c)** + Motion
```plaintext
ce            = Change to end of word
c$            = Change to end of line
```

**Replace (r / R)**
```plaintext
r<char>       = Replace one character
R             = Replace multiple characters (overwrite mode)
```

#### Search & Replace
**Search**
```plaintext
/word         = Search forward
n             = Next match
N             = Previous match
*             = Search word under cursor
```

**Search Settings**
```plaintext
:set ic       = Ignore case
:set noic     = Case-sensitive
:set invic    = Toggle ignore-case
:set hls      = Highlight search matches
:set nohl     = Clear search highlights
:set is       = Show matches while typing (live search)
```

**One-time ignore-case:** `/word\c`

#### Substitute
```plaintext
:s/old/new/g          = Replace in current line
:1,3s/old/new/g       = Replace in lines 1 to 3
:%s/old/new/g         = Replace in whole file
:%s/old/new/gc        = Replace in whole file with confirmation
```

#### Cursor Movement & Motions
```plaintext
h / l         = Left / Right
j / k         = Down / Up
w             = Start of next word
e             = End of current word
b             = Beginning of previous word
0             = Start of line
$             = End of line
gg            = Top of file
G             = Bottom of file
<number>G     = Go to line <number>
Ctrl + G      = Show file status and position
```

#### Visual Mode & Selection
```plaintext
v             = Visual mode (character-wise)
V             = Visual line mode
Ctrl + v      = Visual block mode
```

#### Save selection to a new file
```plaintext
:'<,'>w <filename>     = Save selected lines
```

#### External & File Insert
```plaintext
:!<cmd>       = Run external shell command
:r <file>     = Insert contents of file below current line
:r !<cmd>     = Insert output of command
```

#### Misc
```plaintext
%             = Jump to matching (), {}, []
<Space>       = Leader key (used for custom mappings)
```
