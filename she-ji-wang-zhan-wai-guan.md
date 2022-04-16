---
description: 设计网站外观? 在为网站编写代码之前必须进行规划和设计工作，包括“网站提供什么信息？”、“想要什么字体和颜色？”、“网站是做什么的？”
---

# 设计网站外观



### [第一步：计划](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like#%E7%AC%AC%E4%B8%80%E6%AD%A5%EF%BC%9A%E8%AE%A1%E5%88%92) <a href="#di-yi-bu-ji-hua" id="di-yi-bu-ji-hua"></a>

在做任何事情之前都需要一些想法。网站要达到哪种目的？一个网站基本上可以做任何事情，但对于第一次尝试，应该保持简单。我们将从创建一个包含一个标题、一张图片和几个段落的简单网页开始。

首先，请考虑以下问题：

1. **网站的主题是什么？** 你喜欢狗、上海、还是吃豆人？
2. **基于所选主题要展示哪些信息？** 写下标题和几段文字，构思一个用于展示的图像。
3. **网站采用怎样的外观？** 用高阶术语来说，背景颜色是什么？使用哪种字体比较合适：正式的、卡通的、粗体、瘦体？

**备注：** 复杂项目需要更详细的指引，深入到颜色、字体、页面上项目之间的间距、适当的书写风格等所有细节。这有时被称为设计指南、设计系统或品牌手册，参见：[Firefox Photon Design System](https://design.firefox.com/photon/)。

### [绘制草图](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like#%E7%BB%98%E5%88%B6%E8%8D%89%E5%9B%BE) <a href="#hui-zhi-cao-tu" id="hui-zhi-cao-tu"></a>

接下来，拿起笔和纸，大致勾勒出你所希望的网站样子。虽然第一个简单的网页没有太多的草图，但你现在应该养成这样做的习惯。画草图很有用——并且不需要梵高的手法！

![](https://developer.mozilla.org/en-US/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like/website-drawing-scan.png)

**备注：** 即使在实际的复杂网站中，设计团队通常也是从粗略的草图开始设计的，再使用图形编辑器或 Web 技术建立数字模拟图。

Web 团队通常包括一个平面设计师和一个[用户体验](https://developer.mozilla.org/zh-CN/docs/Glossary/UX) (UX) 设计师。平面设计师把网站的视觉效果放在一起。用户体验设计师则以一种更抽象的模式来解决用户如何体验及与网站交互方面的问题。

### [选定内容](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like#%E9%80%89%E5%AE%9A%E5%86%85%E5%AE%B9) <a href="#xuan-ding-nei-rong" id="xuan-ding-nei-rong"></a>

此时可以开始组织网页上的内容了。

#### [文本](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like#%E6%96%87%E6%9C%AC) <a href="#wen-ben" id="wen-ben"></a>

准备好刚才撰写的标题和文字。

#### [主题颜色](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like#%E4%B8%BB%E9%A2%98%E9%A2%9C%E8%89%B2) <a href="#zhu-ti-yan-se" id="zhu-ti-yan-se"></a>

使用[色彩选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS\_Colors/Color\_picker\_tool)挑选心仪的颜色。当选中某种颜色时，会显示一个六位神秘代码，类似于`#660066`。它是一个_十六进制数_，用于表示颜色。将其复制并暂存。

![](https://developer.mozilla.org/en-US/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like/color-picker.png)

#### [图像](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like#%E5%9B%BE%E5%83%8F) <a href="#tu-xiang" id="tu-xiang"></a>

访问 [Google 图像搜索](https://www.google.com/imghp?gws\_rd=ssl) 来搜索合适的图片。

1. 当找到你想要的图像时，点击该图像以获得其放大的视图。
2. 右键单击图像（Mac上为 Ctrl + 单击），选择_将图像另存为..._，并选择一个安全的地方来保存你的图像。或者，从浏览器地址栏中复制图片的网址，以便以后使用。

![](https://developer.mozilla.org/en-US/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like/updated-google-images.png)

请注意，网络上的大多数图片，包括谷歌图片中的图片，都是有版权的。为了减少侵权的可能性，可以使用谷歌的许可证过滤器。点击_工具_按钮，然后点击下面出现的_使用权限_选项。你应该选择_知识共享许可_这个选项。

![](https://mdn.mozillademos.org/files/17382/%E5%9B%BE%E7%89%87%E8%AE%BE%E7%BD%AE.png)

#### [字体](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/What\_will\_your\_website\_look\_like#%E5%AD%97%E4%BD%93) <a href="#zi-ti" id="zi-ti"></a>

要选择一种字体：

1. 访问 [Google Fonts](https://www.google.com/fonts) 选择一种喜欢的字体。
2. 将谷歌给你的代码行复制至文本编辑器中，以保存备用。
3. 关于使用谷歌字体的更多细节，请参见[本页面](https://developers.google.com/fonts/docs/getting\_started)

