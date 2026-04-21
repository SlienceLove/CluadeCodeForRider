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


