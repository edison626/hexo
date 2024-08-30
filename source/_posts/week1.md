---
title: 网络安全C10-2024.8.10
swiper_index: 10
top_group_index: 10
background: '#fff'
date: 2024-08-30 14:47:08
updated:
tags: 网络安全C10-2024.8.10
categories: 网络安全C10-2024.8.10
keywords:
description:
top:
top_img:
comments:
cover:
toc:
toc_number:
toc_style_simple:
copyright:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
mathjax:
katex:
aplayer:
highlight_shrink:
aside:
ai:
---

## 网络安全C10-2024.8.10

### 使用html写一个网页，要求满足以下条件：

（1）网页标题：网络安全C10期课程

（2）网页背景颜色：蓝色

（3）网页中含有一个超链接，点击即可跳转至百度

（4）如果在网页中不做任何操作，5秒后跳转至马哥教育官网

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="refresh" content="5;url=https://www.magedu.com/">
    <title>网络安全C10期课程</title>
    <style>
        body {
            background-color: blue;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 20%;
        }
        a {
            color: yellow;
            text-decoration: none;
            font-size: 20px;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <h1>欢迎来到网络安全C10期课程</h1>
    <p>点击以下链接跳转到百度：</p>
    <p><a href="https://www.baidu.com/" target="_blank">百度</a></p>
</body>
</html>
```

