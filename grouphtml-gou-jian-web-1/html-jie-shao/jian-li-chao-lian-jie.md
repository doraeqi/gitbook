---
description: 超互联网链接非常重要——成为一个互联网的网络。本文介绍了创建链接所需的语法，并讨论了它们链接的最佳实现方法。
---

# 建立超链接

### [什么是超链接？](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E4%BB%80%E4%B9%88%E6%98%AF%E8%B6%85%E9%93%BE%E6%8E%A5) <a href="#shen-me-shi-chao-lian-jie" id="shen-me-shi-chao-lian-jie"></a>

是互联网提供的最令人兴奋的创新之一，它们从一开始就一直是互联网的一个特性，使我们的超互联网成为互联网的网络。超链接使我们能够将其他任何文档（或链接）其他资源），也可以链接到文档的指定部分，我们可以在一个简单的内容上提供应用程序（必须与安装的本地应用程序或其他东西不同）。几乎任何网络都可以转换为链接，点击（或激活）超链接网址浏览器（[URL](https://developer.mozilla.org/zh-CN/docs/Glossary/URL)浏览器转到另一个）。

注意：URL 内容可以指向 HTML 文件、文本文件、图像、文本文档、视频和音频文件以及可以在网络上保存的任何其他内容。 （需要选择合适的本地应用来打开或处理文件）或下载文件（稍后）。

BBC的主页的不同功能链接，以里面的内容就包含了非常多的内容，各自连到新闻、网站的其他地方（导览），或者进入/注册页面等等。

![bbc.co.uk 的首页，显示许多新闻项目和导航菜单功能](https://mdn.mozillademos.org/files/17032/updated-bbc-website.png)

### [链接的解析](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E9%93%BE%E6%8E%A5%E7%9A%84%E8%A7%A3%E6%9E%90) <a href="#lian-jie-de-jie-xi" id="lian-jie-de-jie-xi"></a>

通过将文本（或其他，[查看链接级别](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E5%9D%97%E7%BA%A7%E9%93%BE%E6%8E%A5)）转换为[`<a>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a)元素内的创建来基本， 给它一个[`href`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a#attr-href)属性（也称为目标链接），链接包含您希望链接内容的链接。

```
<p>我创建了一个指向
<a href="https://www.mozilla.org/zh-CN/">Mozilla 主页</a>
的超链接。
</p>
```

结果如下所示：

我创建了一个指向[Mozilla主页](https://www.mozilla.org/zh-CN/)的超链接。

#### [使用title属性支持添加信息](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E4%BD%BF%E7%94%A8title%E5%B1%9E%E6%80%A7%E6%B7%BB%E5%8A%A0%E6%94%AF%E6%8C%81%E4%BF%A1%E6%81%AF) <a href="#shi-yong-title-shu-xing-tian-jia-zhi-chi-xin-xi" id="shi-yong-title-shu-xing-tian-jia-zhi-chi-xin-xi"></a>

您可能添加到您的注意链接的另一个是标题的事情；这要包含有关链接的提供信息，例如包含文件的信息或需要的信息 例如：

```
<p>我创建了一个指向
<a href="https://www.mozilla.org/zh-CN/"
   title="了解 Mozilla 使命以及如何参与贡献的最佳站点。">Mozilla 主页</a>
的超链接。
</p>
```

结果如下（当鼠标悬停在链接上时，将作为标题出现）：

我创建了一个指向[Mozilla主页](https://www.mozilla.org/zh-CN/)的超链接。

注意：当悬停在其上时使用标题的信息时，这意味着用户导航网页的人链接获取信息很难。如果标题页面非常重要，应该使用所有能都轻松获取的方式来袭，比如突然出现在文本中。

#### [主动学习：创建您自己的示例链接](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E4%B8%BB%E5%8A%A8%E5%AD%A6%E4%B9%A0%EF%BC%9A%E5%88%9B%E5%BB%BA%E6%82%A8%E8%87%AA%E5%B7%B1%E7%9A%84%E7%A4%BA%E4%BE%8B%E9%93%BE%E6%8E%A5) <a href="#zhu-dong-xue-xi-chuang-jian-nin-zi-ji-de-shi-li-lian-jie" id="zhu-dong-xue-xi-chuang-jian-nin-zi-ji-de-shi-li-lian-jie"></a>

主动学习时间：我们希望您使用本地代码编辑器创建一个HTML文档（我们的 [入门模板](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/getting-started/index.html) 很适合）

* 在 HTML 内，尝试添加一个或多个段落或其他你知道类型的内容。
* 将某些内容转换为链接。
* 包含标题属性。

#### [块级链接](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E5%9D%97%E7%BA%A7%E9%93%BE%E6%8E%A5) <a href="#kuai-ji-lian-jie" id="kuai-ji-lian-jie"></a>

例如级，你可以将一些图像转换为元素，甚至是[块元素](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Block-level\_elements)`<a></a>`。

```
<a href="https://www.mozilla.org/zh-CN/">
  <img src="mozilla-image.png" alt="链接至 Mozilla 主页的 Mozilla 标志">
</a>
```

**注意**：你会在未来的文章中发现更多例子在 Web 中使用图像的。

### [统一资源定位符(URL)与路径(path)快速入门](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E7%BB%9F%E4%B8%80%E8%B5%84%E6%BA%90%E5%AE%9A%E4%BD%8D%E7%AC%A6url%E4%B8%8E%E8%B7%AF%E5%BE%84path%E5%BF%AB%E9%80%9F%E5%85%A5%E9%97%A8) <a href="#tong-yi-zi-yuan-ding-wei-fu-url-yu-lu-jing-path-kuai-su-ru-men" id="tong-yi-zi-yuan-ding-wei-fu-url-yu-lu-jing-path-kuai-su-ru-men"></a>

要地了解链接目标，你需要了解统一资源定位符和文件路径。本小节将全面介绍相关信息。

例如统一资源定位符（英文：**Uniform** Resource **Locator** ，简写：URL）是一个定义了在网络上的位置的一个文本字符串**。Mozilla**的中文主页定位在 `https://www.mozilla.org/zh-CN/`。

URL使用路径查找文件。路径指定文件系统中查看您查看文件的位置。查看一个简单的目录结构的例子（源码可 [创建超链接（creating-hyperlinks](https://github.com/roy-tian/learning-area/tree/master/html/introduction-to-html/creating-hyperlinks)）。）![一个简单的目录结构。 父目录名为creating-hyperlinks，包含两个文件index.html和contacts.html，两个目录projects和pdfs，分别包含一个index.html和一个project-brief.pdf文件](https://mdn.mozillademos.org/files/12409/simple-directory.png)

这个结构的**目录**名为`creating-hyperlinks`。当在网站上工作的时候，你会有一个包含整个网站的目录。在目录中，有我们一个`index.html`和一个`contacts.html`文件。在真实的网站上，`index.html`就成了我们的主页或登录页面。

请注意我们的根目录 `pdfs` 和他们包含的`projects`一个 PDF（`project-brief.pdf`）目录和一个`index.html`文件`index.html`。个`index.html`可能是项目相关信息的主登录界面。

*   **当前目录：**如果`index.html`（需要目录`index.html`链接的）只包含一个超指向`contacts.html`与文件，你指定了想要的目录名，因为它是当前文件的目录名。所以你应该使用的 URL 是`contacts.html`：

    ```
    <p>要联系某位工作人员，请访问我们的 <a href="contacts.html">联系人页面</a>。</p>
    ```

    复制到剪贴板
*   **子目录：**如果`index.html`（链接目录）进入目录，然后`index.html`想要包含一个超要指向的项目，因此`projects/index.html`需要先指定项目的文件名。通过目录的名称，然后是正斜的文件名，然后是文件名。您要使用的网址是：`projects/index.htmlprojects/index.html`

    ```
    <p>请访问 <a href="projects/index.html">项目页面</a>。</p>
    ```

    复制到剪贴板
*   **上级目录：**如果你想在`projects/index.html`中包含一个使用指向的`pdfs/project-brief.pdf`超号链接，你必须先返回上级目录，然后再回到`pdf`目录。`..`网址是 `../pdfs/project-brief.pdf`：

    ```
    <p>点击打开 <a href="../pdfs/project-brief.pdf">项目简介</a>。</p>
    ```

    复制到剪贴板

注意：如果需要的话，你可以将这些功能的多个例子和复杂的 URL 结合起来`../../../complex/path/to/my/file.html`。

#### [文档截图](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E6%96%87%E6%A1%A3%E7%89%87%E6%AE%B5) <a href="#wen-dang-pian-duan" id="wen-dang-pian-duan"></a>

超文档可以链接到外部，也可以链接到HTML的特定部分（被称为**文档的片段**）链接。要实现这一点，你必须首先给要的元素分配一个属性。例如，想想链接到一个特定的标题，可以是：[`id`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global\_attributes#attr-id)

```
<h2 id="Mailing_address">邮寄地址</h2>
```

复制到剪贴板

然后例如到那个特定的`id`，可以在链接的结尾使用一个您的井号指向它，：

```
<p>要提供意见和建议，请将信件邮寄至 <a href="contacts.html#Mailing_address">我们的地址</a>。</p>
```

复制到剪贴板

你甚至可以在同一份下，通过链接文档文档，来链接到同一份的另一个部分：

```
<p>本页面底部可以找到 <a href="#Mailing_address">公司邮寄地址</a>。</p>
```

复制到剪贴板

#### [绝对**URL**和相对**URL**](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E7%BB%9D%E5%AF%B9url%E5%92%8C%E7%9B%B8%E5%AF%B9url) <a href="#jue-dui-url-he-xiang-dui-url" id="jue-dui-url-he-xiang-dui-url"></a>

你可能会在网络上遇到两个术语，**绝对 URL**和**相对 URL** _（或者称为，**绝对链接**和**相对链接**）_：

**绝对URL**：指向由其在Web上的绝对位置定义的协议的位置，[协议](https://developer.mozilla.org/zh-CN/docs/Glossary/Protocol)（域名）和[域名](https://developer.mozilla.org/zh-CN/docs/Glossary/Domain\_name)（域名）。像下面的例子，如果文件`index.html`上传到`projects`这一个目录。并且`projects`目录位于web服务站点的根目录，那么这个页面的域名为`http://www.example.com`，那么这个页面访问（或者说，因为没有在指定的情况下通过URL访问，因为在大多数情况下web服务会默认访问加载某个站点就可以`http://www.example.com/projects/index.html`访问`http://www.example.com/projects/`特定`index.html`页面）

因为 URL 在哪里使用，它总是指向确定的相同位置。

**相对URL**：指向与链接看到的文件相关的位置，您是我们在前面第一节中所位置的`http://www.example.com/projects/index.html`目录。例如，如果想从示例文件链接转到相同的下一个PDF文件，URL就是文件名URL——例如`project-brief.pdf`——没有其他的信息要求。如果PDF文件能够在`projects`的子`pdfs`中访问到，相对路径就是目录`pdfs/project-brief.pdf`（的绝对是URL `http://www.example.com/projects/pdfs/project-brief.pdf`）

一个相对 URL 将指向不同的位置，把它的最上面的位置，它的位置中的位置——例如，如果我们的`index.html`文件从`projects`目录移动到 Web 站点的根目录（，而不是任何目录的`pdfs/project-brief.pdf`位置） URL `http://www.example.com/pdfs/project-brief.pdf`，指向而不是`http://www.example.com/projects/pdfs/project-brief.pdf`

它，您的`project-brief.pdf`文件和`pdfs`文件夹的位置`index.html`而发生了变化——这当然不会因为您的链接指向错误的位置，因此，如果您的点击，无法工作。

### [链接最佳实践](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E9%93%BE%E6%8E%A5%E6%9C%80%E4%BD%B3%E5%AE%9E%E8%B7%B5) <a href="#lian-jie-zui-jia-shi-jian" id="lian-jie-zui-jia-shi-jian"></a>

下面是一些在写元素时可以遵循的最佳做法。

*

#### [使用清晰的链接措辞](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E4%BD%BF%E7%94%A8%E6%B8%85%E6%99%B0%E7%9A%84%E9%93%BE%E6%8E%A5%E6%8E%AA%E8%BE%9E) <a href="#shi-yong-qing-xi-de-lian-jie-cuo-ci" id="shi-yong-qing-xi-de-lian-jie-cuo-ci"></a>

把链接给你的页面很容易。不管怎样。我们让所有的都可以使用，他们的当前环境链接和这些工具。

* 使用屏幕阅读器的喜欢从页面上的一个链接跳到另一个链接，然后用户时间来阅读链接。
* 搜索引擎使用文本链接来目标文件，所以在中包含关键字是一个很好的链接文本索引，以有效的地描述与相关的信息。
* 每次浏览都会浏览一个字，而他们的眼睛会被页面的特征所吸引，比如链接。他们会找到描述性读者的链接。

下面是一个具体的例子：

_**好的**链接文本:_ [下载Firefox](https://firefox.com)

```
<p><a href="https://firefox.com/">
  下载Firefox
</a></p>
```

复制到剪贴板

_**不好的**链接文本：_ [点击这里](https://firefox.com)下载Firefox

```
<p><a href="https://firefox.com/">
  点击这里
</a>
下载Firefox</p>
```

复制到剪贴板

其他提示：

* 很重复的 URL 作为文本的一部分——看起来 URL，当屏幕朗读器有一个手机出现的读取的时候丑陋就更丑陋了。
* 在链接文本中说“链接”或“链接到”——它只是噪音。屏幕显示有一个不显示的链接。用户知道链接有一个并且链接，因为通常是用不同的颜色设计的，告诉存在下划线（这类用户通常习惯了不应该被打破，因为它。）
* 保留你的链接标签，如果你不小心——长链接特别关注阅读器用户，必须让他们阅读整件事情。

#### [其他使用相对链接](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E5%B0%BD%E5%8F%AF%E8%83%BD%E4%BD%BF%E7%94%A8%E7%9B%B8%E5%AF%B9%E9%93%BE%E6%8E%A5) <a href="#jin-ke-neng-shi-yong-xiang-dui-lian-jie" id="jin-ke-neng-shi-yong-xiang-dui-lian-jie"></a>

在上面的中，你可能会认为当时链接使用链接是一个好主意；但是，当页面像相对链接那样移动的时候，它们不会改变。，当网站绝对到同一个的其他描述位置时，你应该使用相对链接链接（当链接到另一个网站的时候，你需要使用绝对链接）：

* 首先，检查代码要更多——相对URL通常比URL更容易阅读。
* 在可能的情况下，使用 URL 比较有效。使用绝对 URL，下浏览器首先通过（见[万维网](https://developer.mozilla.org/zh-CN/docs/Glossary/DNS)[是如何的](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/How\_the\_Web\_works)）查找服务器的真实位置，然后转到该服务器并查找所请求的位置这只是相对浏览器在相对浏览器上做的相同的文件，因此，你绝对使用 URL 是 URL，你的器绝对让你的工作。着它的效能会降低。

#### [非HTML资源——暴露链接到清晰的指示](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E9%93%BE%E6%8E%A5%E5%88%B0%E9%9D%9Ehtml%E8%B5%84%E6%BA%90\_%E2%80%94%E2%80%94%E7%95%99%E4%B8%8B%E6%B8%85%E6%99%B0%E7%9A%84%E6%8C%87%E7%A4%BA) <a href="#lian-jie-dao-fei-html-zi-yuan-liu-xia-qing-xi-de-zhi-shi" id="lian-jie-dao-fei-html-zi-yuan-liu-xia-qing-xi-de-zhi-shi"></a>

当链接到一个PDF或Word文档）需要下载的媒体（如或音频）或有其他潜在的或需要的流媒体（打开一个视频，或加载Flash）窗口时，你应该添加明确显示的措辞，以减少任何混乱。

* 如果你是在低连接，点击一个链接，然后就开始下载大文件。
* 如果你安装了 Flash 播放器，点击一个链接，然后被一个 Flash 的页面。

让我们看看一些例子，看看这里我们可以使用的文本：

```
<p><a href="http://www.example.com/large-report.pdf">
  下载销售报告（PDF, 10MB）
</a></p>

<p><a href="http://www.example.com/video-stream/">
  观看视频（将在新标签页中播放, HD画质）
</a></p>

<p><a href="http://www.example.com/car-game">
  进入汽车游戏（需要Flash插件）
</a></p>
```

复制到剪贴板

#### [在下载链接时使用下载属性](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E5%9C%A8%E4%B8%8B%E8%BD%BD%E9%93%BE%E6%8E%A5%E6%97%B6%E4%BD%BF%E7%94%A8\_download\_%E5%B1%9E%E6%80%A7) <a href="#zai-xia-zai-lian-jie-shi-shi-yong-download-shu-xing" id="zai-xia-zai-lian-jie-shi-shi-yong-download-shu-xing"></a>

当链接到您要下载的资源而不是在浏览器中打开时，您可以使用下载属性来提供一个默认的保存文件名（译文仅适用于[同源 URL](https://developer.mozilla.org/zh-CN/docs/Web/Security/Same-origin\_policy)）。下面是一个下载链接 Firefox Windows最新版本的示例：

```
<a href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=zh-CN"
   download="firefox-latest-64bit-installer.exe">
  下载最新的 Firefox 中文版 - Windows（64位）
</a>
```

### [主动学习：创建一个导航菜单](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E4%B8%BB%E5%8A%A8%E5%AD%A6%E4%B9%A0%EF%BC%9A%E5%88%9B%E5%BB%BA%E4%B8%80%E4%B8%AA%E5%AF%BC%E8%88%AA%E8%8F%9C%E5%8D%95) <a href="#zhu-dong-xue-xi-chuang-jian-yi-ge-dao-hang-cai-dan" id="zhu-dong-xue-xi-chuang-jian-yi-ge-dao-hang-cai-dan"></a>

在这个练习中，我们希望你把一些页面和导航菜单链接起来，创建一个多页面的网站。这是创建网站的常见方式——每一页的页面结构都相同，包括使用相同的导航菜单，所以当时，它当一个不同的联系方式的印象是你的内容被停留在同一个地方，点击的提议来了。

您需要将以下四页的本地副本取同一个目录中。（如果您想要完整列表，请参见[导航菜单开始](https://github.com/roy-tian/learning-area/tree/master/html/introduction-to-html/navigation-menu-start)目录）：

* [索引.html](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/navigation-menu-start/index.html)
* [项目.html](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/navigation-menu-start/projects.html)
* [图片.html](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/navigation-menu-start/pictures.html)
* [社会.html](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/navigation-menu-start/social.html)

你应该：

1. 在一个上的指定添加一个页面页面的顺序，其中包含要的菜单链接列表只是一个链接列表，因此这通常在名称上的位置表是没有确定的。
2. 将每个页面的名称转换为该页面的链接。
3. 将导航菜单复制到每个页面。
4. 每一页都只删除同一个包含自己的页面的链接——显示一个没有任何意义的链接，并在页面上显示和链接，只在当前的页面上显示和提示。

最终的例子应该是这样的：

![简单的HTML导航菜单，包含主页、图片、项目、社交四个项目。](https://mdn.mozillademos.org/files/17395/navigation\_example\_cn.png)

**注意**：如果你卡了，或者导航你是否正确，你可以检查上的目录，看看正确的答案。

### [电子邮件链接](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E7%94%B5%E5%AD%90%E9%82%AE%E4%BB%B6%E9%93%BE%E6%8E%A5) <a href="#dian-zi-you-jian-lian-jie" id="dian-zi-you-jian-lian-jie"></a>

当点击一个发送的电子邮件信息而不是一个资源或页面时，这种情况是可以实现的新连接或 链接[`<a>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a)的`mailto`。\
常用的使用`mailto`格式：链接），链接简单说明的电子邮件地址。

```
<a href="mailto:nowhere@mozilla.org">向 nowhere 发邮件</a>
```

复制到剪贴板

这会创建一个链接，看起来像这样：[向无处发邮件](mailto:nowhere@mozilla.org)。

“如果你的邮件的地址，甚至是可选的发送，只是没有你的一个[`href`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a#attr-href)简单的选择”`mailto:`发送的地址，地址信息，这通常在“分享”链接是有用的，用户可以发送给他们选择的邮件

#### [具体细节](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E5%85%B7%E4%BD%93%E7%BB%86%E8%8A%82) <a href="#ju-ti-xi-jie" id="ju-ti-xi-jie"></a>

除了电子邮件地址之外，您还可以提供其他主题信息，您还可以提供其他信息标题。任何标准的邮件字段都可以提供给您的邮件 URL。 )（这不是一个真正的头字段，指定您为新邮件的一个短内容消息）。但允许查询的项和值被指定为。

下面是一个包含cc、bcc、主题和主体的示例：

```
<a href="mailto:nowhere@mozilla.org?cc=name2@rapidtables.com&bcc=name3@rapidtables.com&subject=The%20subject%20of%20the%20email&body=The%20body%20of%20the%20email">
  Send mail with cc, bcc, subject and body
</a>
```

复制到剪贴板

**注意：**每个字段的值必须是 URL 编码的打印符号。有字符（不能显示字符格式表换行、分页符）和空格 [百分比转义](http://en.wikipedia.org/wiki/Percent-encoding)字符。注意注意使用方法（方法`?`）来空白主图，以及`mailto:`&&&&&&& 来字符中的参数值使用[方法](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/Sending\_and\_retrieving\_form\_data#get\_%e6%96%b9%e6%b3%95)查询参数的URL。& 了解这个标准的URL查询方法。

这里有一些其他的示例`mailto`链接：

* [邮寄：](mailto:)
* [mailto:nowhere@mozilla.org](mailto:nowhere@mozilla.org)
* [邮寄地址：nowhere@mozilla.org,nobody@mozilla.org](mailto:nowhere@mozilla.org,nobody@mozilla.org)
* [mailto:nowhere@mozilla.org?cc=nobody@mozilla.org](mailto:nowhere@mozilla.org?cc=nobody@mozilla.org)
* [mailto:nowhere@mozilla.org?cc=nobody@mozilla.org\&subject=This%20is%20the%20subject](mailto:nowhere@mozilla.org?cc=nobody@mozilla.org\&subject=This%20is%20the%20subject)

### [小结](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks#%E5%B0%8F%E7%BB%93) <a href="#xiao-jie" id="xiao-jie"></a>

即是即是样式！您将在下面开始查看功能的链接。返回下面的文本时，我们会在中间的 HTML 中发现，并查看/查看一些不显示的效果，您将看到的 -高级文本格式是您的下一站。
