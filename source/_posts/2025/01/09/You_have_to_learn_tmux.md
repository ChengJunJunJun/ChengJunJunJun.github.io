---
title: Tmux的常用命令
date: 2025-01-09
last_modified: 2025-01-09
author: Cheng Jun
desc: Tmux 是一个非常实用的终端复用工具，它可以让你在一个终端窗口中创建多个会话、窗口和面板，并支持会话保持，即使断开 SSH 连接，之前的工作状态也可以恢复。
tags: [tmux, command, terminal]
categories: Technical sharing
---

#### 基本命令
```bash
tmux new -s <session-name> # 创建一个新的会话
tmux attach -t <session-name> # 连接到已有的会话
tmux ls # 列出所有会话
tmux kill-session -t <session-name> # 关闭指定会话
exit/Ctrl+D # 退出会话
```

#### Tmux 的快捷键以 Ctrl+b 为前缀（称为“前缀键”），按下后再输入其他命令。

```bash
Ctrl+b d # 分离会话
Ctrl+b c # 创建新窗口
Ctrl+b n 或 Ctrl+b p # 切换到下一个或上一个窗口
Ctrl+b " 或 Ctrl+b % # 水平或垂直分割窗口
Ctrl+b q # 显示窗口编号
Ctrl+b t # 显示时间
Ctrl+b I # 强制更新 tmux 配置
Ctrl+b : # 进入命令行模式
```
在这里，我放一个麻省理工学院的missing_semester课程的[tmux教程](https://missing-semester-cn.github.io/2020/command-line/)，有兴趣的可以看看。

