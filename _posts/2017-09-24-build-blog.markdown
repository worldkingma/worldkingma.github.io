---
layout: post
title: Stage of build personal blog
date: 2017-9-24 13:58:51
---


### 准备工作
- ```create```一个```GitHub```仓库(```repository```)并且```clone```到本地,与其建立连接.

- 检查本地是否有```.ssh```目录,并检查目录下是否含有```id_rsa```和```id_rsa_pub```l两个文件.
        
- 如果已经存在就在你的项目目录下运行```git bash```终端.
```
git remote add origin git@github.com:worldkingma/project-name.git
```
把上面以及下面所有用到```worldkingma```改成你自己的
```GitHub```用户名,```project-name```是你本地项目的目录名称.
- 如果没有的话需要手动配置,步骤如下:

- 配置```git```全局属性(与你的```GitHub```相关联)
```
git config --global user.name "worldkingma"
git config --global user.email "worldkingma@gmail.com"
```


- 生成新的```SSH```秘钥
```
ssh-keygen -t rsa -C "worldkingma@gmail.com"
```


> 如果出现光标闪烁,接着连续点击三下回车


```id_rsa```是秘钥,```id_rsa_pub```是公钥

- 拷贝公钥t添加到```GitHub```>```settings```>```SSH and GPK keys```>点击```New SSH key```

- 测试与远程仓库的连接状态

    ```
        ssh -T git@github.com
    ```

出现```Hi, worldkingma! You're successfully authenticated```字样,说明与远程仓库成功建立连接.


- 了解使用[```jekyll```][2]如何建站?.


    - 什么是```jekyll```?
    
     
    介绍```jekyll```之前,先聊聊```GitHub```是什么,它是由```GitHub```官方托管和发布的,你可以使用```GitHub```提供的页面自动生成器,也可以做个人博客，是个轻量级的博客系统，没有麻烦的配置。使用标记语言如Markdown，不需自己搭建服务器，还可以绑定自己的域名。

    [Github Pages - 官方配置指南][3]

    [Github Pages - 自定义页面指南][4]

    [极客学院翻译 - 中文版本指南][5]

    ```GitHub Pages```为了提供对```HTML```内容的支持，选择了[Jekyll][2]作为模板系统，[Jekyll][2]是一个强大的静态模板系统，作为个人博客使用，基本上可以满足要求，也能保持管理的方便-

    ```Jekyll```是一种简单的、适用于博客的、静态网站生成引擎。它使用一个模板目录作为网站布局的基础框架，支持```Markdown```、```Textile```等标记语言的解析，提供了模板、变量、插件等功能，最终生成一个完整的静态```Web```站点。说白了就是，只要安装```Jekyll```的规范和结构，不用写```html```，就可以生成网站。


    ```Jekyll```的核心其实就是一个文本的转换引擎，用你最喜欢的标记语言写文档，可以是```Markdown```、```Textile```或者```HTML```等等，再通过```layout```将文档拼装起来，根据你设置的```URL```规则来展现，这些都是通过严格的配置文件来定义，最终的产出就是```web```页面。

    ```
        |-- _config.yml保存配置数据,在页面模板中使用site.可以应用.
        |-- _includes
        |-- _layouts
        |   |-- default.html
        |    -- post.html
        |-- _posts
        |   |--    2017-09-24-build-blog.markdown
        |-- _site
        -- index.html
    ```

- ```git```可以去廖雪峰的网站查看[文档][1].

![](/assets/article/2017-09-24_20h33_25.png)

[1]:https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000
[2]:http://jekyll.com.cn/
[3]:https://help.github.com/categories/github-pages-basics/
[4]:https://help.github.com/categories/customizing-github-pages/
[5]:http://wiki.jikexueyuan.com/project/github-pages-basics/