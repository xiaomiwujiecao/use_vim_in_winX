## `Vim` 超专业版快捷键


!> 注意：此专业版快捷键在各系统平台大部分通用，可能部分不能使用。

!> 下面的中括号表示可替代的文本，例如` [cmd]` 代表可替换的命令行，

!> ` [file]` 指的是可替换的文件名称。也可表示缩写。

### 启动 `Vim` 开始编辑或新建文件

- `vim -c [cmd] [file]` ：执行指定的命令在打开文件之前
- `vim -r [file]` ：打开文件时，回复上次异常退出的文件
- `vim -R [file]` ：以只读的方式打开文件，但可以强制保存文件
- `vim -M [file]` ：以只读的方式打开文件，但是不可以强制保存
- `vim + [file]` ：以文件的末尾开始编辑文件
- `vim + [num] [file]` ：从第 num 行开始编辑文件
- `vim +/[string] [file]` ： 从匹配到指定字符串行开始编辑文件
- `vim --remoote [file]` ：用已有的 `vim` 进程打开指定的文件 

### 文件文档操作 命令模式下
#### 编辑
- `:e [file]` ：关闭当前编辑的文件，并开启新的文件
- `:e! [file]` ：放弃对当前文件的更改，编辑新的文件
- `e + [file]`：开始新的文件，并从文件尾开始编辑
- `:e +n [file]` : 开始新的文件，从第 n 行开始编辑
- `:enew` ：编辑一个未命名的新文档
- `:e` ：重新加载当前文档
- `:e!` ：重新加载当前文档，并丢弃已做的改动
- `:e#` 或 `ctrl+^`：回到刚才编辑的文件
#### 文件
- `:f` 或 `ctrl+g` ：显示文档名称、是否修改、光标位置
- `:f [filename]` ： 改变编辑的文件名,未编辑版本，如果保存，那么使用刚才的文件将另存为文件
- `gf` ： 打开以光标所在字符串为文件名的文件
- `:w`： 保存修改
- `:wq` ：保存并退出
- `ZZ` ：保存并退出
- `:q` ：退出，如果对缓存区进行修改，则会提示
- `:q!` ：强制退出，放弃修改
- `:x` ：保存并退出
- `:saveas` [newfilename]： 另存为新文件名
- `browse e` ：打开一个文件浏览器让你选择要编辑的文件
- `:set browsedir=last` ：用上次访问过的目录
- `:set browsedir=buffer` ：用当前工作目录
- `:set browsedir=current` ：用当前工作目录
- `:Sex` ：水平分割一个窗口，浏览文件系统
- `:Vex` ：垂直分割一个窗口，浏览文件系统

### `Vim` 移动光标

- `h` ：上
- `j` ：下
- `k` ：左
- `l` ：右
- `ctrl-e` ：向下移动一行
- `ctrl-d` ：下翻半页
- `ctrl-u` ：上翻半页
- `ctrl-f` ：往上翻动一页
- `ctrl-b` ：往下翻动一页
- `ctrl-y` ：往上滚动一行
- `w` 跳转到下一个字首,根据点或单词分割
- `W` 跳转到下一个字首，长跳
- `e` 跳转自下一个字尾
- `E` 跳转到下一个字尾，长跳
- `b` 跳转上一个字
- `B` 跳到上一个字，长跳
- `0` （数字0） 跳转至行首
- `^` 跳转至行首的第一个字符
- `$` 跳至行尾
- `gg` 跳至文首
- `G` 跳至文尾
- `5gg` 或 `5G` 调制第五行
- `gd` 调至当前光标所在的变量的声明处
- `fx` 查找字符 x ，如果找到，就跳转过去
- `;` 重复上一个 f 命令， 而不用重复输入 fx
- `* `查找光标所在的单词，向下查找
- `#` 查找光标所在的单词，向上查找
- `zz` 将当前行移动到屏幕中央
- `zt` 将当前行移动到屏幕顶端
- `zb` 将当前行移动到屏幕底端

### 编辑模式

- `i` 从当前光标处进入输入模式
- `Esc`(按键) 退出输入模式
- `I` 进入输入模式，并置光标于行首
- `a` 追加模式，置光标于当前光标之后
- `A` 追加模式，置光标于行末
- `gl` 在当前行第一列插入
- `o` 在当前行的下一行新加一行，并进入输入模式
- `O` 在当前行的上一行新加一行，并进入输入模式
- `c[n]w` 改写光标后1(n)个词
- `c[n]l` 改写光标后(n)个词
- `c[n]h` 改写光标前n个字母
- `[n]cc` 修改当前[n] 行
- `dd` 删除光标所在行
- `dw` 删除一个字
- `d` 或 `Y` 复制到行末
- `[n]x` 剪切光标右边n个字符
- `y` 复制在可视模式下选中的文本
- `yy` 或 `Y` 复制整行文本
- `y[n]w` 复制一[n]个词
- `y[n]l` 复制光标右边1(n)个字符
- `y[n]h `复制光标左边1(n)个字符
- `y$` 从光标当前位置复制到行尾
- `y0` 从当前位置复制到行首
- `:m,ny<cr>` 复制m 行到 n 行的内容
- `:y1G` 或 `ygg` 复制光标以上所有行
- `yG` 复制光标以下所有行
- `yaw` 和 `yas`  复制一个词和复制一个句子
- `d` 删除（剪切）在可视模式下选中的文本
- `d$` 或 `D` 删除(剪切) 当前位置到行尾的内容
- `d[n]w` 删除(剪切) 1(n) 个单词
- `d[n]l` 删除(剪切) 右边1(n) 个字符
- `d[n]h` 删除(剪切) 左边1(n) 个字符
- `d0` 删除（剪切）当前位置到行首的内容
- `[n] dd` 删除(剪切) 1(n) 行
- `d1G` 或 `dgg` 剪切光标以上所有行
- `dG` 剪切光标以下所有行
- `daw` 或 `das` 剪切一个词和剪切一个句子
- `d`或 `f<cr>` 删除当前位置 到下一个f之间的内容
- `p` 粘贴剪切板的内容到当前行的下面
- `P` 黏贴剪切板的内容到当前行的上面
- 
- ### 查找与替换 命令模式下

- `/pattern`：  向后搜索字符串pattern 
- `?pattern` ： 向前搜索字符串pattern 
- "\c" ： 忽略大小写
- "\C" ： 大小写敏感
- `n` ： 下一个匹配项
- `N` ： 上一个匹配项
- `:s/one/two` ： 将当前光标所在行的第一个 `one` 替换成 `two`
- `:s/one/two/g`：  将当前光标所在行所有 `one` 替换成 `two`
- `:%s/one/two/g`：  将全文中的所有 one 替换成 two


### 排版

- `<<` ：向左缩进一个 `shiftwidth`
- `>>` ：向右缩进一个 `shiftwidth`
- `:ce(nter)` ：本行文字居中
- `:le(ft)` ：本行文本靠左
- `:ri(ght)` ：本行文字靠右
- `gq` ：对选中的文字重排，对过长的文本进行断行
- `gqq` ：重排当前行
- `gqnq` ：重排 n 行 
- `gqnap` ：重排当前段
- `gqnj` ：重排当前行和下面n行
- `gqQ` ：重排当前段对文章末尾
- `J` 拼接当前行和下一行
- `:set spell` ：- 开启拼写检查功能
- `:set nospell` ：-关闭拼写检查功能
- `]s` ：移动下一个拼写错误的单词
- `[s` ：作用域上一命令类似，但它是从相反方向进行搜索
- `z=` ：-显示一个有关拼写单词的列表，可从中选择
- `zg` ：-告诉拼写检查器该单词是拼写正确的
- `set nu` ：显示行号
- `set nonu`： 不显示行号

### 编辑

- `J` ：将下一行和当前行连接为一行
- `cc` ：删除当前行并进入编辑模式
- `cw` ：删除当前字并进入编辑模式
- `c$` ：擦除当从当前位置到行末的内容 ，并进入编辑模式
- `s` ：删除当前字符并进入编辑模式
- `S` ：删除光标所在行并进入编辑模式
- `xp`： 交换当前字符和下一个字符
- `u` ：撤销
- `ctrl+r`： 重做 
- `~` ：对当前字符切换大小写
- `>>` ：对当前行右移一个单位
- `<<` ：将当前行左移一个单位(一个 `tab` 符)
- `== `：自动缩进当前行


### 多文本编辑

- `vim file1...` ：同时打开多个文件
- `:args` ：显示当前编辑文件
- `:next` ：切换到下一个文件
- `:prev` ：切换到前个文件
- `:next!` ：不保存当前编辑文件并切换到下个文件
- `:prev!` ：不保存当前编辑文件并切换到上个文件
- `:wnext` ：保存当前编辑文件并切换到下个文件
- `:wprev` ：保存当前编辑文件并切换到上个文件
- `:first` ：定位首文件
- `:last`： 定位尾文件
- `:close` ：关闭当前窗口
- `ctrl+^` ：快速在最近打开的两个文件之间切换
- `:split[sp]` ：把当前文件水平分割
- `:new file` ：同 split file
- `:split file` ：把当前窗口水平分割,file
- `:all` ：打开所有的窗口
- `:vsplit[vsp] [file]`： 把当前窗口垂直分割， file
- `:only`： 只显示当前窗口，光比所有其他的窗口
- `:vertical al`l ：打开所有的窗口。垂直打开
- `:qall` ：对所有窗口执行: q 操作
- `:qall` ：对所有窗口执行: q! 操作
- `:wall` ：对所有窗口执行 : w 操作
- `:wqall` ：对所有窗口执行 : wq 操作
- `ctrl-w h` ：跳转至左边的窗口
- `ctrl-w l` ：跳转至右边的窗口
- `ctrl-w k` ：跳转至上边的窗口
- `ctrl-w l` ：跳转至下边的窗口
- `ctrl-w t` ：跳转至最顶上的窗口
- `ctrl-w b` ：跳转至最顶下的窗口

### 多标签编辑

- `:tabedit file` ：在新标签中打开编辑文件
- `:tab split file`： 在新标签中打开文件
- `:tabp` ：切换至前一个标签
- `:tabn` ：切换至后一个标签
- `:tabc` ：关闭当前标签
- `:tabo `：关闭其他标签
- `:gt`： 到下一个tab
- `:gT` ：到上一个tab
- `:0gt` ：跳转到第一个tab
- `:5gt` ：跳转至第五个tab

### 调整窗口大小

- `ctrl-w + `  ：当前窗口增高一行
- `ctrl-w - `  ：当前窗口减小一行
- `ctrl-w _ `  ：当前窗口拓展到尽可能大
- `:resize n ` ：当前窗口n行高
- `:ctrl+w =`  ：所有窗口同样高度
- `n ctrl+w _` ：当前窗口的高度设定为 n 行
- `ctrl+w < `  ：当前窗口减少一列
- `ctrl+w > `  ：当前窗口增宽一列
- `ctrl+w |`   ：当前窗口尽可能的宽

### 切换和移动窗口

- - `ctrl+w ctrl+w` ：或者  `ctrl+w w`  切换到下一个窗口 
- - `ctrl+W p` ：切换到前一个窗口
- - `ctrl+w h(l,j,k)` ： 切换到左，（右，下，上）的窗口
- - `ctrl+w t(b)` ：切换到嘴上（下）面的窗口
- - `ctrl+w H(L,K,J)` ：当前窗口移动到最左（右，上，下）面
- - `ctrl+w r` ：旋转窗口的位置
- - `ctrl+w T` ：将当前的窗口移动到新的标签页上

### 编辑特殊文件

- `vim -x file`： 开始编辑一个加密的文件
- `:X `为当前文件设置密码
- `:set key=` ：去除文件的密码
- `:set fenc` ：查看当前文件的编码
- `:set fileeencoding` ：查看当前文件的编码
- `:e ++ff=dos [filename] `：让 vim 用 dos 格式打开这个文件
- `:w +ff=mac [filename]` ：以 mac 格式存储这个文件
- `:set ff` ：显示当前文件的格式

### 命令行模式下快捷键

- `ctrl-w`： 向前删除一个单词
- `ctrl-h`： 向前删除一个字符,等同于 `Backspace`
- `ctrl-u`： 从当前位置移动到命令行开头
- `ctrl-b`： 移动到命令行开头
- `ctrl-e`： 移动到命令行末尾

### 命令模式 `shell`

!>  `%` 百分号在 `shell` 执行过程中是代表当前文件名的特殊变量 例如 ：
在 `windows` 中 `dir % `,`{cmd}` 代表您输入的命令。

- `:!{cmd}`          ：运行 `shell` 命令，显示输出，并在返回当前缓冲区之前提示您。
- `:!`             ：单独运行最后一个（来自您的 `shell` 历史记录的）外部命令
- `:!!`            ：重复上一条命令
- `:silent !{cmd}` ： 消除了在命令执行后按回车键的需要
- `:r !{cmd}`      ：将 `$cmd` 的输出写入到当前缓冲区。