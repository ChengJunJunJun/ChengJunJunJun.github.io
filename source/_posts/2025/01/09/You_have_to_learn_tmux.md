---
title: Tmux的常用命令
date: 2025-01-09
last_modified: 2025-01-19
author: Cheng Jun
desc: Tmux 是一个非常实用的终端复用工具，它可以让你在一个终端窗口中创建多个会话、窗口和面板，并支持会话保持，即使断开 SSH 连接，之前的工作状态也可以恢复。
tags: [tmux, command, terminal]
categories: Technical sharing
---


> 提示：`Ctrl + b` 是 tmux 的默认前缀键，需要先按 `Ctrl + b`，松开后再按其他键。可以修改为其他键，比如 `Ctrl + a`。修改tmux 的配置文件 `~/.tmux.conf` 文件，添加 `set -g prefix C-a` 即可。

#### 基本命令
```bash
tmux new -s <session-name> # 创建一个新的会话
tmux attach -t <session-name> # 连接到已有的会话
tmux ls # 列出所有会话
tmux kill-session -t <session-name> # 关闭指定会话
exit/Ctrl+D # 退出会话
```

#### Tmux 的快捷键以 `Ctrl+b` 为前缀（称为“前缀键”），按下后再输入其他命令。

```bash
Ctrl+b d # 分离会话
Ctrl+b c # 创建新窗口
Ctrl+b n 或 Ctrl+b p 或 Ctrl+b+数字键 # 切换窗口
Ctrl+b " 或 Ctrl+b % # 水平或垂直分割窗口
Ctrl+b q # 显示窗口编号
Ctrl+b t # 显示时间
Ctrl+b I # 强制更新 tmux 配置
Ctrl+b : # 进入命令行模式
```
#### 在 tmux 中关闭分割窗口有几种方法：

1. 最直接的方法是在要关闭的窗格中输入：
```bash
exit
```

2. 使用快捷键（以下任选其一）：
- `Ctrl + b` 然后按 `x` （会提示确认是否关闭）
- `Ctrl + b` 然后按 `&` （关闭整个窗口）

3. 如果在窗格中运行着程序，可以使用 `Ctrl + c` 中断程序，然后再用上述方法关闭窗格

在这里，我放一个麻省理工学院的missing_semester课程的[tmux教程](https://missing-semester-cn.github.io/2020/command-line/)，有兴趣的可以看看。

