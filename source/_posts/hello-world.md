---
title: hello world #【必需】页面标题
date: 2025-05-01 00:13:55
updated: #【可选】页面更新日期
tags: hello world
categories: 生活
keywords: #【可选】文章关键字
description: #【可选】文章描述
top: # 1 置顶
top_img: #【可选】文章顶部图片
comments: #【可选】显示文章评论模块(默认 true)
cover: https://cdn-fusion.imgcdn.store/i/2025/XNSDRF75LbzanYVG.jpg #【可选】文章缩略图(如果没有设置 top_img,文章页顶部将显示缩略图，可设为 false/图片地址/留空)
toc: #【可选】显示文章 TOC(默认为设置中 toc 的 enable 配置)
toc_number: #【可选】显示 toc_number(默认为设置中 toc 的 number 配置)
toc_style_simple: #【可选】显示 toc 简洁模式
copyright: #【可选】显示文章版权模块(默认为设置中 post_copyright 的 enable 配置)
copyright_author: #【可选】文章版权模块的文章作者
copyright_author_href: #【可选】文章版权模块的文章作者链接
copyright_url: #【可选】文章版权模块的文章作者链接
copyright_info: #【可选】文章版权模块的版权声明文字
mathjax: #【可选】显示 mathjax(当设置 mathjax 的 per_page: false 时，才需要配置，默认 false)
katex: #【可选】显示 katex(当设置 katex 的 per_page: false 时，才需要配置，默认 false)
aplayer: #【可选】在需要的页面加载 aplayer 的 js 和 css,请参考文章下面的音乐 配置
highlight_shrink: #【可选】配置代码框是否展开(true/false)(默认为设置中 highlight_shrink 的配置)
aside: #【可选】显示侧边栏 (默认 true)
swiper_index: 10 #【可选】首页轮播图配置 index 索引，数字越小越靠前
top_group_index: 10 #【可选】首页右侧卡片组配置, 数字越小越靠前
ai: #【可选】文章ai摘要
background: "#fff" #【可选】文章主色，必须是16进制颜色且有6位，不可缩减，例如#ffffff 不可写成#fff
---
#### 新建博文
```
hexo new 这是一篇新的博文
```
#### 新建标签页
```
hexo new page 新建的标签页
```
#### 更新追番
```
hexo bangumi -u 
```
#### 部署网页 
```
hexo cl; hexo g; hexo d
```
#### 本地预览
```
hexo cl; hexo s
```


## 更换电脑后继续编辑 
如果你只是想在新电脑上继续编辑原有源代码，核心操作其实很简单，重点在**代码同步**和**基础环境复用**，无需复杂的VS Code设置同步流程。以下是更简化的步骤：  


### 一、**前提：代码已托管在GitHub**  
如果原电脑的代码已推送到GitHub仓库，新电脑只需：  
1. **克隆仓库到本地**：  
   在新电脑打开终端，进入目标文件夹，输入命令（以GitHub仓库为例）：  
``` 
git clone https://github.com/你的用户名/仓库名.git  
```  
2. **用VS Code打开项目**：  
   在VS Code中点击左上角「文件」→「打开文件夹」，选择刚克隆的仓库目录，即可直接编辑代码。  


### 二、**若代码未托管：手动迁移代码**  
如果代码在原电脑本地（未上传GitHub），需先拷贝到新电脑：  
1. **备份代码**：  
   将原电脑中项目文件夹复制到U盘、移动硬盘或云盘（如百度云、OneDrive）。  
2. **在新电脑导入**：  
   将备份的项目文件夹复制到新电脑，用VS Code直接打开文件夹即可编辑。  


### 三、**恢复基础编辑环境（可选）**  
如果希望VS Code的扩展、主题等和原电脑一致，可简化操作：  
1. **安装常用扩展**：  
   比如Markdown编辑、Git工具等，直接在VS Code扩展市场搜索安装（例如搜索“Markdown All in One”“GitLens”）。  
2. **复用主题和设置**：  
   - 主题：在VS Code中按`Ctrl+K Ctrl+T`，选择原电脑使用的主题（如默认主题或第三方主题）。  
   - 快捷键/字体等设置：若记得具体配置，可在新电脑的`设置（Ctrl+,）`中手动调整，或从原电脑复制`settings.json`文件到新电脑（路径见下方）：  
     - Windows：`%APPDATA%\Code\User\settings.json`  
     - macOS：`~/.config/Code/User/settings.json`  


### 四、**关键提醒：避免重复操作**  
- **无需同步全部VS Code设置**：若仅编辑代码，扩展和主题可按需安装，不必强求100%一致。  
- **优先保障代码可访问**：只要代码在GitHub或已拷贝到新电脑，用VS Code打开即可编辑，其他环境配置可逐步补充。  


总结：**核心操作就是克隆/复制代码到新电脑，用VS Code打开即可编辑**。环境配置（扩展、主题等）属于优化项，可根据需要逐步恢复，无需一开始就追求完整同步。