# CluadeCodeForRider
##尝试使用在Rider中链接Claude Code使用
###首先从零开始去官网下载CluadeCll终端  
打开浏览器访问 https://nodejs.org/
点击 "LTS" 版本进行下载（推荐长期支持版本）
下载完成后双击 .msi 文件
按照安装向导完成安装，保持默认设置即可
还需要安装Node.js 以及 Git Bash  Nodejs同样去官网下载 安装好后node --version 验证

1）安装 Git for Windows
去这里下载并安装：
https://git-scm.com/downloads/win

2）确认 bash.exe 的位置
通常在这个路径：

3）设置环境变量 CLAUDE_CODE_GIT_BASH_PATH
把它指向你的 bash.exe。

方法 A：临时设置（当前窗口有效）
在 PowerShell 里输入：
$env:CLAUDE_CODE_GIT_BASH_PATH="C:\Program Files\Git\bin\bash.exe"
然后再运行：
cd /d "你的工程文件"  再运行claude
### Cluade工作
首先第一步/init 构建你的Claude.md文件 这里包含你的核心规则以及如何去使用claude <img width="839" height="621" alt="image" src="https://github.com/user-attachments/assets/fe3e5f3b-5db9-42bb-b8bc-7ed84e8c256e" />
第一步init需要等待3-5min后 既可以开始你的任务，
一开始可以比较谨慎的去使用 可以让它先分析你的工程流程以及漏洞缺陷 并给出一份最小化改动以及可落地的方案
<img width="798" height="416" alt="image" src="https://github.com/user-attachments/assets/23b819f2-87c2-4a0c-8cda-cc2643833a13" />


###接下来等待claude进行检索分析，完成后一般会给出三个选项供选择，第一个是直接自动执行只做最后验证，第二个是拆分多阶段，按阶段执行并告诉你做了什么修改你二次确认后再继续执行3你不做任何事 他会停在这里

####最后补充一下
常用快捷键解释
! — 进入 bash mode
把当前输入切换成 Shell / Bash 命令模式。
适合直接执行终端命令，比如：
!ls
!git status
!python main.py
/ — 查看或执行命令
用于输入 Claude Code 的内置斜杠命令。
例如可能有：

/help
/clear
/model
/keybindings
@ — 引用文件路径
用于让你快速选择或插入文件路径。
常见用途：

指定某个文件让 AI 读取
把文件加入上下文
例如：

@src/main.py
@D:\Project\xxx\file.txt
& — 后台任务
用于把某些操作放到后台执行。
适合耗时任务，比如：

编译
测试
长时间脚本运行
/btw — side question
意思是插入一个顺带问题，不打断当前主任务的上下文。
比如你正在让它改代码，顺便问一句别的事。

编辑输入相关
double tap esc — 清空输入
连按两次 Esc，通常是快速清空当前输入框。

shift + tab — 自动接受编辑
用于快速接受 AI 给出的编辑建议。
如果它给你展示代码修改，这个键可以一键确认。

backslash (\) + return — 换行
在输入时如果想真正输入换行，而不是直接发送，可以用：

\ + 回车
ctrl + g — 在 $EDITOR 中编辑
把当前输入内容交给你系统默认编辑器编辑。
适合写长提示词、多行内容。

ctrl + s — stash prompt
把当前 prompt 暂存，方便以后继续。
类似“先保存一下草稿”。

任务与输出相关
ctrl + o — verbose output
切换更详细的输出模式。
适合你想看更多过程信息、日志细节时使用。

ctrl + t — toggle tasks
切换任务面板或任务显示状态。
一般用于查看当前进行中的任务。

ctrl + shift + _ — undo
撤销最近的操作。
这里的 _ 实际上通常对应的是 撤销快捷键的组合，不同键盘布局可能有细微差异。

alt + v — paste images
粘贴图片。
如果你从剪贴板复制了截图，可以直接贴进来。

alt + p — switch model
切换模型。
比如在 Haiku / Sonnet 之间切换。

! 可以直接输入终端命令
/ 是 Claude 的功能命令
@ 是文件引用
& 是后台任务
一些快捷键能提升输入、编辑、切换模型的效率
最实用的几个
如果你刚开始用，我建议先记这几个：
!：执行命令
/：看内置命令
@：引用文件
Alt + P：切模型
Ctrl + O：看详细输出
Shift + Tab：接受修改

总结确实好用但是token也太贵了吧😭
<img width="1550" height="597" alt="image" src="https://github.com/user-attachments/assets/1ade7fb6-95ac-45bc-933e-02f54124e3a9" />



