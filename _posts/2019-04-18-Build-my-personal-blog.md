---
layout:     post
title:      用 GitHub Pages 快速搭建个人博客
subtitle:	
date:       2019-04-18
author:     Magicalsoso
header-img: img/home-bg-o.jpg
catalog: true
tags:
    - Blog
---

## 前言

今天在清理电脑文件时，不小心把以前记录的学习笔记给清理掉了！！当时那个心疼啊。顿时醒悟想到把自己的学习笔记放到博客上，防止本地误删。于是百度了一下哪个博客好。发现Github可以搭建个人的博客网站，于是果断就选择了使用Github。

我的个人博客是参考[BYQiu](https://www.jianshu.com/p/e68fba58f75c)大神的博客模板来进行搭建修改的，在此特别感谢。

<br>
## 关于GitHub Pages

这是它的官网介绍[GitHub pages](https://pages.github.com)

<br>
## 开始搭建

### 主页效果图 

![V1qGa6.png](https://s2.ax1x.com/2019/06/01/V1qGa6.png)

<br>
### 使用GitHub Pages 建立博客

1、首先你要有一个Github账号

2、然后新建一个仓库，点击右上角的 **+** 新建一个仓库，如下图所示：

![V1qlrR.png](https://s2.ax1x.com/2019/06/01/V1qlrR.png) 

3、接下来克隆我的仓库到你的本地
```shell
git clone https://github.com/Magicalsoso/Magicalsoso.github.io.git
```
4、在本地新建一个文件夹，文件夹命名使用你刚刚新建的仓库名，然后把你刚刚下载的我的仓库里的文件夹，全部复制到你的文件夹目录下。

5、接下来，在你的文件夹下运行命令，使用git把全部内容推送到你新建的远程仓库。

1）初始化一个Git仓库
```
git init
```
2）把文件添加到仓库
```
git add <filename>
```
3）把文件提交到仓库
```
git commit -m "initialization file"
```
4）将本地和远程仓库关联起来
```
git remote add origin <你的远程仓库地址>
```
5）推送内容到远程仓库
```
git push -u origin master
```
等待上传完成，进入你的仓库页面，然后点击environment->View deployment进入你的个人博客。当然,现在看到的都是我的博客的内容, 如果不喜欢这个主题也可以到[Jekyll官网](http://jekyllthemes.org/)找自己喜欢的。

<br>
### 修改仓库内容

博客算是搭建完了, 但要变成自己的内容, 还需要修改代码。

如果不想太多了解代码, 简单一些, 我们只需要改一点点就行。

<br>
#### 网站基本设置

先来看 <code>_config.yml</code> 文件

![V1qQM9.png](https://s2.ax1x.com/2019/06/01/V1qQM9.png)

这里一般都看的懂, 根据自己的来改就行

<br>
#### 社交网络设置

然后就是看着

![V1qnGF.png](https://s2.ax1x.com/2019/06/01/V1qnGF.png)

这里就是你其他的一些社交网络账户了网站与他对的就是下面这张图, 侧边栏也有

![V1qmPU.png](https://s2.ax1x.com/2019/06/01/V1qmPU.png)

没有可以删除或注释掉, 如果有其他的那就写上, 然后打开<code>_includes</code>文件夹下的<code>footer.html</code>文件

![V1q1q1.png](https://s2.ax1x.com/2019/06/01/V1q1q1.png)

找到图上面的代码, 复制图片中的两段中的一段, 粘贴到他们上面或者下面, 按照下图根据据自己情况来改

![V1qu24.png](https://s2.ax1x.com/2019/06/01/V1qu24.png)

然后还有在<code>_layouts</code>目录下的 <code>page.html</code>的 100行左右也按照上面的来修改一下

<br>
#### 博客评论修改
继续来看到_config.yml的这里![V1qze1.png](https://s2.ax1x.com/2019/06/01/V1qze1.png)
这里是你关于博客的评论, 原博主讲的很详细了, 这里就直接引用一下[为博客添加 Gitalk 评论插件](https://www.jianshu.com/p/78c64d07124d)

<br>
#### 其他设置

其他还有就是 <code>_config.yml</code> 的 friends , <code>package.json, manifest</code> 根据自己的来修改还

剩下就是 <code> about.html, index.html, tags.html </code> 的开头部分,更据自己的来改

![V1qKxJ.png](https://s2.ax1x.com/2019/06/01/V1qKxJ.png)

还有就是图片都放在 img 文件夹下 另外你修改一下pwa/icons的图片, 改成自己设计的就行

<br>

#### 添加博客搜索功能

参考[jekyll博客搜索插件](https://github.com/androiddevelop/jekyll-search)

<br>
### 提交更改, 查看效果

修改完代码之后,我们就可以上传了,这里同样使用git命令进行提交。
```
git status
git add filename
git commit -m "message"
git push origin master
```

到此，我们的博客就已经完工了, 可以访问自己博客的地址浏览看一下效果。

最后，因为我们的博客文章是通过Markdown编写的，如果不懂如何使用Markdown格式，建议花个三十分钟看一下：[认识与入门 Markdown](https://sspai.com/post/25137)