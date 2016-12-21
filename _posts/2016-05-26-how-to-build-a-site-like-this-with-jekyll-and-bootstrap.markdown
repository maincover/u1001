---
layout:     post
title:      History
author:     u1001
date:       2016-05-26 08:13:00 +0800
categories: notes
tags: Bootstrap Jekyll U1001
mediaImage: images/history-tamara5.png
excerpt: Inserm u1001
---

Ta Ma Ra’s friendship started in the spring of 1991, when ,two young PhD students Ivan and François joined Miro Radman's lab on the scientific campus of the Institut Jacques Monod in Jussieu (Paris, France). Miro Radman's scientific life had already a rich history (clik on pre-TaMaRa history) including the discovery of the SOS response, the mechanisms of mismatch repair and the molecular nature of the species barrier.


The lab was relatively small (10-15 people very dynamic people) and poor but they had great fun and their work (evolution of mutators, barriers to horizontal transfer in bacteria, errors in RNA) was well published, attracting interest from the scientitic community at large and even more importantly from young students, colleagues and post-docs. Most of these belonged to the " mutator network " which included 7 labs from 7 different disciplines and which met on a regular basis to exchange ideas and data about the role played by mutator in bacterial evolution (and related topics such as pathogenesis and the emergence of antibiotic resistance) .


After 9 years spent together in Jussieu, which included the PhD of Ivan and François in 1995, Ta Ma Ra’s lab was created in the Necker Children's Hospital Medical School in Paris where it doubled in space and number of people and receive enough funding to start completely new projects. Convinced of the use of Escherichia coli that brought so much to science and so much fun to us, we decided to increase even further the importance of it's genetic analysis by using generic technologies such as fluorescent microscopy that could be applied to investigate many different basic questions about sex, life and death of this model bacteria on an individual basis.


## 这个博客网站的源代码在哪里？

这个网站的源代码仓库放在了[Github](http://github.com/)上，点击[这里]({{site.repository}})查看源代码。
在Github中，个人、组织、项目，都可以有自己的[GitHub Pages](https://pages.github.com)，程序员们可以使用编程的方式，进行个人、组织、项目的介绍页制作。
这篇博客就放在了[易企秀团队](http://github.com/eqxiu/)的Github Pages中。

## 什么是Jekyll？

[Jekyll](http://jekyll.bootcss.com/)是一个用Ruby开发的静态站点生成器——将原始的纯文本格式的文档（比如这一篇博客，
是用[Markdown](https://daringfireball.net/projects/markdown/)写的），
加上使用[Liquid](https://github.com/Shopify/liquid/wiki)标记写的模版（存储为HTML格式），从而转化成一个完整的静态网站。

这里的需要特别指出一点——[Github Pages原生支持使用Jekyll](https://help.github.com/articles/about-github-pages-and-jekyll/)。
当我往Github Pages所在的代码仓库发布新博客的时候（比如这一篇），Jekyll会读取设置、生成网页，最终生成一个由静态网页形成的网站；
如果在本地查看的话，你会发现Jekyll生成的静态网站被放在了一个名称为“_site”的文件夹下 —— 一个没有后端、没有数据库的静态网站。

关于Jekyll的更多详细信息，请到[这个网站](http://jekyll.bootcss.com/)查看。

## 什么是Bootstrap？

[Bootstrap](http://www.bootcss.com/)是一个非常优秀的前端开发框架，由于它诸多设计良好的CSS样式（比如网格，组件等等）、Javascript插件，
能让你快速开发一个漂亮的页面。

点击[这里](http://expo.bootcss.com/)，欣赏众多使用Bootstrap开发的网站。

到目前为止，我们可以看出来——我们是通过提供纯本文（比如Markdown格式的文本）和模版，让Jekyll生成静态的HTML页面，借助于Bootstrap良好设计的CSS样式，
我们就得到了一个漂亮的博客网站。

## 怎么样发布一篇新博客？

以当前这篇博客为例，如果你已经下载了这个博客网站的[源代码]({{site.repository}})，那么你可以在源代码的**“_post”**目录下，
找到一个名称为**“2016-05-26-how-to-build-a-site-like-this-with-jekyll-and-bootstrap.markdown”**的文件，就是你正在读的这篇博客了。

### 创建文章的文件

如果你要创建一篇新博客，需要按照以下规则给博客文件起名字：

{% highlight bash %}
YEAR-MONTH-DAY-title.MARKUP
{% endhighlight %}

在这里，`年`是4位数字，`月`和`日`都是2位数字。`MARKUP`扩展名代表了这篇文章是用什么格式写的。下面是一些合法的文件名的例子：

{% highlight bash %}
2011-12-31-new-years-eve-is-awesome.md
2012-09-12-how-to-write-a-blog.textile
{% endhighlight %}

### 内容格式

所有博客文章顶部必须有一段[YAML头信息](http://jekyll.bootcss.com/docs/frontmatter/)(YAML front- matter)。
在它下面，就可以选择你喜欢的格式来写文章。Jekyll支持2种流行的标记语言格式：
[Markdown](http://daringfireball.net/projects/markdown/) 和 [Textile](http://textile.sitemonks.com/)。 

正是头信息开始让 Jekyll 变的很酷。任何只要包含 [YAML](http://yaml.org/) 头信息的文件在 Jekyll 中都能被当做一个特殊的文件来处理。
头信息必须在文件的开始部分，并且需要按照 YAML 的格式写在两行三虚线之间。下面是一个基本的例子：

{% highlight yml%}
---
highlight
layout: post
title: Blogging Like a Hacker
---
{% endhighlight %}

接下来，你就可以通过使用[Markdown](https://daringfireball.net/projects/markdown/)来写文章内容了（想看例子的话，可以看看本博客是怎么写的）。

例如，在文章里引用其他资源文件，比如下面这张图片（名称为**“jekyll-blog.png”**，让我放到了网站源代码**“images”**目录下）：

![使用Jekyll和Bootstrap，创建一个静态网站]({{ site.url }}/images/jekyll-blog.png)

我就可以通过以下形式引用到博客里面：

{% highlight text %}
![使用Jekyll和Bootstrap，创建一个静态网站]({% raw %}{{ site.url }}{% endraw %}/images/jekyll-blog.png)
{% endhighlight %}
