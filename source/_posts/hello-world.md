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
#### hexo new 这是一篇新的博文
#### hexo new page 新建的标签页
#### 更新追番
> hexo bangumi -u 

要在 SSH 下部署服务器，一般步骤如下（以 Linux 服务器为例）：

---

### 一、连接到服务器

```bash
ssh username@your_server_ip
```

例如：

```bash
ssh root@192.168.1.100
```

---

### 二、更新系统

```bash
sudo apt update && sudo apt upgrade -y    # Ubuntu/Debian 系
# 或
sudo yum update -y                        # CentOS/RHEL 系
```

---

### 三、安装必要的软件（以部署网站为例）

#### 安装 Nginx（或 Apache）

```bash
sudo apt install nginx -y
```

#### 安装 Node.js（举例）

```bash
sudo apt install nodejs npm -y
```

#### 安装 Git

```bash
sudo apt install git -y
```

---

### 四、部署项目

1. **拉取代码**：

   ```bash
   git clone https://github.com/yourusername/yourproject.git
   cd yourproject
   ```

2. **安装依赖并构建**（如使用 Node.js）：

   ```bash
   npm install
   npm run build    # 如果是 React/Vue 项目
   ```

3. **启动服务**：

   ```bash
   npm start        # 或使用 pm2 更稳妥
   ```

---

### 五、配置 Nginx（反向代理）

编辑配置文件：

```bash
sudo nano /etc/nginx/sites-available/default
```

示例配置：

```nginx
server {
    listen 80;
    server_name yourdomain.com;

    location / {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
```

然后重启 Nginx：

```bash
sudo systemctl restart nginx
```

---

### 六、设置防火墙（可选）

```bash
sudo ufw allow 'Nginx Full'
```

---

你想部署哪种类型的服务器（比如 Web 服务、API、数据库、应用等）？我可以给出更具体的配置。