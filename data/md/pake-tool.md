---
title: 发现一个好用的打包工具
description: 一个把任何网页打包成桌面程序的开源程序
date: '2024-09-17T07:47:43.945Z'
---
## 用 Pake 打包了个极简 Twitter

#### Categories: Creation 2022-11-05

## 介绍 Pake

![](https://cdn.fliggy.com/upic/KgRONl.jpg?x-oss-process=image/resize,w_3600/format,webp)

**开源地址：[https://github.com/tw93/Pake](https://github.com/tw93/Pake)**

一个很简单的用 Rust 打包网页生成很小的 Mac App 工具，底层使用 Tauri，当前支持微信读书、Twitter、语雀、RunCode、Witeboard、Flomo、Vercel 等。技术含量其实不高，只是 Rust 替代之前套壳网页老的思路玩法的一个尝试，新瓶装旧酒，其实 PWA / Electron 也很好用很方便的。

Pake 比较特别的是，相比传统的 Electron 套壳打包，大小要小将近 40 倍，一般 2M 左右，此外由于底层使用的，Rust Tauri 框架，性能体验较 JS 框架要轻快不少，内存小很多；此外实现了通用快捷键的透传、容器通信、样式改写注入、沉浸式的窗口、拖动、简化使用流程优化等功能，有一点点可玩性，你可以 Fork 自己打包喜欢的。

![](https://cdn.fliggy.com/upic/U1VYEV.jpg?x-oss-process=image/resize,w_3600/format,webp)

这里主要介绍最近折腾的「用 Pake 打包了一个极简版的 Twitter Mac 客户端」。

## 极简 Twitter

使用 Pake 结合开源 thomaswang/minimal-twitter 的样式注入改写，花了大概 1 小时打包了一个你可能会喜欢的极简 Twitter 版本，依旧只有 2M 左右，相比官方的看起来舒服很多，将乱七八糟的东西都干掉了，优化不少强迫症体验，效果如下。

### 首页

![](https://cdn.fliggy.com/upic/JKQcHf.png?x-oss-process=image/resize,w_3600/format,webp)

### 详情页

![](https://cdn.fliggy.com/upic/SET1Cf.png?x-oss-process=image/resize,w_3600/format,webp)

### 个人主页

![](https://cdn.fliggy.com/upic/eklvBB.png?x-oss-process=image/resize,w_3600/format,webp)

### 推文

![](https://cdn.fliggy.com/upic/eTOf07.png?x-oss-process=image/resize,w_3600/format,webp)

## 打包汇总

<table><tbody><tr><td>WeRead</td><td>Twitter</td></tr><tr><td><img src="https://cdn.fliggy.com/upic/ffUmdj.png?x-oss-process=image/resize,w_3600/format,webp" width="600"></td><td><img src="https://cdn.fliggy.com/upic/L4HNQ6.png?x-oss-process=image/resize,w_3600/format,webp" width="600"></td></tr><tr><td>RunCode</td><td>Witeboard</td></tr><tr><td><img src="https://gw.alipayobjects.com/zos/k/qc/SCR-20221018-fmj.png?x-oss-process=image/resize,w_3600/format,webp" width="600"></td><td><img src="https://cdn.fliggy.com/upic/o5QY4c.png?x-oss-process=image/resize,w_3600/format,webp" width="600"></td></tr><tr><td>Flomo</td><td>语雀</td></tr><tr><td><img src="https://cdn.fliggy.com/upic/B49SAc.png?x-oss-process=image/resize,w_3600/format,webp" width="600"></td><td><img src="https://cdn.fliggy.com/upic/mv9dvj.png?x-oss-process=image/resize,w_3600/format,webp" width="600"></td></tr></tbody></table>

## 最后

其实 Pake 属于我一个无心插柳的小项目，当时使用微信读书的时候习惯用 Mac 来看，发现只有网页版本，就自己打包了一个，后面有不少人来问怎么搞的，就将代码放到 Github 上面去了，其实代码很简单，不过用 Rust 打包这个思路还比较新，包括后面还有不少贡献者参与进来一起 [建设](https://github.com/tw93/Pake/issues/39)，想着做完善些，做到相比 [国外收费的 Electron 打包页面的工具](https://www.google.com/search?q=Turn+any+webpage+into+a+real+Mac+App&newwindow=1&sxsrf=ALiCzsaRyaZYGi04wFCtU6HTi72nQnxGCg%3A1667610724145&ei=ZLhlY9XKCMHdkPIPs9G4qAE&ved=0ahUKEwjVjNiG7pX7AhXBLkQIHbMoDhUQ4dUDCBA&uact=5&oq=Turn+any+webpage+into+a+real+Mac+App&gs_lp=Egxnd3Mtd2l6LXNlcnC4AQP4AQL4AQFI7AFQAFgAcAB4AcgBAJABAJgBAKABAKoBAOIDBCBNGAHiAwQgQRgA4gMEIEYYAIgGAQ&sclient=gws-wiz-serp) 好用些，满足一波爱好者喜欢就够了。
