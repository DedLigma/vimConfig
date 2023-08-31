https://github.com/amix/vimrc

https://github.com/preservim/nerdtree - nerdtree че ещё сказать Ctrl+t
https://github.com/Xuyuanp/nerdtree-git-plugin - показывает в nerdtree че вообще по гиту изменилось
https://github.com/ryanoasis/vim-devicons - иконочки. надо поставить шрифты

https://github.com/itchyny/lightline.vim - для вот этой вот нижней полоски

https://github.com/terryma/vim-multiple-cursors - мульти курсор Ctrl+n

https://github.com/tpope/vim-commentary - закоментить раскоментить g+c+c или g+c+направление hjkl че ещё закоментить

https://github.com/dense-analysis/ale - синтаксис чекинг Ctrl+p чтобы выпали подсказки по команде

https://github.com/maxbrunsfeld/vim-yankstack - изменение с прошлых сессий (типо вышел зашел и можешь u прожать чтоб вернуть изменения)

https://github.com/skywind3000/asyncrun.vim - асинхронность. нужен для оптимизации

https://github.com/amix/open_file_under_cursor.vim - открывает файлы под курсором g+f



```
set tabstop=4
set shiftwidth=4
set smarttab
set et
set wrap
set ai
set cin
set showmatch
set hlsearch
set incsearch
set ignorecase
syntax on
set number
set wrap linebreak nolist
set cursorline

set lz 
set listchars=tab:··
set list

set ffs=unix,dos,mac
set fencs=utf-8,cp1251,koi8-r,ucs-2,cp866

call plug#begin()
Plug 'preservim/nerdtree' | 
            \ Plug 'Xuyuanp/nerdtree-git-plugin' |
Plug 'itchyny/lightline.vim'
Plug 'ryanoasis/vim-devicons' 
Plug 'terryma/vim-multiple-cursors'
Plug 'tpope/vim-commentary'
Plug 'dense-analysis/ale'
Plug 'maxbrunsfeld/vim-yankstack'
Plug 'skywind3000/asyncrun.vim'
Plug 'amix/open_file_under_cursor.vim'

call plug#end()

" ======== NERDTREE ========================
nnoremap <leader>n :NERDTreeFocus<CR>
nnoremap <C-e> :NERDTree<CR>
nnoremap <C-t> :NERDTreeToggle<CR>
nnoremap <C-f> :NERDTreeFind<CR>
" Start NERDTree and put the cursor back in the other window.
"autocmd VimEnter * NERDTree | wincmd p

" Exit Vim if NERDTree is the only window remaining in the only tab.
autocmd BufEnter * if tabpagenr('$') == 1 && winnr('$') == 1 && exists('b:NERDTree') && b:NERDTree.isTabTree() | quit | endif
" ======== NERDTREE ========================

nnoremap <F3> :AsyncRun ctags -R<CR>
```
