---
layout: post
title: 通过Jekyll搭建个人博客
date: 2017-01-10 
tags: 博客   
---



### 简介

 　 Jekyll 是一个简单的博客形态的静态站点生产机器。它有一个模版目录，其中包含原始文本格式的文档，通过 Markdown （或者 Textile） 以及 Liquid 转化成一个完整的可发布的静态网站，你可以发布在任何你喜爱的服务器上。Jekyll 也可以运行在 GitHub Page 上，也就是说，你可以使用 GitHub 的服务来搭建你的项目页面、博客或者网站，而且是完全免费的

　  使用 Jekyll 搭建博客之前要确认下本机环境，Git 环境（用于部署到远端）、[Ruby](http://www.ruby-lang.org/en/downloads/) 环境（Jekyll 是基于 Ruby 开发的）、包管理器 [RubyGems](http://rubygems.org/pages/download)        
   
　　如果你是 Mac 用户，你就需要安装 Xcode 和 Command-Line Tools了。下载方式 Preferences → Downloads → Components。

　　Jekyll 是一个免费的简单静态网页生成工具，可以配合第三方服务例如： Disqus（评论）、多说(评论) 以及分享 等等扩展功能，Jekyll 可以直接部署在 Github（国外） 或 Coding（国内） 上，可以绑定自己的域名。[Jekyll中文文档](http://jekyll.bootcss.com/)、[Jekyll英文文档](https://jekyllrb.com/)、[Jekyll主题列表](http://jekyllthemes.org/)。


### Jekyll 环境配置

安装 jekyll

```     
$ gem install jekyll     
```    

创建博客

```    
$ jekyll new myBlog    
```   

进入博客目录

```
$ cd myBlog  
```

启动本地服务

```
$ jekyll serve
```

在浏览器里输入： [http://localhost:4000](http://localhost:4000)，就可以看到你的博客效果了。


so easy !

### 目录结构
　
　  Jekyll 的核心其实是一个文本转换引擎。它的概念其实就是： 你用你最喜欢的标记语言来写文章，可以是 Markdown，也可以是 Textile, 或者就是简单的 HTML, 然后 Jekyll 就会帮你套入一个或一系列的布局中。在整个过程中你可以设置 URL 路径, 你的文本在布局中的显示样式等等。这些都可以通过纯文本编辑来实现，最终生成的静态页面就是你的成品了。

 一个基本的 Jekyll 网站的目录结构一般是像这样的：

```
.
├── _config.yml
├── _includes
|   ├── footer.html
|   └── header.html
├── _layouts
|   ├── default.html
|   ├── post.html
|   └── page.html
├── _posts
|   └── 2017-01-10-welcome-to-jekyll.markdown
├── _sass
|   ├── _base.scss
|   ├── _layout.scss
|   └── _syntax-highlighting.scss
├── about.md
├── css
|   └── main.scss
├── feed.xml
└── index.html

```

这些目录结构以及具体的作用可以参考 [官网文档](http://jekyll.com.cn/docs/structure/) 

进入 _config.yml 里面，修改成你想看到的信息，重新 jekyll server ，刷新浏览器就可以看到你刚刚修改的信息了。

到此，博客初步搭建算是完成了。

### 博客部署到远端 

　  我这里讲的是部署到 Github Page ,创建一个 github 账号，然后创建一个跟你账户名一样的仓库，如我的 github 账户名叫 [swzhang](https://github.com/swzhang)，我的 github 仓库名就叫 [swzhang.github.io](https://github.com/swzhang/swzhang.github.io)，创建好了之后，把刚才建立的 iBlog 项目 push 到 username.github.io仓库里去（username指的是你的github用户名），检查你远端仓库已经跟你本地 iBlog 同步了，然后你在浏览器里输入 username.github.io ，就可以访问你的博客了。


### 编写文章

　　所有的文章都是 _posts 目录下面，文章格式为 mardown 格式，文章文件名可以是 .mardown 或者 .md。


```

---
layout: post
title:  "Welcome to Jekyll!"
date:   2017-01-10 14:35:08 +0800
categories: jekyll-Blog
---

正文...

```


title: 显示的文章名， 如：title: 我的第一篇blog                    
date:  显示的文章发布日期，如：date: 2017-01-10                          
categories: tag标签的分类，如：categories: 随笔            

注意：文章头部格式必须为上面的，.... 就是文章的正文内容。

我写文章使用的是 Sublime Text 3 编辑器，如果你对 markdown 语法不熟悉的话，可以看看[作业部落的教程](https://www.zybuluo.com/) 。











