# Better Rainbow Parentheses

This repo is mostly unmaintained - I switched to using
https://github.com/luochen1990/rainbow instead and generally suggest you do to.

Originally forked from https://github.com/kien/rainbow_parentheses.vim since
that was really unmaintained and needed some fixes.

### Installation 

Using [pathogen.vim](https://github.com/tpope/vim-pathogen):

```
cd ~/.vim/bundle
git clone git://github.com/eapache/rainbow_parentheses.vim.git
```

### Options:

The colours used; the outermost pair is coloured with the last colour in the
list, the next-outermost with the second-last colour, etc. The first element of
each entry is the terminal colour, the second element is the GUI (gvim) colour.
```vim
let g:rbpt_colorpairs = [
    \ ['red',         'RoyalBlue3'],
    \ ['brown',       'SeaGreen3'],
    \ ['blue',        'DarkOrchid3'],
    \ ['gray',        'firebrick3'],
    \ ['green',       'RoyalBlue3'],
    \ ['magenta',     'SeaGreen3'],
    \ ['cyan',        'DarkOrchid3'],
    \ ['darkred',     'firebrick3'],
    \ ['brown',       'RoyalBlue3'],
    \ ['darkblue',    'DarkOrchid3'],
    \ ['gray',        'firebrick3'],
    \ ['darkgreen',   'RoyalBlue3'],
    \ ['darkmagenta', 'SeaGreen3'],
    \ ['darkcyan',    'DarkOrchid3'],
    \ ['red',         'firebrick3'],
    \ ]
```

How deep to colour (repeating the colour list if necessary) before giving up;
limited for performance reasons.
```vim
let g:rbpt_max = 15
```

```vim
let g:rbpt_loadcmd_toggle = 0
```

Also bold parenthese to make the colours stand out more.
```vim
let g:bold_parentheses = 1      " Default on
```

### Commands:

```vim
:RainbowParenthesesToggle       " Toggle it on/off
:RainbowParenthesesLoadRound    " (), the default when toggling
:RainbowParenthesesLoadSquare   " []
:RainbowParenthesesLoadBraces   " {}
:RainbowParenthesesLoadChevrons " <>
```

### Always On:

Add the following to your `~/.vimrc` to always use Rainbow Parenthesis

```vim
au VimEnter * RainbowParenthesesToggle
au Syntax * RainbowParenthesesLoadRound
au Syntax * RainbowParenthesesLoadSquare
au Syntax * RainbowParenthesesLoadBraces
```

Or just use `RainbowParenthesesToggleAll`. You may need to put `syntax on` in
your `.vimrc` *before* you enable rainbow parentheses.
