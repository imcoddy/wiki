Screen 常用命令,

Ctrl-a S 新建水平分割窗口
Ctrl-a Tab 切换窗口
Ctrl-a :screen bash 新建 screen 终端，并运行 bash
Ctrl-a :quit 退出 screen，将关闭所有 screen 终端，结束其中所有任务




Ctrl-a c 新建 bash screen 终端
Ctrl-a " 列出
Ctrl-a A 重命名
Ctrl-a n 在当前窗口中切换到下一个 screen 终端
Ctrl-a p 在当前窗口中切换到上一个 screen 终端   

Ctrl-a d 断开所有 screen 终端，返回 screen 执行前状态，但 screen 内所有终端的任务都在执行
screen -ls 列出当前用户的所有 screen 实例，包括联接和断开的
screen -R <pid> 重新联接到已断开的 screen 实例，如果有多个已断开的 screen 实例，则用 <pid> 区分

Ctrl-a S 新建水平分割窗口
Ctrl-a Tab 切换窗口
Ctrl-a X 关闭当前窗口
Ctrl-a + 扩大当前窗口，默认增加3行
Ctrl-a - 缩小当前窗口，默认减小3行

Ctrl-a :screen <command>    新建 screen 终端，并运行命令<command>
Ctrl-a :resize <height> 改变当前窗口高度为<height>
Ctrl-a :quit 退出 screen，将关闭所有 screen 终端，结束其中所有任务

Ctrl-a <Esc>     进入选择模式
<PageUp> 或 Ctrl-u 光标上移一页
<PageDown> 或 Ctrl-d    光标下移一页    
<Left> 或 h  光标左移一格
<Down> 或 j 光标下移一行
<Up> 或 k 光标上移一行
<Right> 或 l     光标右移一格
<Space> 选择开始，选择结束
<Esc> 退出选择模式

Ctrl-a ] 粘贴选择的内容
