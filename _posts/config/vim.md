---
title: Vim
---

```bash
" 02.2 Inserting text

" see what mode you are in
set showmode

" 03.6 Telling where you are

" display line number
set number
" display cursor position
set ruler

" 03.8 Simple searches

" Ignoring case
set ignorecase
" Highlighting matches
set hlsearch
" match the string while typing
set incsearch

" 05.2 The example vimrc file explained

" let Vim working in an improved way, not completely Vi compatible
set nocompatible
" In insert mode the <BS> is allowed to delete the white line space
" at the start of the line, a line break and the character before
" where Insert mode started
set backspace=indent,eol,start

" 05.8 Often used options

set listchars=tab:>-,trail:-
" 06.x Using syntax highlighting

" switch it on only when the terminal supports colors
set background=dark
if &t_Co > 1
    syntax enable
endif

" 24.2 Showing matches

" show matches of (), [], {}
set showmatch

" 25.3 Indents and tabs

" insert indent automatically
set autoindent
" to make '>>' insert four spaces worth of indent
set shiftwidth=4
" make <Tab> key insert four spaces worth of indent
set softtabstop=4

" 25.4 Dealing with long lines

" breaking at words
set linebreak

" 30.2 Indenting C style text

set cindent

" 30.3 Automatic indenting

" enable detecting the type of a file
" then search for an indent file for this type of file
filetype indent on

" 30.4 Other indenting

set smartindent

" 30.5 Tabs and spaces

" <TAB> inserts 4 spaces
set softtabstop=4
" <Tab> key inserts a series of spaces
set expandtab

" 45.3 Using another encoding

set encoding=utf-8

" Others

" Color bar at column 80
set colorcolumn=80
highlight ColorColumn ctermbg=red guibg=red
" Highlight the line currently under cursor
set cursorline
" auto wrap line
set wrap
" status bar
set laststatus=2
" spell check
" set spell spelllang=en_us
" no backup file x.py~
set nobackup
" no swap file .x.py.swp
set noswapfile
" monitor if file is changed while open
set autoread
" command line completion
set wildmenu
set wildmode=longest:list,full
" redraw only when we need to
set lazyredraw
" Use TAB in makefile
autocmd FileType make setlocal noexpandtab
```