​	微信公众号里面的内容对搜索引擎不太友好，由于它的`robots.txt`限制，所有的搜索引擎都无法在外面检索到公众号里面的内容(_注:后来发现搜狗搜索引擎可以检索微信公众号的内容，但是这个意义不大，平常用的人实在太少_)，因此不太利于技术知识的传播，为了提升自己的一些文章在互联网的曝光度，决定再基于`github pages`来搭建一个blog。

​	搭建教程网上已经有很多，因此实在没必要再单独写一遍，所以我这篇文章主要记录一下搭建过程中遇到的一些问题以及使用感受。

#### 一、一些背景

##### 1、github pages是什么

​	官方网站的说明:“Hosted directly from your GitHub repository. Just edit, push, and your changes are live.”简单来说，GitHub Pages是github基于github的仓库提供的一项服务，可以用于存放静态网页，包括博客、项目文档甚至整本书。一般GitHub Pages的网站使用github.io的子域名，但是也可以使用第三方域名。

##### 2、jekyll是什么

​	`jekyll`是一个静态网页生成框架，如果不使用这个框架的话，你仍然可以使用github pages来写博客，但是很多东西需要手动管理，例如排版布局、目录等等，为了简化这些操作，一般会使用工具来管理。

​	除了`jekyll`之外，还有一些例如 `hexo`、`hugo`之类的静态网页框架等，各有利弊，大家可以网上自行查阅，不再赘述。我也使用了`jekyll`来做管理，因为我的主要目的是为了简单高效地写作，所以对工具暂时没有特别多的诉求。

##### 3、搭建教程

​	参考官方地址: https://docs.github.com/cn/pages ，有中文版本，写得非常清楚。跟着教程step-by-step即可。同时这个官方教程里面还提供了关于`jekyll`的使用说明。



#### 二、搭建之后的问题

​	这些问题主要是基于`jekyll`工具来引发的，如果使用的不是这个工具，不需要再往下看了。

##### 1、google analytics 配置

jekyll默认情况下，没有办法查看自己博客的访问量，用户分布等，因此需要借助 `google analytics` 来完成。google analytics的注册和配置方式这里就不重复了，自行google即可，`google analytics`的配置方式跟当前使用的theme是有关系的，jekyll默认情况下使用的是 `minima` 这个theme。这种在github开源的theme，都会写明google analytics的配置方式。

去github找到这个主题的地址，然后按照教程配置即可，例如minima的google analytics配置方式地址: https://github.com/jekyll/minima#enabling-google-analytics

##### 2、更换主题

使用jekyll theme 关键字去github搜索，查看各个仓库的 `readme.md` ，按需配置即可。

##### 3、本地调试问题

按照官方教程安装jekyll之后，它里面写的是使用`bundle exec jekyll serve`命令来启动本地调试，某些情况下可能会遇到错误提示，提示说“cannot load such file --webrick”，如下图所示

<img src="https://raw.githubusercontent.com/beiyu/beiyu.github.io/main/imgs/image-20220623230348972.png">1</img>



解决办法:

在你的博客目录执行 `bundle add webrick` 即可解决

参考官方issue: https://github.com/jekyll/jekyll/issues/8523

##### 4、本地以生产环境模式启动

某些时候，在本地调试模式启动之后，某些逻辑不会生效，可以设置环境环境，让其以生产环境模式运行，如下所示

`JEKYLL_ENV=production bundle exec jekyll serve`

##### 5、图片问题

一般的markdown里面，直接使用相对路径即可引用图片，但是在jekyll里面会存在一些问题，导致无法正常显示。我暂时没找到比较优雅的解决方案，所以暂时直接把图片先传到github仓库，然后markdown里面直接使用 https开头的绝对路径。



### 三、最后

​	适当的多写一些文章到公开的地方，可以为互联网贡献一些自己的知识经验，也有利于逐步的扩大自己的个人IP知名度。
