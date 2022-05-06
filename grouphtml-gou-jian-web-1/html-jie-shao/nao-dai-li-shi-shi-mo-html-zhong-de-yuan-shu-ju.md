---
description: >-
  在页面加载完成的时候，标签头里的内容显示，是不会在页面中出来的。它包含了像页面的<title>（标题），CSS（如果你选择用CSS来为HTML添加内容样式），指向自定义图标的链接和其他的（描述
  HTML 的数据元数据，如描述文档，以及描述重要的作者）。本文将包含上述内容并扩展，为您对标记的使用打下一个良好的基础。
---

# 脑袋里是什么？HTML中的元数据

### [什么是 HTML 头部元素？](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E4%BB%80%E4%B9%88%E6%98%AF\_html\_%E5%A4%B4%E9%83%A8%E5%85%83%E7%B4%A0) <a href="#shen-me-shi-html-tou-bu-yuan-su" id="shen-me-shi-html-tou-bu-yuan-su"></a>

让我们简单回顾一下[上一章的 HTML 文档](https://developer.mozilla.org/zh-CN/docs/learn/HTML/Introduction\_to\_HTML/Getting\_started#%e5%89%96%e6%9e%90html%e6%96%87%e6%a1%a3)：

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>我的测试站点</title>
  </head>
  <body>
    <p>这是我的页面</p>
  </body>
</html>
```

HTML[`<head>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/head) 元素与 [`<body>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/body)元素不同，它不会在浏览中显示，它的作用是保存页面的一些[元数据](https://developer.mozilla.org/zh-CN/docs/Glossary/Metadata)。

```
<head>
  <meta charset="utf-8">
  <title>我的测试站点</title>
</head>
```

复制到剪贴板

大型元数据  节策划[者工具](https://developer.mozilla.org/zh-CN/docs/Learn/Common\_questions/What\_are\_browser\_developer\_tools) 查看网页头像吧。

### [添加标题](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E6%B7%BB%E5%8A%A0%E6%A0%87%E9%A2%98) <a href="#tian-jia-biao-ti" id="tian-jia-biao-ti"></a>

之前已经讲过 [`<title>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/title)，不过它可以为添加文档和[`<h1>` (en-US)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading\_Elements)元素混搞了，[`<h1>` (en-US)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading\_Elements)正文标题的。但是另外一个标题是添加标题[`<h1>` (en-US)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading\_Elements)也叫作网页标题。不一样。

* [`<h1>` (zh-CN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading\_Elements) 元素在页面加载完毕时显示在页面中，通常只显示一次，显示标记页面内容的标题（故事名称、新闻摘要等）。
* [`<title>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/title)元素是一个元数据，用于表示整个 HTML 文档的标题（而不是文档内容）。

#### [主动学习：一个简单的例子](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E4%B8%BB%E5%8A%A8%E5%AD%A6%E4%B9%A0%EF%BC%9A%E4%B8%80%E4%B8%AA%E7%AE%80%E5%8D%95%E7%9A%84%E7%A4%BA%E4%BE%8B) <a href="#zhu-dong-xue-xi-yi-ge-jian-dan-de-shi-li" id="zhu-dong-xue-xi-yi-ge-jian-dan-de-shi-li"></a>

1. 为了开始这个操作库。我们希望你到我们的 Github 中下载一个我们希望的[标题](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/the-html-head/title-example.html)-example.html 类，你可以选择下面 的一个网页来学习
   1. 使用你的代码器，从页面中复制粘贴代码到一个新的文本文件中，然后将其保存到一个合适的地方。
   2. 点击页面中的“Raw”按钮，从浏览器的菜单中选择文件_>另存网页为..._，然后选择一个地方来保存这个文件。
2.  在浏览器中打开文件，你会看到类似的效果：

    ![一个简单的网页，标题设置为 \<title> 元素，\<h1> 设置为 \<h1> 元素。](https://mdn.mozillademos.org/files/17388/%E6%A0%87%E9%A2%98%E7%A4%BA%E4%BE%8B.png)现在很明显的可以看到`<h1>`出现的地方，和  `<title>`出现的地方！
3. 你应该尝试着在你的代码编辑器中打开这些代码，编辑这些元素的内容，然后在你的浏览器中刷新。祝你玩得开心。

如果元素`<title>`也被作为其他类似的点击类型，（浏览器中标地址栏被使用建议的星标），你会看到`<title>`的书签名的方式。 。

![Firefox中将网页添加为目录。书签名根据\<title>元素自动生成。](https://mdn.mozillademos.org/files/17389/%E4%B9%A6%E7%AD%BE%E7%A4%BA%E4%BE%8B.png)

元素`<title>`的内容被用在搜索的结果中，就像你即将在下面看到的一样。

### [元数据：\<meta>元素](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E5%85%83%E6%95%B0%E6%8D%AE%EF%BC%9A%3Cmeta%3E%E5%85%83%E7%B4%A0) <a href="#yuan-shu-ju-meta-yuan-su" id="yuan-shu-ju-meta-yuan-su"></a>

元数据就是描述元数据而HTML有一个“官方的方式来为一个文档添加元数据——  [`<meta>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meta)当然，其他在中提到的也可以被称为元数据。”有很多文章数据。会解释一些你经常看到的，先让`<meta>`你有一个概念。

#### [指定你的文档中字符的编码](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E6%8C%87%E5%AE%9A%E4%BD%A0%E7%9A%84%E6%96%87%E6%A1%A3%E4%B8%AD%E5%AD%97%E7%AC%A6%E7%9A%84%E7%BC%96%E7%A0%81) <a href="#zhi-ding-ni-de-wen-dang-zhong-zi-fu-de-bian-ma" id="zhi-ding-ni-de-wen-dang-zhong-zi-fu-de-bian-ma"></a>

在上面的中，这行是被包含的例子：

```
<meta charset="utf-8">
```

复制到剪贴板

元素的简单指定了该字符的编码——在这个文档中被使用的字符集。`utf-8`是一个通用的字符集，它包含了任何语言中的字符的字符。任意的语言；所以每个页面都使用设置会是一个好主意！

![包含中文和藏书的编码为utf8后，设置文字的网页。将正常显示。](https://mdn.mozillademos.org/files/17390/%E7%BC%96%E7%A0%81%E6%AD%A3%E7%A1%AE.png)这时，如果你将你的字符集设置为`GBK`（中国大陆国标字符集），页面将出现乱码：

![包含中文和藏文的网页。将页面编码设置为gbk后，藏语无法正常显示。](https://mdn.mozillademos.org/files/17391/%E7%BC%96%E7%A0%81%E9%94%99%E8%AF%AF.png)

**注**：一些设备（Chrome自动修改错误的编码）会编排问题，你所使用的浏览器，你可能不会这样说，你仍然应该为你的手动设置`utf-8`页面来避免在其他浏览器中可能出现的潜在问题。

#### [学习：体验集](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E4%BA%A4%E4%BA%92%E5%BC%8F%E5%AD%A6%E4%B9%A0%EF%BC%9A\_%E4%BD%93%E9%AA%8C%E5%AD%97%E7%AC%A6%E9%9B%86) <a href="#jiao-hu-shi-xue-xi-ti-yan-zi-fu-ji" id="jiao-hu-shi-xue-xi-ti-yan-zi-fu-ji"></a>

为了进行这个练习，回到你在前面\<title>中的HTML模板（[title-example.html网页](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/the-html-head/title-example.html)），改变获取字符集的`GBK`页面到，然后将其藏语添加到中。使用的代码：

```
<p>藏语示例：བཀྲ་ཤིས་བདེ་ལེགས།</p>
```

复制到剪贴板

#### [添加作者和描述](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E6%B7%BB%E5%8A%A0%E4%BD%9C%E8%80%85%E5%92%8C%E6%8F%8F%E8%BF%B0) <a href="#tian-jia-zuo-zhe-he-miao-shu" id="tian-jia-zuo-zhe-he-miao-shu"></a>

该`<meta>`元素包含的`name`和`content`特性：

* `name`指定元素的类型；说明该元素包含了元素类型的信息。
* `content`指定实际的元数据内容。

这两个元元素用于定义你的页面的作者和提供页面的简要描述是有用的。让我们看一个例子：

```
<meta name="author" content="Chris Mills">
<meta name="description" content="The MDN Learning Area aims to provide
complete beginners to the Web with all they need to know to get
started with developing web sites and applications.">
```

复制到剪贴板

指定作者可以在某些情况下管理系统有用的内容：如果您需要联系页面内容的，询问一些关于页面问题的作者。 一些自动获取页面作者的信息，然后用于某些用途。

指定包含内容关于页面内容的关键字的页面的描述是很有用的，因为它可能或者让你的页面在搜索引擎的相关的搜索中出现得更多（这些行为术语上被称为[搜索引擎优化](https://developer.mozilla.org/zh-CN/docs/Glossary/SEO)，或者[搜索引擎优化](https://developer.mozilla.org/zh-CN/docs/Glossary/SEO)。）

#### [实践操作：在搜索引擎中描述的使用](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E5%AE%9E%E8%B7%B5%E6%93%8D%E4%BD%9C\_%E5%9C%A8%E6%90%9C%E7%B4%A2%E5%BC%95%E6%93%8E%E4%B8%ADdescription%E7%9A%84%E4%BD%BF%E7%94%A8) <a href="#shi-jian-cao-zuo-zai-sou-suo-yin-qing-zhong-description-de-shi-yong" id="shi-jian-cao-zuo-zai-sou-suo-yin-qing-zhong-description-de-shi-yong"></a>

描述也被使用在搜索引擎显示的结果页中。下面通过一个来说明

1. 访问 [MDN Web Docs](https://developer.mozilla.org/zh-CN/)。
2. 查看网页源代码（_通过网页鼠标选择点击网页在弹出的菜单中查看\[\[\[\[\[\[\[\[]]]]]_】
3.  找到描述的元标签。就和做这样的展示：+

    ```
    <meta name="description" content="The MDN Web Docs site
        provides information about Open Web technologies
        including HTML, CSS, and APIs for both Web sites and
        progressive web apps.">
    ```

    复制到剪贴板
4. 现在，在你喜欢的搜索引擎里搜索“MDN Web Docs（下图展示是在谷歌搜索的情况）。你会在搜索里显示的内容`<meta>`和`<title>`元素如何——很值得看到哦！”

![“MDN Web Docs”的 Google 搜索结果](https://mdn.mozillademos.org/files/16074/mdn-search-result.png)

**注意**：在谷歌搜索里，在下面的主页面链接中，你会看到一些相关的子页面，你可以在 [谷歌的站长工具](https://www.google.com/webmasters/tools/)中看到这些是站点链接 ——一种可以让你的站点对搜索引擎配置更友好的方式。

**注意**：`<meta>`搜索特性已经不再。，关键词——提供关键词给搜索，根据不同的词，查找到的网站——已经被相关引擎收录，因为作弊者搜索了使用元素关键词`<meta>`关键词`<meta  name="keywords" content="fill, in, your, keywords, here">`到关键字，错误地引导搜索结果。

#### [其他类型的元数据](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E5%85%B6%E4%BB%96%E7%B1%BB%E5%9E%8B%E7%9A%84%E5%85%83%E6%95%B0%E6%8D%AE) <a href="#qi-ta-lei-xing-de-yuan-shu-ju" id="qi-ta-lei-xing-de-yuan-shu-ju"></a>

当你在网站上源码的时候，你会发现其他类型的元数据。信息。

例如，Facebook 编写的元数据协议 [Open Graph Data](https://ogp.me) 为网站提供了更丰富的元数据。在 MDN 源代码中，你会发现：

```
<meta property="og:image" content="https://developer.mozilla.org/static/img/opengraph-logo.png">
<meta property="og:description" content="The Mozilla Developer Network (MDN) provides
information about Open Web technologies including HTML, CSS, and APIs for both Web sites
and HTML5 Apps. It also documents Mozilla products, like Firefox OS.">
<meta property="og:title" content="Mozilla Developer Network">
```

复制到剪贴板

这个代码的效果和描述的一个效果，当你在 Facebook 上显示到 MDN 的时候，该链接将提供一个用户提供的链接：这为更丰富的体验。

![从 facebook 上显示的 MDN 主页打开图形协议数据，显示图像、标题和描述。](https://mdn.mozillademos.org/files/12349/facebook-output.png)Twitter 还拥有自己的原型数据协议，当网站的 URL 显示在 twitter.com 上时，它有类似的。

```
<meta name="twitter:title" content="Mozilla Developer Network">
```

复制到剪贴板

### [在你的站点增加自定义图标](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E5%9C%A8%E4%BD%A0%E7%9A%84%E7%AB%99%E7%82%B9%E5%A2%9E%E5%8A%A0%E8%87%AA%E5%AE%9A%E4%B9%89%E5%9B%BE%E6%A0%87) <a href="#zai-ni-de-zhan-dian-zeng-jia-zi-ding-yi-tu-biao" id="zai-ni-de-zhan-dian-zeng-jia-zi-ding-yi-tu-biao"></a>

为了进一步丰富你的网站设计，你可以在元数据中添加对自定义图标的引用，这些将在特定的场合中。

眼睛的图标已经存在，16 x 16 这些页面中这是很多浏览图标的第一个类型。您可以看到在每个打开的页面中的标签中出现了很多图标，以及在每个面板中在的目录页面中。

页面添加图标的方式有：

1. 将其保存在与网站的索引页面相同的目录中，以 ico 格式保存（或浏览器将支持更通用的，如 .gif.png，但使用 ICO 格式将确保能够在 Internet Explorer 6久远的浏览器显示一样）
2.  将引用添加到HTML \<head>中以引用它：

    ```
    <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
    ```

    复制到剪贴板

现代浏览器在各种场合使用favicons，如打开页面标签页和首页的页面。下面是一个favicon出现在首页的例子：![Firefox 书签面板，显示一个带有书签的示例，旁边显示一个网站图标。](https://mdn.mozillademos.org/files/12351/bookmark-favicon.png)

还有很多其他类似的图标类型可以考虑。例如，你可以在 MDN 主页的源中找到它：

```
<!-- third-generation iPad with high-resolution Retina display: -->
<link rel="apple-touch-icon-precomposed" sizes="144x144" href="https://developer.mozilla.org/static/img/favicon144.png">
<!-- iPhone with high-resolution Retina display: -->
<link rel="apple-touch-icon-precomposed" sizes="114x114" href="https://developer.mozilla.org/static/img/favicon114.png">
<!-- first- and second-generation iPad: -->
<link rel="apple-touch-icon-precomposed" sizes="72x72" href="https://developer.mozilla.org/static/img/favicon72.png">
<!-- non-Retina iPhone, iPod Touch, and Android 2.1+ devices: -->
<link rel="apple-touch-icon-precomposed" href="https://developer.mozilla.org/static/img/favicon57.png">
<!-- basic favicon -->
<link rel="shortcut icon" href="https://developer.mozilla.org/static/img/favicon32.png">
```

复制到剪贴板

解释解释每个 iPad 的东西的用途的用途 - 提供这些图标的图标，用来保存这些图标的主屏幕时使用。

不用担心现在所有这些类型的图标 - 这是一个相当被实现的功能，你将不会要求在这个课堂上学习这个先进知识点。这里的主要目的是让你提前了解有这东西防当你浏览其他网站的源代码时不理解源代码的含义。

*

**注**：如果你的网站使用了安全性策略（Content Security Policy, CSP）来增加安全性，这个会应用在图标上。如果你遇到图标没有被加载的问题，你需要确认headers [`Content-Security-Policy`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy)的 [`img-src` 指令](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/img-src) 没有禁止访问图标。

### [在 HTML 中应用 CSS 和 JavaScript](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E5%9C%A8html%E4%B8%AD%E5%BA%94%E7%94%A8css%E5%92%8Cjavascript) <a href="#zai-html-zhong-ying-yong-css-he-javascript" id="zai-html-zhong-ying-yong-css-he-javascript"></a>

几乎你使用网页地图的所有网站很容易使用 [网页](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS)功能，使用这些[网页](https://developer.mozilla.org/zh-CN/docs/Glossary/JavaScript)功能让网页工具，现在可以应用视频播放，以及其他网页功能[`<link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link)。以及[`<script>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script)元素。

*   &#x20;[`<link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link)元素元素位于文档的顶部。link元素有2个，rel="stylesheet"这个属性经常是这个文档的样式表，而href包含样式文件表的路径：

    ```
    <link rel="stylesheet" href="my-css-file.css">
    ```

    复制到剪贴板
*   [`<script>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script)部分没有必要调用文档，实际上是把它说明在你的（`</body>标签之前`选择之前）的一个更好的浏览器上，这样可以确保已经解析了 HTML 内容（如果脚本加载）个不存在的元素，浏览器会报错）。

    ```
    <script src="my-js-file.js"></script>
    ```

    复制到剪贴板

    **元素：** `<script>`元素，但它调用了，因此，你还需要一个标记`<script>`。

#### [实践操作：在网页中应用CSS和JavaScript](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E5%AE%9E%E8%B7%B5%E6%93%8D%E4%BD%9C\_%E5%9C%A8%E7%BD%91%E9%A1%B5%E4%B8%AD%E5%BA%94%E7%94%A8css%E5%92%8Cjavascript) <a href="#shi-jian-cao-zuo-zai-wang-ye-zhong-ying-yong-css-he-javascript" id="shi-jian-cao-zuo-zai-wang-ye-zhong-ying-yong-css-he-javascript"></a>

1. 开始操作之前，先拷贝我们的 [meta-example.html](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/the-html-head/meta-example.html) , [script.js](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/the-html-head/script.js)和[style.css](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/the-html-head/style.css)文件，然后把它们保存到本地电脑的同一个目录下，确保使用正确的文件名和文件格式。
2. 使用浏览器和文字编辑器同时打开你的HTML文件。
3. 根据上面的信息，添加[`<link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link)和[`<script>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script)部分到你的HTML文件中，这样你的HTML就可以应用CSS和JavaScript了。

如果你按照上面的步骤保存HTML文件并重新发现发现地的话，你会页面已经改了样了：

![包含 JS/CSS 的网页示例。CSS 将页面背景设置为绿色，由 JS 向页面添加一个动态列表。](https://mdn.mozillademos.org/files/17392/JS\_CSS\_%E7%A4%BA%E4%BE%8B.png)

* JavaScript 在页面内容中添加了一个列表。现在，当你点击列表中的列表项时，浏览器会自动输入一个对话框，要求你为新的项目按钮。当你点击确定时，启动那个新的列表项会上，当你点击添加到那些项目的文本列表项修改时，会弹出一个对话框允许你。
* CSS 使页面变成了一个大的文本到它的背景。一些 JavaScript 内容添加到中的页面中进行了样式化样式（添加了黑色的红色条）是 CSSjs 生成的白色中的样式。）

**注意**：如果你卡在这个我们的示例中，无法正常应用 CSS 和 JavaScript 页面，尝试查看一下 JavaScripts   [-and-js.html](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/the-html-head/css-and-js.html) 实例。

### [为文档设定语言主](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E4%B8%BA%E6%96%87%E6%A1%A3%E8%AE%BE%E5%AE%9A%E4%B8%BB%E8%AF%AD%E8%A8%80) <a href="#wei-wen-dang-she-ding-zhu-yu-yan" id="wei-wen-dang-she-ding-zhu-yu-yan"></a>

最后，值得一提的是可以（而且有必要）为站点设置语言，这个可以通过添加`lang`属性到HTML开始标签中来实现（  [meta-example.html](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/the-html-head/meta-example.html)），如下：

```
<html lang="zh-CN">
```

复制到剪贴板

这在很多方面都有用。你的 HTML 文档的保护设置很好，所以你的 HTML 文档有更有效的索引（例如，如果它允许在特定语言的结果中正确显示），对于使用屏幕上那些其他阅读器的视障人士也很有用（比如，汉语和英语中有“六个”这个词，发音却完全不同）。

你还可以将文档的设置为不同的语言。例如，我们可以将日语部分设置为日语，如下所示：

```
<p>日语实例: <span lang="jp">ご飯が熱い。</span>.</p>
```

复制到剪贴板

这些代码是根据[ISO 639-1](https://en.wikipedia.org/wiki/ISO\_639-1)标准定义的。你可以在[HTML 和 XML 中的语言标签](https://www.w3.org/International/articles/language-tags/)找到更多相关的。

### [总结](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/The\_head\_metadata\_in\_HTML#%E6%80%BB%E7%BB%93) <a href="#zong-jie" id="zong-jie"></a>

已经到了快速的HTML头的学习你学到更多的，但是现在只播了我们这番迷惑的演讲的潜在目标，并且希望，我们现在正在充分了解你的相关概念！上一篇我们将要学习 HTML 文本基础。
