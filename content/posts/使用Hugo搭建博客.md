+++
title = '使用Hugo搭建博客'
date = 2024-01-19T18:59:21+08:00
draft = false

+++
### 一、关于博客的技术选型
博客有很多种技术方案，对于我来说，主要有两个需求：
- 以文本形式保存内容，数据可以随时迁移和备份，所以优先考虑markdown源文件的形式，pass掉了WordPress和ghost这些方案。
- 以写作体验优先，需求比较纯粹，尽量降低成本不要self-host。

结合这两个需求，就选择了`github pages + hugo`的方案

### 二、操作流程
花了一些时间先看一遍官方文档，整体还是比较清晰的，一共分两步：
#### 1、用Hugo在本地创建一个项目
参考 [https://gohugo.io/getting-started/quick-start/](https://gohugo.io/getting-started/quick-start/)
- 安装Hugo
- 初始化项目
- 设置一个主题，修改一些基本配置

#### 2、配置github的actions
参考 [https://gohugo.io/hosting-and-deployment/hosting-on-github/](https://gohugo.io/hosting-and-deployment/hosting-on-github/)

- 在github创建一个特殊命名的仓库
- 配置github的actions
- 提交本地仓库，触发build

### 三、结尾
整个过程非常简单，之所以选择了hugo，也是因为我比较喜欢go语言的设计理念。
先这样吧，等以后有了什么问题或者其他新发现，我也许会来更新这篇文章。