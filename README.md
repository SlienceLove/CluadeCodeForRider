# CluadeCodeForRider
##Claude Code使用
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

## 总结确实好用但是token也太贵了吧😭
<img width="1550" height="597" alt="image" src="https://github.com/user-attachments/assets/1ade7fb6-95ac-45bc-933e-02f54124e3a9" />
<img width="1207" height="922" alt="image" src="https://github.com/user-attachments/assets/afa9a8ae-5632-423a-9f6b-2677b0160335" /> 
## 现在好像各大厂商都更推荐使用Cil终端 而不是采用mcp链接方式 有点好奇不过最近在研究RPA或者链接飞书的智能机器人应用 这样就可以手机远程操控ClaudeTeam了 
## 再补充一个skills库 Superpowers,装上后可以使工作流更加标准化，虽然前期看似做了很多的工作，但大大减少了后期返工修bug的工作量，总的来说token花的更有价值

注意它的定位并不是让ai变聪明，实际上大多数人使用ai觉得ai不够强大，都是因为prompt做得不够好，ai没有真正理解需求而出现误差，Superpowers 用 14 个可组合的 Skills 加上强制触发机制，把软件工程的标准流程焊在 AI Agent 上。
### 它的工作原理和大多数人的 AI 编程习惯不一样：
Agent 看到引导指令后，不会直接写代码
先退后一步，询问你真正想做什么
通过对话提炼需求规格，分段展示供你审阅
你审批设计后，生成实施计划
启动子代理逐任务开发，自动代码审查
### 翻译成大白话：
头脑风暴 - 先聊清楚要做什么
Git Worktree 隔离 - 创建独立工作空间
编写计划 - 拆成 2-5 分钟的小任务
子代理开发 - 每个任务派一个独立子代理
测试驱动 - 先写失败测试，再写生产代码
代码审查 - 自动审查代码质量
完成分支 - 验证通过后收尾
#### 铁律一：没有失败测试就不写生产代码
#### 铁律二：不做根因调查就不修 bug
#### 铁律三：没有新鲜验证证据就不做完成声明
#### 安装方式 claudeccode用户 一行命令即可安装 /plugin install superpowers@claude-plugins-official 其他平台（Codex、OpenCode、Gemini CLI、GitHub Copilot CLI）的安装方式可以在项目 README 里找到。六个平台全部支持，这是 Superpowers 相比同类项目的一个优势 - 不绑定单一工具。

#### 总结一下Superpowers 什么时候用，什么时候不必
 适合有一定复杂度的开发任务。改个配置文件、写个简单脚本，用它反而重了。
但涉及多文件改动、需要测试保护、需要代码审查的场景，Superpowers 的价值就出来了。尤其是子代理驱动开发这个机制 - 让每个任务独立执行、独立审查，对复杂项目帮助很大，Skills 是可组合的，不需要每次走完整流程。修 bug 就是个例子 - 只用 3 个 Skills。但要注意强制触发机制：如果存在适用的技能，Agent 会自动使用。想精细控制的话，可以在配置里调整。说实话，这套流程上手会有不习惯 - 毕竟大多数人用 AI 编程图的就是快，但如果是应用在生产项目中建议还是严格按照软件工程的标准工作流进行！



