# [hellmonky的技术博客](hellmonky.github.io)

结合github和emacs(org-mode)来搭建自己的博客。
依托于github的友好特定，将所有个人博客搬迁到这儿，并且可以方便的远程提交和访问，将之前的memo内容合并在这儿，作为整体的显示内容来进行提交。

***一边用一边学习***

## 博客搭建

博客的搭建参考了网上提供的许多教程进行，主要有下面几个站点提供的资源：


阮一峰：[搭建一个免费的，无限流量的Blog](http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html)
一个热爱木工的软件工程师：[emacs + org-mode + octopress + github](http://ifq.github.io/blog/2012/08/10/org-octopress/)
on_1y：[使用 GitHub, Jekyll 打造自己的免费独立博客](http://blog.csdn.net/on_1y/article/details/19259435)
tuhaihe：[使用 Emacs Org 制作静态网站](http://tuhaihe.com/2013/06/17/use-emacs-orgmode-generate-website.html)

>其中阮一峰的教程



## 自己的实现

主要参考了上面资料中[on_1y的教程](http://blog.csdn.net/on_1y/article/details/19259435)

目录结构如下：
```shell
+ blog               # 博客根目录
   + org             # org文件根目录
      + _post
   + source          # org导出根目录，也是octopress本身用于生成blog的根目录
      + _post        # markdown或者org导出的html存在这里
      + _include     # 这里是一些octopress的UI template文件
      + _layouts     # 这里也是
      + rc           # 我的照片等资源的文件夹
      + video        # 我的视频文件夹
      + ...
   + public          # 通过命令 source下的内容会自动导出到 该目录，包括自定义的 rc、video
      + blog         # 内部的子文件按年月日排列
      + rc
      + video
      + ...
   + _deploy         #通过部署命令生产，为了更新github而产生
      + ...
```
