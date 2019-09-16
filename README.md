# mac-install

## xcode 开发工具

App Store 搜 xcode 安装, 安装后打开点击 agree 授权

## shadowsocks 翻墙

<http://160.16.231.71/ssx-2.6.3.dmg>

## 搜狗输入法

<https://pinyin.sogou.com/mac/?r=pinyin>

## chrome 浏览器

<https://www.google.com/chrome/browser/desktop/index.html>

## iTerm2 终端

<https://www.iterm2.com/downloads.html>

## homebrew Mac软件源

`cd ~ && mkdir homebrew && curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew`

将 `homebrew/bin` 添加到环境变量

修改为中科大源
```
# 替换brew.git:
cd "$(brew --repo)"
git remote set-url origin https://mirrors.ustc.edu.cn/brew.git

# 替换homebrew-core.git:
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-core.git

brew update
```

homebrew 加速 <http://w3cboy.com/post/2017/03/homebrew-speed-up/>

## zsh 系统shell

`brew install zsh`

oh-my-zsh `sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

编辑配置 `~/.zshrc`, 修改主题为 ys

## tmux 终端窗口工具

`brew install tmux`

编辑配置文件 `vim ~/.tmux.conf`
```
set -g prefix C-a
unbind C-b
set -g mouse on

# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'
set -g @plugin 'tmux-plugins/tmux-resurrect'
set -g @plugin 'tmux-plugins/tmux-yank'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
```

使配置生效 `tmux source-file ~/.tmux.conf`

安装 tmp `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`

安装 yank `git clone https://github.com/tmux-plugins/tmux-yank ~/clone/path`

修改 iTerm2 设置
1. Go into iTerm2's preferences.
2. Go to the "General" tab.
3. Check "Applications in terminal may access clipboard"

进入 tmux, 输入快捷键 prefix + I, 安装插件

## Alfred 快速启动

<http://xclient.info/s/alfred.html?_=baf317d2a9932afca9b32c327f8a34c9>

## vscode 编辑器

<https://code.visualstudio.com/download>

## github desktop GIT客户端

<https://desktop.github.com/>

## Dash 离线文档

<http://xclient.info/s/dash.html?_=baf317d2a9932afca9b32c327f8a34c9>

## nvm node版本管理

`brew install nvm`

添加下列到内容到 .zshrc, 注意替换 xxx 为你实际的路径, `vim ~/.zshrc`
```
export NVM_DIR="$HOME/.nvm"
. "/xxx/bin/homebrew/opt/nvm/nvm.sh"
export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node
```

## node.js

`nvm install x.y.z`

## vim 命令行编辑器

```
syntax on
set showmatch
set nu
set tabstop=4
set noexpandtab
setlocal noswapfile
set bufhidden=hide
set history=100
set hlsearch
set nobackup
set ruler
set rulerformat=%20(%2*%<%f%=\ %m%r\ %3l\ %c\ %p%%%)
set selection=exclusive
set selectmode=mouse,key
set formatoptions=tcrqn
set autoindent
set showcmd
au BufReadPost * if line("'\"") > 0|if line("'\"") <= line("$")|exe("norm '\"")|else|exe "norm $"|endif|endif
colorscheme desert
syntax enable
set tags=tags;
set backspace=indent,eol,start
let g:winManagerWindowLayout='FileExplorer|TagList'
nmap wm :WMToggle<cr>
let Tlist_Show_One_File=1
let Tlist_Exit_OnlyWindow=1
let g:miniBufExplMapCTabSwitchBufs=1
let g:miniBufExplorerMoreThanOne=2
nnoremap <silent> <F3> :Grep<CR>
let Grep_Default_Options='-r --exclude-dir=.svn'
set cscopequickfix=s-,c-,d-,i-,t-,e-
set nocompatible              " be iMproved, required
filetype off                  " required
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
Bundle 'gmarik/Vundle.vim'
Bundle 'a.vim'
Bundle 'taglist.vim'
Bundle 'winmanager'
Bundle 'minibufexpl.vim'
Bundle 'grep.vim'
Bundle 'wolfpython/cscope_map.vim'
call vundle#end()            " required
filetype plugin indent on    " required
```

安装插件工具 `git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim`

安装插件 `vim +PluginInstall +qall`

## Dr. Cleaner Pro 内存/垃圾清理

<http://xclient.info/s/dr-cleaner-pro.html?_=baf317d2a9932afca9b32c327f8a34c9>

## Charles 抓包

<http://xclient.info/s/charles.html?_=baf317d2a9932afca9b32c327f8a34c9>

## MongoDB MAC 客户端

<https://robomongo.org/download>

## SwitchHosts! 管理、切换多个 hosts

<http://xclient.info/s/switchhosts.html?_=3a347412eed8e3045f3b8d948be8a8e6>

## Sketch 

<http://xclient.info/s/sketch.html?_=6e9531566b50dd93cdcfdcf10a1d7c03>

自动导出标注插件: <https://oursketch.com/plugin/sketch-measure>

## 欧路词典 翻译工具

AppStore 下载

## Parallels Desktop 虚拟机, IE调试

<https://xclient.info/s/parallels-desktop.html>

## LICEcap 捕获桌面, 保存GIF

<https://xclient.info/s/licecap.html>

## Royal TSX SSH连接和文件传输

<https://www.royalapplications.com/ts/mac/features>

首先进入设置, 安装 `Terminal` 和 `File Transfer` 插件  
创建 Terminal 任务, 设置名称和服务器ip, 在 Credentials 选项页设置用户名和密码  
创建 File Transfer 任务, 设置名称和服务器ip, 选择 SFTP 协议, 在 Credentials 选项页设置用户名和密码

## zan-proxy 开发代理

<https://youzan.github.io/zan-proxy/>

## Chrome 实用插件

* [Proxy SwitchyOmega](https://chrome.google.com/webstore/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif) 代理管理
* [Adblock Plus](https://chrome.google.com/webstore/detail/adblock-plus/cfhdojbkjhnklbpkdaibdccddilifddb?hl=zh-CN) 广告拦截
* [ModHeader](https://chrome.google.com/webstore/detail/modheader/idgpnmonknjnojddfkpgkljpfnnfcklj) 自定义请求/响应头, 跨域hack
* [JSONView](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc?hl=zh-CN) json浏览美化
* [Postman](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=zh-CN) http请求工具
* [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=zh-CN) React开发工具
* [Redux DevTools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=zh-CN) Redux开发工具
* [RGB转Hex](https://chrome.google.com/webstore/detail/rgb%E8%BD%AChex/pbbmhedhahomalkbcigoejgllbbopofi?hl=zh-CN) 颜色值转换
* [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=zh-CN) 运行自定义脚本
* [User-Agent Switcher for Chrome](https://chrome.google.com/webstore/detail/user-agent-switcher-for-c/djflhoibgkdhkhhcedjiklpkjnoahfmg?hl=zh-CN) 修改UA
* [Vue.js devtools](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=zh-CN) Vue开发工具
* [二维码生成器](https://chrome.google.com/webstore/detail/quick-qr-code-generator/afpbjjgbdimpioenaedcjgkaigggcdpp) 生成当前页面二维码
* [开发常用工具(Develop Tools)](https://chrome.google.com/webstore/detail/%E5%BC%80%E5%8F%91%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7develop-tools/fmmbocgmijhikfppllmnamafcphnelgn?hl=zh-CN) 常用工具集
* [Google 翻译](https://chrome.google.com/webstore/detail/google-translate/aapbdbdomjkkjkaonfhkkikfgjllcleb)
* [Separate Window](https://chrome.google.com/webstore/detail/separate-window/cbgkkbaghihhnaeabfcmmglhnfkfnpon) 视频小窗口播放
