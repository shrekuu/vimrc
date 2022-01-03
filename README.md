# 我的 vim 配置脚本

![截图](./QQ20220103-123446@2x.png)

> 只为方便我配置 vim 到新机器上，仓库都已导入到 gitee.com 加速。

## 克隆的 amix 的 vim 配置(蛤蛤蛤~)

```bash
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh

```

太慢就用国内服务器
```bash
git clone https://gitee.com/shrekuu/amix-vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
```

## 增加 one-monokai 配色

```bash
git clone https://gitee.com/shrekuu/vim-one-monokai.git ~/.vim_runtime/my_plugins/one-monokai

## 创建个人配置文件

```bash
touch ~/.vim_runtime/my_configs.vim
```

把下面的配置复制进去

```vim
colorscheme one-monokai     " one molokai color scheme
let g:molokai_original=1
set termguicolors

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

## 参考

- https://github.com/amix/vimrc
- https://github.com/fratajczak/one-monokai-vim
