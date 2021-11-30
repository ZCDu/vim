# Vim Guidance
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


