# 我的 vim 配置脚本

> 只为方便我配置 vim 到新机器上，仓库都已导入到 gitee.com 加速。

## 克隆的 amix 的 vim 配置(蛤蛤蛤~)

```bash
git clone https://gitee.com/shrekuu/amix-vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh

```

## 增加 monokai 配色

```bash
git clone https://github.com/fratajczak/one-monokai-vim.git ~/.vim_runtime/my_plugins

# 也可再装两个

git clone https://gitee.com/shrekuu/vim-molokai.git ~/.vim_runtime/my_plugins/molokai
git clone https://gitee.com/shrekuu/vim-molokayo.git ~/.vim_runtime/my_plugins/molokayo
```

## 创建个人配置文件

```bash
touch ~/.vim_runtime/my_configs.vim
```

把下面的配置复制进去

```vim
colorscheme molokai       " molokai color scheme
" colorscheme molokayo      " molokai color scheme
let g:molokai_original=1
set background=dark

set number                " set line number
set showcmd               " show command when type

" switch buffer
map <C-K> :bnext<CR>
map <C-J> :bprev<CR>

" switch tab
map <C-L> :tabn<CR>
map <C-H> :tabp<CR>

" Enable the list of buffers
let g:airline#extensions#tabline#enabled = 1

" Show just the filename
let g:airline#extensions#tabline#fnamemod = ':t'

" quit buffer
map <leader>q :bd<CR>

" auto open the current file dir when open nerdtree
autocmd BufEnter * lcd %:p:h

" map the multiple_cursor_next_key back to C-n, C-s does not work
let g:multi_cursor_next_key='<C-n>'

" airline font fix
" let airline_left_sep=''
" let airline_right_sep=''

" remove highlighting search result quickly
map <leader>h :set hlsearch!<cr>

" share system clipboard
set clipboard=unnamed

" disable folding
set nofoldenable

" add syntax highlight for *.conf files
:autocmd BufRead,BufNewFile logging.conf setf dosini
```

好了, 预览一下:

![截图](https://camo.githubusercontent.com/4cd35820d082afc0fe12a2c1acbc809b8c7826d0/687474703a2f2f7777312e73696e61696d672e636e2f6c617267652f30303575683444536c79316676307a733661646b666a33306d683066797461792e6a7067)



## 参考

- https://github.com/amix/vimrc
- https://github.com/tomasr/molokai
- https://github.com/fmoralesc/molokayo

