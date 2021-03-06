---
description: >-
  层叠样式表（Cascading Style Sheet，简称：CSS）是为网页添加样式的代码。本节将介绍 CSS
  的基础知识，并解答类似问题：怎样将文本设置为黑色或红色？怎样将内容显示在屏幕的特定位置？怎样用背景图片或颜色来装饰网页？
---

# CSS 基础

### [CSS 究竟什么来头？](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#css\_%E7%A9%B6%E7%AB%9F%E4%BB%80%E4%B9%88%E6%9D%A5%E5%A4%B4%EF%BC%9F) <a href="#css-jiu-jing-shen-me-lai-tou" id="css-jiu-jing-shen-me-lai-tou"></a>

和 HTML 类似，CSS 也不是真正的编程语言，甚至不是标记语言。它是一门样式表语言，这也就是说人们可以用它来选择性地为 HTML 元素添加样式。举例来说，要选择一个 HTML 页面里**所有**的段落元素，然后将其中的文本改成红色，可以这样写 CSS：

```
p {
  color: red;
}
```

Copy to Clipboard

不妨试一下：首先新建一个 `styles` 文件夹，在其中新建一个 `style.css` 文件，将这三行 CSS 保存在这个新文件中。

然后再将该 CSS 文件连接至 HTML 文档，否则 CSS 代码不会对 HTML 文档在浏览器里的显示效果有任何影响。（如果你没有完成前几节的实践，请复习 [处理文件](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/Dealing\_with\_files) 和 [HTML 基础](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/HTML\_basics)。）

1.  打开 `index.html` 文件，然后将下面一行粘贴到文档头（也就是 `<head>` 和 `</head>` 标签之间）。

    ```
    <link href="styles/style.css" rel="stylesheet">
    ```

    Copy to Clipboard
2. 保存 `index.html` 并用浏览器将其打开。应该看到以下页面：

![测试页面，文字设置为红色](https://mdn.mozillademos.org/files/16480/beginner-site-red.png)如果段落文字变红，那么祝贺你，你已经成功地迈出了 CSS 学习的第一步。

#### [“CSS 规则集”详解](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#%E2%80%9Ccss\_%E8%A7%84%E5%88%99%E9%9B%86%E2%80%9D%E8%AF%A6%E8%A7%A3) <a href="#css-gui-ze-ji-xiang-jie" id="css-gui-ze-ji-xiang-jie"></a>

让我们来仔细看一看上述CSS：

![图解CSS声明](https://mdn.mozillademos.org/files/16483/css-declaration.png)

整个结构称为 **规则集**（通常简称“规则”），各部分释义如下：

选择器（**Selector**）HTML 元素的名称位于规则集开始。它选择了一个或多个需要添加样式的元素（在这个例子中就是 `p` 元素）。要给不同元素添加样式只需要更改选择器就行了。声明（**Declaration**）一个单独的规则，如 `color: red;` 用来指定添加样式元素的**属性**。属性（**Properties**）改变 HTML 元素样式的途径。（本例中 `color` 就是 [`<p>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/p) 元素的属性。）CSS 中，由编写人员决定修改哪个属性以改变规则。属性的值（Property value）在属性的右边，冒号后面即**属性的值**，它从指定属性的众多外观中选择一个值（我们除了 `red` 之外还有很多属性值可以用于 `color` ）。

注意其他重要的语法：

* 每个规则集（除了选择器的部分）都应该包含在成对的大括号里（`{}`）。
* 在每个声明里要用冒号（`:`）将属性与属性值分隔开。
* 在每个规则集里要用分号（`;`）将各个声明分隔开。

如果要同时修改多个属性，只需要将它们用分号隔开，就像这样：

```
p {
  color: red;
  width: 500px;
  border: 1px solid black;
}
```

Copy to Clipboard

#### [多元素选择](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#%E5%A4%9A%E5%85%83%E7%B4%A0%E9%80%89%E6%8B%A9) <a href="#duo-yuan-su-xuan-ze" id="duo-yuan-su-xuan-ze"></a>

也可以选择多种类型的元素并为它们添加一组相同的样式。将不同的选择器用逗号分开。例如：

```
p, li, h1 {
  color: red;
}
```

Copy to Clipboard

#### [不同类型的选择器](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#%E4%B8%8D%E5%90%8C%E7%B1%BB%E5%9E%8B%E7%9A%84%E9%80%89%E6%8B%A9%E5%99%A8) <a href="#bu-tong-lei-xing-de-xuan-ze-qi" id="bu-tong-lei-xing-de-xuan-ze-qi"></a>

选择器有许多不同的类型。上面只介绍了**元素选择器**，用来选择 HTML 文档中给定的元素。但是选择操作可以更加具体。下面是一些常用的选择器类型：

| 选择器名称              | 选择的内容                                               | 示例                                                                                                                  |
| ------------------ | --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 元素选择器（也称作标签或类型选择器） | 所有指定(该)类型的 HTML 元素                                  | <p><code>p</code><br>选择 <code>&#x3C;p></code></p>                                                                   |
| ID 选择器             | 具有特定 ID 的元素（单一 HTML 页面中，每个 ID 只对应一个元素，一个元素只对应一个 ID） | <p><code>#my-id</code><br>选择 <code>&#x3C;p id="my-id"></code> 或 <code>&#x3C;a id="my-id"></code></p>                |
| 类选择器               | 具有特定类的元素（单一页面中，一个类可以有多个实例）                          | <p><code>.my-class</code><br>选择 <code>&#x3C;p class="my-class"></code> 和 <code>&#x3C;a class="my-class"></code></p> |
| 属性选择器              | 拥有特定属性的元素                                           | <p><code>img[src]</code><br>选择 <code>&#x3C;img src="myimage.png"></code> 而不是 <code>&#x3C;img></code></p>            |
| 伪（Pseudo）类选择器      | 特定状态下的特定元素（比如鼠标指针悬停）                                | <p><code>a:hover</code><br>仅在鼠标指针悬停在链接上时选择 <code>&#x3C;a></code>。</p>                                               |

选择器的种类远不止于此，更多信息请参阅 [选择器](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building\_blocks/Selectors)。

### [字体和文本](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#%E5%AD%97%E4%BD%93%E5%92%8C%E6%96%87%E6%9C%AC) <a href="#zi-ti-he-wen-ben" id="zi-ti-he-wen-ben"></a>

译注：再一次说明，中文字体文件较大，不适合直接用于 Web Font。

在探索了一些 CSS 基础后，我们来把更多规则和信息添加至 `style.css` 中，从而让示例更美观。首先，让字体和文本变得更漂亮。

1.  第一步，找到之前 [Google Font 输出的地址](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like#%E5%AD%97%E4%BD%93)。并以 [`<link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link) 元素的形式添加进 `index.html` 文档头（ [`<head>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/head) 和 `</head>` 之间的任意位置）。代码如下：

    ```
     <link href="https://fonts.font.im/css?family=Open+Sans" rel="stylesheet" type="text/css"> 
    ```

    Copy to Clipboard以上代码为当前网页下载 Open Sans 字体，从而使自定义 CSS 中可以对 HTML 元素应用这个字体。
2. 接下来，删除 `style.css` 文件中已有的规则。虽然测试是成功的了，但是红字看起来并不太舒服。
3.  将下列代码添加到相应的位置，用你在 Google Fonts 找到的字体替代 `font-family` 中的占位行。（ `font-family` 意味着你想要你的文本使用的字体。）这条规则首先为整个页面设定了一个全局字体和字号（因为 `<html>` 是整个页面的父元素，而且它所有的子元素都会继承相同的 `font-size` 和 `font-family`）：

    ```
    html {
      /* px 表示 “像素（pixels）”: 基础字号为 10 像素 */
      font-size: 10px;
      /* Google fonts 输出的 CSS */
      font-family: 'Open Sans', sans-serif;
    }
    ```

    Copy to Clipboard

    **注：**CSS 文档中所有位于 `/*` 和 `*/` 之间的内容都是 CSS 注释，它会被浏览器在渲染代码时忽略。你可以在这里写下对你现在要做的事情有帮助的笔记。

    **译注：**`/**/` 不可嵌套，`/*这样的注释是/*不行*/的*/`。CSS 不接受 `//` 注释。
4.  接下来为文档体内的元素（[`<h1>` (en-US)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading\_Elements)、[`<li>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/li) 和 [`<p>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/p)）设置字号。将标题居中显示，并为正文设置行高和字间距，从而提高页面的可读性。

    ```
    h1 {
      font-size: 60px;
      text-align: center;
    }

    p, li {
      font-size: 16px;
      /* line-height 后而可以跟不同的参数，如果是数字，就是当前字体大小乘上数字 */
      line-height: 2;
      letter-spacing: 1px;
    }
    ```

    Copy to Clipboard

可以随时调整这些 `px` **** 值来获得满意的结果，以下是大体效果：

![测试页面，设置了文字间距和行间距等格式。](https://mdn.mozillademos.org/files/16481/beginner-site-text.png)

### [一切皆盒子](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#%E4%B8%80%E5%88%87%E7%9A%86%E7%9B%92%E5%AD%90) <a href="#yi-qie-jie-he-zi" id="yi-qie-jie-he-zi"></a>

编写 CSS 时你会发现，你的工作好像是围绕着一个一个盒子展开的——设置尺寸、颜色、位置，等等。页面里大部分 HTML 元素都可以被看作若干层叠的盒子。

![a big stack of boxes or crates sat on top of one another](https://mdn.mozillademos.org/files/9441/boxes.jpg)

并不意外，CSS 布局主要就是基于盒模型的。每个占据页面空间的块都有这样的属性：

* `padding`：即内边距，围绕着内容（比如段落）的空间。
* `border`：即边框，紧接着内边距的线。
* `margin`：即外边距，围绕元素外部的空间。

![three boxes sat inside one another. From outside to in they are labelled margin, border and padding](https://mdn.mozillademos.org/files/9443/box-model.png)

这里还使用了：

* `width` ：元素的宽度
* `background-color` ：元素内容和内边距底下的颜色
* `color` ：元素内容（通常是文本）的颜色
* `text-shadow` ：为元素内的文本设置阴影
* `display` ：设置元素的显示模式（暂略）

开始在页面中添加更多 CSS 吧！大胆将这些新规则都添加到页面的底部，而不要纠结改变属性值会带来什么结果。

#### [更改页面颜色](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#%E6%9B%B4%E6%94%B9%E9%A1%B5%E9%9D%A2%E9%A2%9C%E8%89%B2) <a href="#geng-gai-ye-mian-yan-se" id="geng-gai-ye-mian-yan-se"></a>

```
html {
  background-color: #00539F;
}
```

Copy to Clipboard

这条规则将整个页面的背景颜色设置为 [所计划的颜色](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like)。

#### [文档体格式设置](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#%E6%96%87%E6%A1%A3%E4%BD%93%E6%A0%BC%E5%BC%8F%E8%AE%BE%E7%BD%AE) <a href="#wen-dang-ti-ge-shi-she-zhi" id="wen-dang-ti-ge-shi-she-zhi"></a>

```
body {
  width: 600px;
  margin: 0 auto;
  background-color: #FF9500;
  padding: 0 20px 20px 20px;
  border: 5px solid black;
}
```

Copy to Clipboard

现在是 [`<body>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/body) 元素。以上条声明，我们来逐条查看：

* `width: 600px;` —— 强制页面永远保持 600 像素宽。
* `margin: 0 auto;` —— 为 `margin` 或 `padding` 等属性设置两个值时，第一个值代表元素的上方**和**下方（在这个例子中设置为 `0`），而第二个值代表左边**和**右边（在这里，`auto` **** 是一个特殊的值，意思是水平方向上左右对称）。你也可以使用一个，三个或四个值，参考 [这里](https://developer.mozilla.org/zh-CN/docs/Web/CSS/margin#%E5%8F%96%E5%80%BC) 。
* `background-color: #FF9500;` —— 如前文所述，指定元素的背景颜色。我们给 body 用了一种略微偏红的橘色以与深蓝色的 [`<html>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/html) 元素形成反差，你也可以尝试其它颜色。
* `padding: 0 20px 20px 20px;` —— 我们给内边距设置了四个值来让内容四周产生一点空间。这一次我们不设置上方的内边距，设置右边，下方，左边的内边距为20像素。值以上、右、下、左的顺序排列。
* `border: 5px solid black;` —— 直接为 body 设置 5 像素的黑色实线边框。

#### [定位页面主标题并添加样式](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#%E5%AE%9A%E4%BD%8D%E9%A1%B5%E9%9D%A2%E4%B8%BB%E6%A0%87%E9%A2%98%E5%B9%B6%E6%B7%BB%E5%8A%A0%E6%A0%B7%E5%BC%8F) <a href="#ding-wei-ye-mian-zhu-biao-ti-bing-tian-jia-yang-shi" id="ding-wei-ye-mian-zhu-biao-ti-bing-tian-jia-yang-shi"></a>

```
h1 {
  margin: 0;
  padding: 20px 0;
  color: #00539F;
  text-shadow: 3px 3px 1px black;
}
```

Copy to Clipboard

你可能发现页面的顶部有一个难看的间隙，那是因为浏览器会在没有任何 CSS 的情况下 **** 给 [`<h1>` (en-US)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading\_Elements) 等元素设置一些**默认样式**。但这并不是个好主意，因为我们希望一个没有任何样式的网页也有基本的可读性。为了去掉那个间隙，我们通过设置 `margin: 0;` 来覆盖默认样式。

至此，我们已经把标题的上下内边距设置为 20 像素，并且将标题文本与 HTML **** 的背景颜色设为一致。

需要注意的是，这里使用了一个 `text-shadow` 属性，它可以为元素中的文本提供阴影。四个值含义如下：

* 第一个值设置**水平偏移值** —— 即阴影右移的像素数（负值左移）。
* 第二个值设置**垂直偏移值** —— 即阴影下移的像素数（负值上移）。
* 第三个值设置阴影的**模糊半径** —— 值越大产生的阴影越模糊。
* 第四个值设置阴影的基色。

不妨尝试不同的值看看能得出什么结果。

#### [图像居中](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#%E5%9B%BE%E5%83%8F%E5%B1%85%E4%B8%AD) <a href="#tu-xiang-ju-zhong" id="tu-xiang-ju-zhong"></a>

```
img {
  display: block;
  margin: 0 auto;
}
```

Copy to Clipboard

最后，我们把图像居中来使页面更美观。可以复用 body 的 `margin: 0 auto` ，但是需要一点点调整。 [`<body>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/body) 元素是**块级**元素，意味着它占据了页面的空间并且能够赋予外边距和其他改变间距的值。而图片是**内联**元素，不具备块级元素的一些功能。所以为了使图像有外边距，我们必须使用 `display: block` 给予其块级行为。

**注：**以上说明假定所选图片小于页面宽度（600 pixels）。更大的图片会溢出 body 并占据页面的其他位置。要解决这个问题，可以：\
1）使用 [图片编辑器](https://en.wikipedia.org/wiki/Raster\_graphics\_editor) 来减小图片宽度；\
2）用 CSS 限制图片大小，即减小 `<img>` 元素 [`width`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/width) 属性的值（比如 `400 px`）。

**注：**如果你暂时不能理解 `display: block` 和块级元素与行内元素的差别也没关系；随着你对 CSS 学习的深入，你将明白这个问题。`display` 属性的更多信息请查看 [参考页面](https://developer.mozilla.org/zh-CN/docs/Web/CSS/display) 。

### [小结](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/CSS\_basics#%E5%B0%8F%E7%BB%93) <a href="#xiao-jie" id="xiao-jie"></a>

如果你按部就班完成本文的实践，那么最终可以得到以下页面（可以 [查看我们的版本](https://roy-tian.github.io/learning-area/extras/getting-started-web/beginner-html-site-styled/)）：

![测试页面，设置了标题、正文字体，图片居中，背景色、文字块颜色。](https://mdn.mozillademos.org/files/16482/beginner-site-styled.png)

若遇到问题，可以参考 GitHub 上的 [完整示例代码](https://github.com/roy-tian/learning-area/tree/master/extras/getting-started-web/beginner-html-site-styled) 做对比。

本章介绍的 CSS 知识非常有限，更多内容请访问 [CSS学习页面](https://developer.mozilla.org/zh-CN/docs/Learn/CSS)。
