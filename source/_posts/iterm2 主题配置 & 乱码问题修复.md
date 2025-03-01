---
title: Iterm2 主题配置 & 乱码问题修复
data: 2025/3/1 17:05
categories: 🔧 开发工具
tags: iterm2
---

## iterm2 主题修改
1、查看 zshrc 配置文件，并找到 `ZSH_THEME` 配置
```bash
cat -n .zshrc | grep ZSH_THEME
12	ZSH_THEME="agnoster"
15	# Setting this variable when ZSH_THEME=random will cause zsh to load
18	# ZSH_THEME_RANDOM_CANDIDATES=( "robbyrussell" "agnoster" )
```

2、在 ohmyzsh themes 找到你想要修改的主题，将 ZSH_THEME 改为你想要的主题， eg: ZSH_THEME="agnoster"

## 乱码问题
在修改主题后可能出现乱码的问题，修复步骤如下：

1、下载字体
```bash
# 你本机的某个目录
cd ~/code && git clone https://github.com/powerline/fonts.git

cd fonts && ./install.sh

cd && rm -rf ~/code/fonts
```
2、修改 iterm 字体配置

Iterm2的设置路径是: [iTerm2] -> [Profiles] -> [Default] -> [Text] -> [Font] -> [DejaVu Sans Mono for Powerline]



## 参考

- iterm2 下载地址：https://iterm2.com/
- themes: https://github.com/ohmyzsh/ohmyzsh/wiki/themes
