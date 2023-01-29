# Vim Guidance
> This repository is vim configuration file, although it can be used for neovim.
本仓库已不再使用，作者转去使用lua配置了，具体可以转去[luavim](https://github.com/ZCDu/luavim)
# Before Installation
- nodejs (needed by coc.nvim)
- lazygit (needed by \\g)
- fzf (needed by fzf.vim) 在init.vim配置部分需要指定系统fzf安装的路径, 确定路径是一致的
- ranger *(needed by rnvimr)

# Installation
Clone this repository to $HOME as .vim, and create a soft link of init.vim to $HOME/.vimrc(ln -s .vim/init.vim $HOME/.vimrc). Then, open vimrc to auto install plugins.
If not work, run PlugInstall to manual setup(PlugInstall is a function from vim-plug).

# vim-plug
## Plug options
|Option|Description|补充说明|例子|
|----|----|----|----|
|branch/tag/commmit|Branch/tag/commmit of the repository to use|所以不需要在修改master分支名进行操作|Plug 'rdnetto/YCM-Generator', {'branch':'stable'}|
|dir|指定安装插件的目录||Plug 'junegunn/fzf', {'dir':'~/.fzf', 'do':'./install --all'}|
|do|Post-update hook(string or funcref)||Plug 'junegunn/fzf', {'dir':'~/.fzf', 'do':'./install --all'}|
|on|按需载入，只有在使用到的时候才进行|在指定指定命令的时候才会启动|Plug 'scrooloose/nerdtree', {'on': 'NERDTreeToggle'}|
|for|按需载入，启动指定文件类型的时候启动|如打开python脚本的时候才进行|Plug 'tpope/vim-fireplace', {'for': 'clojure'}|
|frozen|除非明确指定否则不进行更新|可以避免在PlugUpdate的更新这个插件||

# Basic setting
\<Leader\> : 空格
; : 被修改为了:

# Basic Grammar
noremap : 设置正常模式下的键位map
\<nop\> : 表示为空，可以通过将指定键位设置为这个值从而取消默认的绑定

# Instruction
## clipboard
- Y : 将内容复制到到系统剪贴板
- P : 粘贴系统剪贴板的内容

## terminal
- \\t : 打开一个新的st终端，在同一个文件夹下
- \<Leader\>\\ : 打开一个vim内置的terminal

## git
- \\g ： 启动lazgyit

## run
- F5 : 使用pudb来调试python代码
- R  : 简易的编译，当前只用来继续markdown编译

## windows
### move
- 空格+wkjhl ：在不同的窗口间移动
- \<Leader\>s : 快速移动到指定的字母上
### split
- su : 上下分屏，指针位于上方 
- se : 上下分屏，指针位于下方
- sn : 左右分屏，指针位于左边
- si : 左右分屏，指针位于右边
- sh : 将分屏窗口调整为水平分屏
- sv : 将分屏窗口调整为垂直分屏
- srh : 水平分屏的窗口位置对调
- srv : 垂直分屏的窗口位置对象
### Resize
- \<C-up\> : 往上移动窗口的边界
- \<C-down\> :
- \<C-right\> : 
- \<C-left\> :

## session
\\F2 : 保存当前的vim会话
\\F3 ：打开会话
\\F4 : 删除指定的会话

## FZF
- J       : MRU 
- \<C-t\>       : BTags
- L       ：LinesWithPereview
- B       : Buffers
- H       : History
- \<C-p\> : FZF 
- \<C-f\> : AG

## bookmark
- mm : 设置标签
- mi : 设置标签并定义名称
- ma : 查看所有标签
- mn : 移动到下一个标签位置
- mN : 移动到上一个标签位置
- mc : 清除当前的标签
- mC : 清除所有标签

## undo
\<F7\> : 当前文件的历史修改查看

## Code navigation
T : 代码导航
\<Leader\>n : 使用ranger的形式打开文件目录
\\n : 打开目录


## coc.nvim
- gd : 调整到定义位置
- gr
- gy
- ga

## suda.vim
sw : vim下的提权操作

## Focused mode
F9 : 将当前的窗口最大化（在使用分屏的时候很好用）
