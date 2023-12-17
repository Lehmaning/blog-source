---
date: 2023-12-17
title: fish shell 的一些注意事项
tags:
- fish
- shell
- tips
authors:
- lain
---
以下内容适用于 fish 3.6.4 版本。

## 集成工具
集成 `starship` 、`zoxide`、`carapace`、`nvm` 等工具时，不建议直接写在 `~/.config/fish/config.fish` 下，要用到模块化的思想！

按习惯，我会在 `~/.config/fish/conf.d` 下创建 `starship.fish`、`zoxide.fish` 等文件，并将各自的配置生成命令和 source 命令写在各自的 fish 脚本文件里面。

## functions 文件夹
fish 中的 function 相当于 POSIX 标准下 shell 的 alias，而     `~/.config/fish/functions` 是 fish 用于存放自动加载的 function 脚本文件。

即便该目录下的文件是空文件，fish 也会创建和文件名同名的 function，所以<u>请勿在 `~/.config/fish/functions` 下面创建和 fish 内置命令同名的文件。</u>
