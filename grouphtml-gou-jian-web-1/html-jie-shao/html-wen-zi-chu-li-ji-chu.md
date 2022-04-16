---
description: >-
  HTML的主要工作是编辑文本结构和文本内容（也称为语义semantics），以便浏览器能正确的显示。 本文介绍了
  HTML的使用方法：在一段文本中添加标题和段落，强调语句，创建列表等等。
---

# HTML 文字处理基础

### [基础: 标题和段落](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E5%9F%BA%E7%A1%80\_%E6%A0%87%E9%A2%98%E5%92%8C%E6%AE%B5%E8%90%BD) <a href="#ji-chu-biao-ti-he-duan-luo" id="ji-chu-biao-ti-he-duan-luo"></a>

大部分的文本结构由标题和段落组成。 不管是小说、报刊、教科书还是杂志等。

![An example of a newspaper front cover, showing use of a top level heading, subheadings and paragraphs.](https://mdn.mozillademos.org/files/16552/peoples.jpg)

内容结构化会使读者的阅读体验更轻松，更愉快。

在HTML中，每个段落是通过 [`<p>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/p) 元素标签进行定义的, 比如下面这样：

```
<p>我是一个段落，千真万确。</p>
```

Copy to Clipboard

每个标题（Heading）是通过“标题标签”进行定义的：

```
<h1>我是文章的标题</h1>
```

Copy to Clipboard

这里有六个标题元素标签 —— `<h1>`、`<h2>`、`<h3>`、`<h4>`、`<h5>`、`<h6>`。每个元素代表文档中不同级别的内容; `<h1>` 表示主标题（the main heading），`<h2>` 表示二级子标题（subheadings），`<h3>` 表示三级子标题（sub-subheadings），等等。

#### [编辑结构层次](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E7%BC%96%E8%BE%91%E7%BB%93%E6%9E%84%E5%B1%82%E6%AC%A1) <a href="#bian-ji-jie-gou-ceng-ci" id="bian-ji-jie-gou-ceng-ci"></a>

这里举一个例子。在一个故事中，\<h1>表示故事的名字，\<h2>表示每个章节的标题， \<h3>表示每个章节下的子标题，以此类推。

```
<h1>三国演义</h1>

<p>罗贯中</p>

<h2>第一回 宴桃园豪杰三结义 斩黄巾英雄首立功</h2>

<p>话说天下大势，分久必合，合久必分。周末七国分争，并入于秦。及秦灭之后，楚、汉分争，又并入于汉……</p>

<h2>第二回 张翼德怒鞭督邮 何国舅谋诛宦竖</h2>

<p>且说董卓字仲颖，陇西临洮人也，官拜河东太守，自来骄傲。当日怠慢了玄德，张飞性发，便欲杀之……</p>

<h3>却说张飞</h3>

<p>却说张飞饮了数杯闷酒，乘马从馆驿前过，见五六十个老人，皆在门前痛哭。飞问其故，众老人答曰：“督邮逼勒县吏，欲害刘公；我等皆来苦告，不得放入，反遭把门人赶打！”……</p>
```

Copy to Clipboard

所涉及的元素具体代表什么，完全取决于作者编辑的内容，只要层次结构是合理的。在创建此类结构时，您只需要记住一些最佳实践：

* 您应该最好只对每个页面使用一次\<h1> — 这是顶级标题，所有其他标题位于层次结构中的下方。
* 请确保在层次结构中以正确的顺序使用标题。不要使用\<h3>来表示副标题，后面跟\<h2>来表示副副标题 - 这是没有意义的，会导致奇怪的结果。
* 在可用的六个标题级别中，您应该只在每页使用不超过三个，除非您认为有必要使用更多。具有许多级别的文档（即，较深的标题层次结构）变得难以操作并且难以导航。在这种情况下，如果可能，建议将内容分散在多个页面上。

#### [为什么我们需要结构化?](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E4%B8%BA%E4%BB%80%E4%B9%88%E6%88%91%E4%BB%AC%E9%9C%80%E8%A6%81%E7%BB%93%E6%9E%84%E5%8C%96) <a href="#wei-shen-me-wo-men-xu-yao-jie-gou-hua" id="wei-shen-me-wo-men-xu-yao-jie-gou-hua"></a>

回答这个问题前，让我们先来看一段文档示例“[text-start.html](https://github.com/mdn/learning-area/blob/master/html/introduction-to-html/html-text-formatting/text-start.html)” — 并从运行这段文档示例（美味的豆沙食谱）开始。首先，您可以复制一份并保存到本地机器上，在之后的练习中您将用到它。在这个文档的主体 （body）中包含了多个内容 — 这些内容没有做任何标记，但是编辑时使用了换行 (输入回车/换行跳转到下一行)处理。

然而，当您在浏览器中打开文档时，您会看到文本显示为一整块！

![A webpage that shows a wall of unformatted text, because there are no elements on the page to structure it.](https://mdn.mozillademos.org/files/12972/text-no-formatting.png)

这是因为没有元素给内容结构，所以浏览器不知道什么是标题，什么是段落。此外：

* 用户在阅读网页时，往往会快速浏览以查找相关内容，经常只是阅读开头的标题（我们通常在一个网页上会花费很少的时间 [spend a very short time on a web page](http://www.nngroup.com/articles/how-long-do-users-stay-on-web-pages/))。如果用户不能在几秒内看到一些有用的内容，他们很可能会感到沮丧并离开。
* 对您的网页建立索引的搜索引擎将标题的内容视为影响网页搜索排名的重要关键字。没有标题，您的网页在[SEO](https://developer.mozilla.org/zh-CN/docs/Glossary/SEO)（搜索引擎优化）方面效果不佳。
* 严重视力障碍者通常不会阅读网页；他们用听力来代替。完成这项工作的软件叫做屏幕阅读器（[screen reader](http://en.wikipedia.org/wiki/Screen\_reader)）。该软件提供了快速访问给定文本内容的方法。在使用的各种技术中，它们通过朗读标题来提供文档的概述，让用户能快速找到他们需要的信息。如果标题不可用，用户将被迫听到整个文档的大声朗读。
* 使用[CSS](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS)样式化内容，或者使用[JavaScript](https://developer.mozilla.org/zh-CN/docs/Glossary/JavaScript)做一些有趣的事情，你需要包含相关内容的元素，所以CSS / JavaScript可以有效地定位它。

因此，我们需要给我们的内容结构标记。

#### [实践操作: 编辑我们的内容结构](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E5%AE%9E%E8%B7%B5%E6%93%8D%E4%BD%9C\_%E7%BC%96%E8%BE%91%E6%88%91%E4%BB%AC%E7%9A%84%E5%86%85%E5%AE%B9%E7%BB%93%E6%9E%84) <a href="#shi-jian-cao-zuo-bian-ji-wo-men-de-nei-rong-jie-gou" id="shi-jian-cao-zuo-bian-ji-wo-men-de-nei-rong-jie-gou"></a>

让我们直接跳进一个实例。在下面的示例中，向“Input”字段中的原始文本添加元素，使其在“Output”字段中显示为标题和两个段落。

如果您犯了错误，您可以使用_重置_按钮进行重置。如果卡住，请按_显示解决方案_按钮以查看答案。

#### [为什么我们需要语义？](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E4%B8%BA%E4%BB%80%E4%B9%88%E6%88%91%E4%BB%AC%E9%9C%80%E8%A6%81%E8%AF%AD%E4%B9%89%EF%BC%9F) <a href="#wei-shen-me-wo-men-xu-yao-yu-yi" id="wei-shen-me-wo-men-xu-yao-yu-yi"></a>

在我们身边的任何地方都要依赖语义学 — 我们依靠以前的经验就知道日常事物都代表什么；当我们看到什么，我们就会知道它代表什么。举个例子, 我们知道红色交通灯表示“停止”，绿色交通灯表示”通行“。 如果运用了错误的语义，事情会迅速地变得非常棘手 (难道有某个国家使用红色代表通行？我不希望如此)

同样的道理，我们需要确保使用了正确的元素来给予内容正确的意思、作用以及外形。在这里，[`<h1>` (en-US)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading\_Elements) 元素也是一个语义元素，它给出了包裹在您的页面上用来表示顶级标题的角色（或意义）的文本。

```
<h1>这是一个顶级标题</h1>
```

Copy to Clipboard

一般来说，浏览器会给它一个更大的字形来让它看上去像个标题（虽然你可以使用CSS让它变成任何你想要的样式。更重要的是，它的语义值将以多种方式被使用，比如通过搜索引擎和屏幕阅读器（上文提到过的）。

在另一方面，你可以让任一元素看起来像一个顶级标题，如下：

```
<span style="font-size: 32px; margin: 21px 0;">这是顶级标题吗？</span>
```

Copy to Clipboard

这是一个 [`<span>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/span) 元素，它没有语义。当您想要对它用CSS（或者JS）时，您可以用它包裹内容，且不需要附加任何额外的意义（在未来的课程中你会发现更多这类元素）。我们已经对它使用了CSS来让它看起来像一个顶级标题。然而，由于它没有语义值，所以它不会有任何上文提到的帮助。最好的方法是使用相关的HTML元素来标记这个项目。

### [列表 Lists](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E5%88%97%E8%A1%A8\_lists) <a href="#lie-biao-lists" id="lie-biao-lists"></a>

现在，让我们学习一下列表。列表在生活中随处可见——从购物清单到回家的路线方案，再到本教程的说明列表。在网络上，列表也随处可见，大致包含了三种不同类型的列表。

#### [无序 Unordered](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E6%97%A0%E5%BA%8F\_unordered) <a href="#wu-xu-unordered" id="wu-xu-unordered"></a>

无序列表用于标记列表项目顺序无关紧要的列表 — 让我们以早点清单为例。

```
豆浆
油条
豆汁
焦圈
```

每份无序的清单从 [`<ul>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ul) 元素开始——需要包裹清单上所有被列出的项目：

```
<ul>
豆浆
油条
豆汁
焦圈
</ul>
```

Copy to Clipboard

然后就是用 [`<li>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/li) 元素把每个列出的项目单独包裹起来：

```
<ul>
  <li>豆浆</li>
  <li>油条</li>
  <li>豆汁</li>
  <li>焦圈</li>
</ul>
```

Copy to Clipboard

**实践操作: 标记无序列表**

尝试编辑下面的示例来创建一个HTML无序列表。

#### [有序 Ordered](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E6%9C%89%E5%BA%8F\_ordered) <a href="#you-xu-ordered" id="you-xu-ordered"></a>

有序列表需要按照项目的顺序列出来——让我们以一组方向为例：

```
沿着条路走到头
右转
直行穿过第一个十字路口
在第三个十字路口处左转
继续走 300 米，学校就在你的右手边
```

这个标记的结构和无序列表一样，除了需要用[`<ol>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ol) 元素将所有项目包裹, 而不是`<ul>：`

```
<ol>
  <li>沿着条路走到头</li>
  <li>右转</li>
  <li>直行穿过第一个十字路口</li>
  <li>在第三个十字路口处左转</li>
  <li>继续走 300 米，学校就在你的右手边</li>
</ol>
```

Copy to Clipboard

**实践操作: 标记有序列表**

尝试编辑下面的示例来创建一个HTML有序列表：

#### [实践操作: 标记我们的食谱](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E5%AE%9E%E8%B7%B5%E6%93%8D%E4%BD%9C\_%E6%A0%87%E8%AE%B0%E6%88%91%E4%BB%AC%E7%9A%84%E9%A3%9F%E8%B0%B1) <a href="#shi-jian-cao-zuo-biao-ji-wo-men-de-shi-pu" id="shi-jian-cao-zuo-biao-ji-wo-men-de-shi-pu"></a>

到了这里，你拥有了所有你需要的信息来标记我们的食谱样例。你可以选择从[text-start.html](https://github.com/mdn/learning-area/blob/master/html/introduction-to-html/html-text-formatting/text-start.html)复制一份文件并保存在本地，打开它进行编辑，或者在下面的例子中进行编辑。因为在本地你可以保存你的项目，所以在本地做这个工作可能更好。而如果你在下面可编辑的样本中作业，下一次你打开这个网站时你可能会丢失你的数据。各有利弊吧。

如果你感到棘手，你可以随时按下_Show solution_按钮，或者在我们的github repo上检查我们的 [text-complete.html](https://github.com/mdn/learning-area/blob/master/html/introduction-to-html/html-text-formatting/text-complete.html) 样例。

#### [嵌套列表 Nesting lists](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E5%B5%8C%E5%A5%97%E5%88%97%E8%A1%A8\_nesting\_lists) <a href="#qian-tao-lie-biao-nestinglists" id="qian-tao-lie-biao-nestinglists"></a>

将一个列表嵌入到另一个列表是完全可以的。 你可能想让一些子项目列在首项目之下。让我们从食谱示例中获取第二个列表：

```
<ol>
  <li>先用蛋白一个、盐半茶匙及淀粉两大匙搅拌均匀，调成“腌料”，鸡胸肉切成约一厘米见方的碎丁并用“腌料”搅拌均匀，腌渍半小时。</li>
  <li>用酱油一大匙、淀粉水一大匙、糖半茶匙、盐四分之一茶匙、白醋一茶匙、蒜末半茶匙调拌均匀，调成“综合调味料”。</li>
  <li>鸡丁腌好以后，色拉油下锅烧热，先将鸡丁倒入锅内，用大火快炸半分钟，炸到变色之后，捞出来沥干油汁备用。</li>
  <li>在锅里留下约两大匙油，烧热后将切好的干辣椒下锅，用小火炒香后，再放入花椒粒和葱段一起爆香。随后鸡丁重新下锅，用大火快炒片刻后，再倒入“综合调味料”继续快炒。</li>
  <li>如果你采用正宗川菜做法，最后只需加入花生米，炒拌几下就可以起锅了。</li>
  <li>如果你在北方，可加入黄瓜丁、胡萝卜丁和花生米，翻炒后起锅。</li>
 </ol>
```

由于最后两项与它们的前一项非常密切相关（它们看起来更像该项的子项或选项），将它们编辑成无序列表，并嵌套在该项的子项中可能更合理。就像下面这样：

```
<ol>
  <li>先用蛋白一个、盐半茶匙及淀粉两大匙搅拌均匀，调成“腌料”，鸡胸肉切成约一厘米见方的碎丁并用“腌料”搅拌均匀，腌渍半小时。</li>
  <li>用酱油一大匙、淀粉水一大匙、糖半茶匙、盐四分之一茶匙、白醋一茶匙、蒜末半茶匙调拌均匀，调成“综合调味料”。</li>
  <li>鸡丁腌好以后，色拉油下锅烧热，先将鸡丁倒入锅内，用大火快炸半分钟，炸到变色之后，捞出来沥干油汁备用。</li>
  <li>在锅里留下约两大匙油，烧热后将切好的干辣椒下锅，用小火炒香后，再放入花椒粒和葱段一起爆香。随后鸡丁重新下锅，用大火快炒片刻后，再倒入“综合调味料”继续快炒。
    <ul>
      <li>如果你采用正宗川菜做法，最后只需加入花生米，炒拌几下就可以起锅了。</li>
      <li>如果你在北方，可加入黄瓜丁、胡萝卜丁和花生米，翻炒后起锅。</li>
    </ul>
  </li>
</ol>
```

Copy to Clipboard

尝试回到上一个实践操作的例子中，并更新第二个列表。

### [重点强调](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E9%87%8D%E7%82%B9%E5%BC%BA%E8%B0%83) <a href="#zhong-dian-qiang-tiao" id="zhong-dian-qiang-tiao"></a>

在日常用语中，我们常常会加重某个字的读音，或者用加粗等方式突出某句话的重点。与此类似，HTML 也提供了相应的标签，用于标记某些文本，使其具有加粗、倾斜、下划线等效果。下面，我们将学习一些最常见的标签。

#### [强调](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E5%BC%BA%E8%B0%83) <a href="#qiang-tiao" id="qiang-tiao"></a>

在口语表达中，我们有时会强调某些字，用来改变这句话的意思。同样地，在书面用语中，我们可以使用斜体字来达到同样的效果。例如，下面两个句子便有不同的意思：

I am glad you weren't late.

I am _glad_ you weren't _late_. (ps: 此句中"_glad"_和"late"为斜体字体)

第一句话听起来真的像松了一口气因为没有迟到。相反，第二句话听起来具有讽刺性而且有隐含的攻击性，表达对一个人迟到的恼怒。

在HTML中我们用[`<em>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/em)（emphasis）元素来标记这样的情况。这样做既可以让文档读起来更有趣，也可以被屏幕阅读器识别出来，并以不同的语调发出。浏览器默认风格为斜体，但你不应该纯粹使用这个标签来获得斜体风格，为了获得斜体风格，你应该使用[`<span>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/span)元素和一些CSS，或者是[`<i>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/i)元素（见下文）。

```
<p>I am <em>glad</em> you weren't <em>late</em>.</p>
```

Copy to Clipboard

#### [非常重要](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E9%9D%9E%E5%B8%B8%E9%87%8D%E8%A6%81) <a href="#fei-chang-zhong-yao" id="fei-chang-zhong-yao"></a>

为了强调重要的词，在口语方面我们往往用重音强调，在文字方面则是用粗体字来达到强调的效果。例如下面这段:

This liquid is **highly toxic**.

I am counting on you. **Do not** be late!

在HTML中我们用[`<strong>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/strong) (strong importance) 元素来标记这样的情况。这样做既可以让文档更加地有用，也可以被屏幕阅读器识别出来，并以不同的语调发出。浏览器默认风格为粗体，但你不应该纯粹使用这个标签来获得粗体风格，为了获得粗体风格，你应该使用[`<span>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/span)元素和一些CSS，或者是 [`<b>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/b) 元素 (见下文)。

```
<p>This liquid is <strong>highly toxic</strong>.</p>

<p>I am counting on you. <strong>Do not</strong> be late!</p>
```

Copy to Clipboard

如有需要你可以将strong元素和em元素嵌套在其他的标签中：

```
<p>This liquid is <strong>highly toxic</strong> —
if you drink it, <strong>you may <em>die</em></strong>.</p>
```

Copy to Clipboard

#### [实践操作: 我们是重要的!](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E5%AE%9E%E8%B7%B5%E6%93%8D%E4%BD%9C\_%E6%88%91%E4%BB%AC%E6%98%AF%E9%87%8D%E8%A6%81%E7%9A%84!) <a href="#shi-jian-cao-zuo-wo-men-shi-zhong-yao-de" id="shi-jian-cao-zuo-wo-men-shi-zhong-yao-de"></a>

在这个实践操作中，我们提供了可编辑的例子。在这个例子中，我们想让你把斜体(em)和加粗(strong)放在你认为重要的词汇上，仅仅为了练习。

#### [斜体字、粗体字、下划线...](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E6%96%9C%E4%BD%93%E5%AD%97%E3%80%81%E7%B2%97%E4%BD%93%E5%AD%97%E3%80%81%E4%B8%8B%E5%88%92%E7%BA%BF...) <a href="#xie-ti-zi-cu-ti-zi-xia-hua-xian-..." id="xie-ti-zi-cu-ti-zi-xia-hua-xian-..."></a>

迄今为止我们已经讨论的元素都是意义清楚的语义元素。[`<b>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/b), [`<i>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/i), 和 [`<u>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/u) 的情况却有点复杂。它们出现于人们要在文本中使用粗体、斜体、下划线但CSS仍然不被完全支持的时期。像这样的元素，仅仅影响表象而且没有语义，被称为**表象元素（presentational elements）**并且不应该再被使用。因为正如我们在之前看到的，语义对可访问性，SEO（搜索引擎优化）等非常重要。

HTML5用新的语义规则重新定义了`<b>`,`<i>`和`<u>`,使得它们的语言显得稍微有点混乱。

这里是最好的经验法则：如果没有更合适的元素，那么使用 `<b>`、`<i>` 或 `<u>` 来表达传统上的粗体、斜体或下划线表达的意思是合适的。然而，始终拥有[可访问性](https://developer.mozilla.org/zh-CN/docs/learn/Accessibility)的思维模式是至关重要的。斜体的概念对人们使用屏幕阅读器是没有帮助的，对使用其他书写系统而不是拉丁文书写系统的人们也是没有帮助的。

* [`<i>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/i) 被用来传达传统上用斜体表达的意义：外国文字，分类名称，技术术语，一种思想……
* [`<b>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/b) 被用来传达传统上用粗体表达的意义：关键字，产品名称，引导句……
* [`<u>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/u) 被用来传达传统上用下划线表达的意义：专有名词，拼写错误……

使用下划线的忠告：因为我们常常会认为网页中的下划线代表着一个超链接**，**所以最好只用下划线来代表超链接。而在语义适合的情况下不得不使用\<u>元素时，可以使用CSS来改变\<u>元素对应的下划线的默认样式，从而和超链接的下划线区分开来。下面是一个具体的例子：

```
<!-- 学名 -->
<p>
  红喉北蜂鸟（学名：<i>Archilocus colubris</i>）
  是北美东部最常见的蜂鸟品种。
</p>

<!-- 舶来词 -->
<p>
  菜单上有好多舶来词汇，比如 <i lang="uk-latn">vatrushka</i>（东欧乳酪面包）,
  <i lang="id">nasi goreng</i>（印尼炒饭）以及<i lang="fr">soupe à l'oignon</i>（法式洋葱汤）。
</p>

<!-- 已知的错误书写 -->
<p>
  总有一天我会改掉写<u style="text-decoration-line: underline; text-decoration-style: wavy;">措字</u>的毛病。
</p>

<!-- 在一组指令中突出显示关键字 -->
<ol>
  <li>
    <b>切</b>下两片面包，
  </li>
  <li>
    在两片面包中间<b>夹入</b>一片西红柿和一片生菜叶。
  </li>
</ol>
```

### [总结](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction\_to\_HTML/HTML\_text\_fundamentals#%E6%80%BB%E7%BB%93) <a href="#zong-jie" id="zong-jie"></a>

至此，本文应该给您做了一个很好的了解，如何开始在HTML中标记文本，并介绍了一些最重要的元素。在这一领域还有许多语义元素，我们将在后面的“更多语义元素”文章中看到更多的语义元素。 在下一篇文章中，我们将详细介绍如何创建超链接（[create hyperlinks](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction\_to\_HTML/Creating\_hyperlinks)），它可能是Web上最重要的元素。
