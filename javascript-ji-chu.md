---
description: >-
  JavaScript 是一门编程语言，可为网站添加交互功能（例如：游戏、动态样式、动画以及在按下按钮或收到表单数据时做出的响应等）。本文介绍了
  JavaScript 的精彩之处和主要用途。
---

# JavaScript基础

### [JavaScript 到底是什么？](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#javascript\_%E5%88%B0%E5%BA%95%E6%98%AF%E4%BB%80%E4%B9%88%EF%BC%9F) <a href="#javascript-dao-di-shi-shen-me" id="javascript-dao-di-shi-shen-me"></a>

[JavaScript](https://developer.mozilla.org/zh-CN/docs/Glossary/JavaScript)（缩写：JS）是一门完备的 [动态编程语言](https://developer.mozilla.org/zh-CN/docs/Glossary/Dynamic\_programming\_language)。当应用于 [HTML](https://developer.mozilla.org/zh-CN/docs/Glossary/HTML) 文档时，可为网站提供动态交互特性。由布兰登·艾克（ Brendan Eich，Mozilla 项目、Mozilla 基金会和 Mozilla 公司的联合创始人）发明。

JavaScript 的应用场合极其广泛，简单到幻灯片、照片库、浮动布局和响应按钮点击，复杂到游戏、2D/3D 动画、大型数据库驱动程序等等。

JavaScript 相当简洁，却非常灵活。开发者们基于 JavaScript 核心编写了大量实用工具，可以使 开发工作事半功倍。其中包括：

* 浏览器应用程序接口（[API](https://developer.mozilla.org/zh-CN/docs/Glossary/API)）—— 浏览器内置的 API 提供了丰富的功能，比如：动态创建 HTML 和设置 CSS 样式、从用户的摄像头采集处理视频流、生成3D 图像与音频样本等等。
* 第三方 API —— 让开发者可以在自己的站点中整合其它内容提供者（Twitter、Facebook 等）提供的功能。
* 第三方框架和库 —— 用来快速构建网站和应用。

本节是一篇 JavaScript 简介，因此这个阶段不会对 JavaScript 语言和上述工具做过多的介绍。之后可以到 [JavaScript 学习区](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript) 和 MDN 的其它地方学习更多细节。

下面对语言核心做一个不完整介绍，期间还可以接触到一些浏览器 API 特性。

### [“Hello World!”示例](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E2%80%9Chello\_world!%E2%80%9D%E7%A4%BA%E4%BE%8B) <a href="#helloworld-shi-li" id="helloworld-shi-li"></a>

读到这里你一定很激动，诚然 —— JavaScript 是最振奋人心的 Web 技术之一，而且在娴熟驾驭之后，你的网站在功能和创新力上将达到一个新的维度。

然而，JavaScript 比 HTML 和 CSS 学习起来更加复杂一点，所以必须一步一个脚印地学习。首先，来看看如何在页面中添加一些基本的 JavaScript 脚本来建造一个 “Hello world!” 示例（[一切始于 Hello World](https://zh.wikipedia.org/wiki/Hello\_World)）。

**重要：**如果你没有完成之前的课程实践，可下载 [上一章节示例的压缩包](https://github.com/roy-tian/learning-area/raw/master/extras/getting-started-web/beginner-html-site-styled.zip) 并在本地解压作出发点。

1. 首先，打开你的测试站点，创建一个名为 `scripts` 的文件夹。然后在其中创建一个名为 main.js 的文件。
2.  下一步，在 `index.html` 文件\</body> 标签前的新行添加以下代码。

    ```
    <script src="scripts/main.js" defer></script>
    ```

    Copy to Clipboard
3. 与 CSS 的 [`<link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link) 元素类似，它将 JavaScript 引入页面以作用于 HTML（以及 CSS 等页面上所有内容）：
4.  现在将以下代码添加到 `main.js` 文件中：

    ```
    let myHeading = document.querySelector('h1');
    myHeading.textContent = 'Hello world!';
    ```

    Copy to Clipboard
5. 最后，保存 HTML 和 JavaScript 文件，用浏览器打开 `index.html`。可以看到如下内容：![](https://mdn.mozillademos.org/files/9543/hello-world.png)

**注：**我们将 [`<script>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script) 放在HTML文件的底部附近的原因是浏览器会按照代码在文件中的顺序加载 HTML。如果先加载的 JavaScript 期望修改其下方的 HTML，那么它可能由于 HTML 尚未被加载而失效。因此，将 JavaScript 代码放在 HTML页面的底部附近通常是最好的策略。

#### [发生了什么？](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E5%8F%91%E7%94%9F%E4%BA%86%E4%BB%80%E4%B9%88%EF%BC%9F) <a href="#fa-sheng-le-shen-me" id="fa-sheng-le-shen-me"></a>

JavaScript 把页面的标题改成了 “Hello world!” 。首先用 [`querySelector()`](https://developer.mozilla.org/zh-CN/docs/Web/API/Document/querySelector) 函数获取标题的引用，并把它储存在 `myHeading` 变量中。这与 CSS 选择器的用法非常相像：若要对某个元素进行操作，首先得选择它。

之后，把 `myHeading` 变量的属性 [`textContent`](https://developer.mozilla.org/zh-CN/docs/Web/API/Node/textContent) （标题内容）修改为 “Hello world!” 。

**注：**上面用到的两个函数都来自 [文档对象模型 (DOM) API](https://developer.mozilla.org/zh-CN/docs/Web/API/Document\_Object\_Model)， 均用于控制文档。

### [JavaScript 快速入门](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#javascript\_%E5%BF%AB%E9%80%9F%E5%85%A5%E9%97%A8) <a href="#javascript-kuai-su-ru-men" id="javascript-kuai-su-ru-men"></a>

我们来学习一些 JavaScript 的核心特性，从而更好地理解它的运行机制。学习这些知识很有意义，因为这些原理普遍适用于所有编程语言，掌握好它们，可以做到融会贯通。

**重要：**学习本节时，请尝试将示例代码输入到 JavaScript 控制台里看看会发生什么。 JavaScript 控制台的更多信息请查看 [浏览器开发者工具](https://developer.mozilla.org/zh-CN/docs/Learn/Common\_questions/What\_are\_browser\_developer\_tools)。

#### [变量（Variable）](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E5%8F%98%E9%87%8F%EF%BC%88variable%EF%BC%89) <a href="#bian-liang-variable" id="bian-liang-variable"></a>

[变量 (en-US)](https://developer.mozilla.org/en-US/docs/Glossary/Variable) 是存储值的容器。要声明一个变量，先输入关键字 `let` 或 `var`，然后输入合适的名称：

```
let myVariable;
```

Copy to Clipboard

**注：**行末的分号表示当前语句结束，不过只有在单行内需要分割多条语句时，这个分号才是必须的。然而，一些人认为每条语句末尾加分号是一种好的风格。分号使用规则的更多细节请参阅 [JavaScript 分号使用指南](http://news.codecademy.com/your-guide-to-semicolons-in-javascript/)（英文页面）。

**注：**几乎任何内容都可以作为变量名，但还是有一些限制（请参阅 [变量命名规则](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Grammar\_and\_types#%e5%8f%98%e9%87%8f)）。如果你不确定，还可以 [验证变量名](https://mothereff.in/js-variables) 是否有效。

**注：**JavaScript 对大小写敏感，`myVariable` 和 `myvariable` 是不同的。如果代码出现问题了，先检查一下大小写！

**注：**想要了解更多关于 `var` 和 `let` 的不同点，可以参阅 [var 与 let 的区别](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First\_steps/Variables#var\_%E4%B8%8E\_let\_%E7%9A%84%E5%8C%BA%E5%88%AB)。

变量定义后可以进行赋值：

```
myVariable = '李雷';
```

Copy to Clipboard

也可以将定义、赋值操作写在同一行：

```
let myVariable = '李雷';
```

Copy to Clipboard

可以直接通过变量名取得变量的值：

```
myVariable;
```

Copy to Clipboard

变量在赋值后是可以更改的：

```
let myVariable = '李雷';
myVariable = '韩梅梅';
```

注意变量可以有不同的 [数据类型](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Data\_structures) ：

| 变量                                                                   | 解释                                            | 示例                                                                                                                             |
| -------------------------------------------------------------------- | --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| [String](https://developer.mozilla.org/zh-CN/docs/Glossary/String)   | 字符串（一串文本）：字符串的值必须用引号（单双均可，必须成对）扩起来。           | `let myVariable = '李雷';`                                                                                                       |
| [Number](https://developer.mozilla.org/zh-CN/docs/Glossary/Number)   | 数字：无需引号。                                      | `let myVariable = 10;`                                                                                                         |
| [Boolean](https://developer.mozilla.org/zh-CN/docs/Glossary/Boolean) | 布尔值（真 / 假）： `true`/`false` 是 JS 里的特殊关键字，无需引号。 | `let myVariable = true;`                                                                                                       |
| [Array](https://developer.mozilla.org/zh-CN/docs/Glossary/array)     | 数组：用于在单一引用中存储多个值的结构。                          | <p><code>let myVariable = [1, '李雷', '韩梅梅', 10];</code><br>元素引用方法：<code>myVariable[0]</code>, <code>myVariable[1]</code> ……</p> |
| [Object](https://developer.mozilla.org/zh-CN/docs/Glossary/Object)   | 对象：JavaScript 里一切皆对象，一切皆可储存在变量里。这一点要牢记于心。     | <p><code>let myVariable = document.querySelector('h1');</code><br>以及上面所有示例都是对象。</p>                                            |

那么变量有什么用呢？我们说，编程时它们无所不在。如果值无法改变，那么就无法做任何动态的工作，比如发送个性化的问候，或是改变在图片库当前展示的图片。

#### [注释](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E6%B3%A8%E9%87%8A) <a href="#zhu-shi" id="zhu-shi"></a>

类似于 CSS，JavaScript 中可以添加注释。

```
/*
这里的所有内容
都是注释。
*/
```

Copy to Clipboard

如果注释只有一行，可以更简单地将注释放在两个斜杠之后，就像这样：

```
// 这是一条注释。
```

Copy to Clipboard

#### [运算符](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E8%BF%90%E7%AE%97%E7%AC%A6) <a href="#yun-suan-fu" id="yun-suan-fu"></a>

[运算符 (en-US)](https://developer.mozilla.org/en-US/docs/Glossary/Operator) 是一类数学符号，可以根据两个值（或变量）产生结果。以下表格中介绍了一些最简单的运算符，可以在浏览器控制台里尝试一下后面的示例。

**译注：**这里说“根据**两个**值（或变量）产生结果”是不严谨的，计算两个变量的运算符称为“二元运算符”，还有一元运算符和三元运算符，下表中的“取非”就是一元运算符。

| 运算符   | 解释                                              | 符号            | 示例                                                                                                                        |
| ----- | ----------------------------------------------- | ------------- | ------------------------------------------------------------------------------------------------------------------------- |
| 加     | 将两个数字相加，或拼接两个字符串。                               | `+`           | <p><code>6 + 9;</code><br><code>"Hello " + "world!";</code></p>                                                           |
| 减、乘、除 | 这些运算符操作与基础算术一致。只是乘法写作星号，除法写作斜杠。                 | `-`, `*`, `/` | <p><code>9 - 3;</code><br><code>8 * 2; //乘法在JS中是一个星号</code><br><code>9 / 3;</code></p>                                    |
| 赋值运算符 | 为变量赋值（你之前已经见过这个符号了）                             | `=`           | `let myVariable = '李雷';`                                                                                                  |
| 等于    | 测试两个值是否相等，并返回一个 `true`/`false` （布尔）值。           | `===`         | <p><code>let myVariable = 3;</code><br><code>myVariable === 4; // false</code></p>                                        |
| 不等于   | 和等于运算符相反，测试两个值是否不相等，并返回一个 `true`/`false` （布尔）值。 | `!==`         | <p><code>let myVariable = 3;</code><br><code>myVariable !== 3; // false</code></p>                                        |
| 取非    | 返回逻辑相反的值，比如当前值为真，则返回 `false`。                   | `!`           | <p>原式为真，但经取非后值为 <code>false</code>：<br><code>let myVariable = 3;</code><br><code>!(myVariable === 3); // false</code></p> |

运算符种类远不止这些，不过目前上表已经够用了。完整列表请参阅 [表达式和运算符](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators)。

**注：**不同类型数据之间的计算可能出现奇怪的结果，因此必须正确引用变量，才能得出预期结果。比如在控制台输入 `"35" + "25"`，为什么不能得到 `60`？因为引号将数字转换成了字符串，所以结果是连接两个字符串而不是把两个数字相加。输入 `35 + 25` 才能得到正确结果。

#### [条件语句](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E6%9D%A1%E4%BB%B6%E8%AF%AD%E5%8F%A5) <a href="#tiao-jian-yu-ju" id="tiao-jian-yu-ju"></a>

条件语句是一种代码结构，用来测试表达式的真假，并根据测试结果运行不同的代码。一个常用的条件语句是 `if ... else`。下面是一个示例：

```
let iceCream = 'chocolate';
if (iceCream === 'chocolate') {
  alert('我最喜欢巧克力冰激淋了。');
} else {
  alert('但是巧克力才是我的最爱呀……');
}
```

Copy to Clipboard

`if ( ... )` 中的表达式进行测试，用（上文所提到的）等于运算符来比较变量 `iceCream` 与字符串 `'chocolate'` 是否相等。 如果返回 `true`，则运行第一个代码块；如果返回 `false`，则跳过第一块直接运行 `else` 之后的第二个代码块。

#### [函数（Function）](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E5%87%BD%E6%95%B0%EF%BC%88function%EF%BC%89) <a href="#han-shu-function" id="han-shu-function"></a>

[函数](https://developer.mozilla.org/zh-CN/docs/Glossary/Function) 用来封装可复用的功能。如果没有函数，一段特定的操作过程用几次就要重复写几次，而使用函数则只需写下函数名和一些简短的信息。之前已经涉及过一些函数，比如：

1.  ```
    let myVariable = document.querySelector('h1');
    ```

    Copy to Clipboard
2.  ```
    alert('hello!');
    ```

    Copy to Clipboard

`document.querySelector` 和 `alert` 是浏览器内置的函数，随时可用。

如果代码中有一个类似变量名后加小括号 `()` 的东西，很可能就是一个函数。函数通常包括[参数](https://developer.mozilla.org/zh-CN/docs/Glossary/Argument)，参数中保存着一些必要的数据。它们位于括号内部，多个参数之间用逗号分开。

比如， `alert()` 函数在浏览器窗口内弹出一个警告框，还应为其提供一个字符串参数，以告诉它警告框里要显示的内容。

好消息是：人人都能定义自己的函数。下面的示例是为两个参数进行乘法运算的函数：

```
function multiply(num1, num2) {
  let result = num1 * num2;
  return result;
}
```

Copy to Clipboard

尝试在控制台运行这个函数，不妨多试几组参数，比如：

```
multiply(4, 7);
multiply(20, 20);
multiply(0.5, 3);
```

Copy to Clipboard

**注：**[`return`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/return) 语句告诉浏览器当前函数返回 `result` 变量。这是一点很有必要，因为函数内定义的变量只能在函数内使用。这叫做变量的 [作用域](https://developer.mozilla.org/zh-CN/docs/Glossary/Scope)。（详见 [变量作用域](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Values,\_variables,\_and\_literals#Variable\_scope)。）

#### [事件](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E4%BA%8B%E4%BB%B6) <a href="#shi-jian" id="shi-jian"></a>

事件能为网页添加真实的交互能力。它可以捕捉浏览器操作并运行一些代码做为响应。最简单的事件是 [点击事件](https://developer.mozilla.org/zh-CN/docs/Web/API/Element/click\_event)，鼠标的点击操作会触发该事件。 可尝试将下面的代码输入到控制台，然后点击页面的任意位置：

```
document.querySelector('html').onclick = function() {
    alert('别戳我，我怕疼。');
}
```

Copy to Clipboard

将事件与元素绑定有许多方法。在这里选用了 [`<html>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/html) 元素，把一个匿名函数（就是没有命名的函数，这里的匿名函数包含单击鼠标时要运行的代码）赋值给了 `html` 的 [`onclick (en-US)`](https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers/onclick) 属性。

请注意：

```
document.querySelector('html').onclick = function() {};
```

Copy to Clipboard

等价于

```
let myHTML = document.querySelector('html');
myHTML.onclick = function() {};
```

Copy to Clipboard

只是前者更简洁。

### [完善示例网页](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E5%AE%8C%E5%96%84%E7%A4%BA%E4%BE%8B%E7%BD%91%E9%A1%B5) <a href="#wan-shan-shi-li-wang-ye" id="wan-shan-shi-li-wang-ye"></a>

现在你已经具备了一些 JavaScript 基础，下面来为示例网页添加一些更酷的特性。

#### [添加一个图像切换器](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E6%B7%BB%E5%8A%A0%E4%B8%80%E4%B8%AA%E5%9B%BE%E5%83%8F%E5%88%87%E6%8D%A2%E5%99%A8) <a href="#tian-jia-yi-ge-tu-xiang-qie-huan-qi" id="tian-jia-yi-ge-tu-xiang-qie-huan-qi"></a>

这里将用新的 DOM API 为网页添加另一张图片，并用 JavaScript 使图片在点击时进行切换。

1. 首先，找到另一张你想要在你的页面上展示的图片，且尺寸与第一张图片尽可能相同。
2. 将这张图片储存在你的`images`目录下。
3. 将图片重命名为'firefox2.png'（去掉引号）。
4.  打开 `main.js` 文件，输入下面的 JavaScript 代码 ( 请删除刚才的 "hello world" 脚本)：

    ```
    let myImage = document.querySelector('img');

    myImage.onclick = function() {
        let mySrc = myImage.getAttribute('src');
        if(mySrc === 'images/firefox-icon.png') {
          myImage.setAttribute('src', 'images/firefox2.png');
        } else {
          myImage.setAttribute('src', 'images/firefox-icon.png');
        }
    }
    ```

    Copy to Clipboard
5. 保存所有文件并用浏览器打开 `index.html` 。点击图片可以发现它能够切换了！

这里首先把 [`<img>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/img) 元素的引用存放在 `myImage` 变量里。然后将这个变量的 `onclick` 事件与一个匿名函数绑定。每次点击图片时：

1. 获取这张图片的 `src` 属性值。
2. 用一个条件句来判断 `src` 的值是否等于原始图像的路径:
   1. 如果是，则将 `src` 的值改为第二张图片的路径，并在 [`<img>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/img) 内加载该图片。
   2. 如果不是（意味着它已经修改过）, 则把 `src` 的值重新设置为原始图片的路径，即原始状态。

#### [添加个性化欢迎信息](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E6%B7%BB%E5%8A%A0%E4%B8%AA%E6%80%A7%E5%8C%96%E6%AC%A2%E8%BF%8E%E4%BF%A1%E6%81%AF) <a href="#tian-jia-ge-xing-hua-huan-ying-xin-xi" id="tian-jia-ge-xing-hua-huan-ying-xin-xi"></a>

下面来添加另一段代码，在用户初次进入站点时将网页的标题改成一段个性化欢迎信息（即在标题中添加用户的名字）。名字信息会由 [Web Storage API](https://developer.mozilla.org/zh-CN/docs/Web/API/Web\_Storage\_API) 保存下来，即使用户关闭页面之后再重新打开，仍可得到之前的信息。还会添加一个选项，可以根据需要改变用户名字以更新欢迎信息。

1.  打开 `index.html`， 在 [`<script>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script) 标签**前**添加以下代码，将在页面底部显示一个“切换用户”字样的按钮：

    ```
    <button>切换用户</button>
    ```

    Copy to Clipboard
2.  将以下 JavaScript 代码原封不动添加到 `main.js` 文件底部，将获取新按钮和标题的引用，并保存至变量中：

    ```
    let myButton = document.querySelector('button');
    let myHeading = document.querySelector('h1');
    ```

    Copy to Clipboard
3.  然后添加以下函数来设置个性化欢迎信息。（函数需要在调用后生效，下文中提供了两种对该函数的调用方式）

    ```
    function setUserName() {
      let myName = prompt('请输入你的名字。');
      localStorage.setItem('name', myName);
      myHeading.textContent = 'Mozilla 酷毙了，' + myName;
    }
    ```

    Copy to Clipboard该函数首先调用了 [`prompt()`](https://developer.mozilla.org/zh-CN/docs/Web/API/Window/prompt) 函数， 与 `alert()` 类似会弹出一个对话框。但是这里需要用户输入数据，并在确定后将数据存储在 `myName` 变量里。接下来将调用 [`localStorage`](https://developer.mozilla.org/zh-CN/docs/Web/API/Window/localStorage) API ，它可以将数据存储在浏览器中供后续获取。这里用 `localStorage` 的 `setItem()` 函数来创建一个`'name'` 数据项，并把 `myName` 变量复制给它。最后将 `textContent` 属性设置为一个欢迎字符串加上这个新设置的名字。
4.  接下来，添加以下的 `if ... else` 块。我们可以称之为初始化代码，因为它在页面初次读取时进行构造工作：

    ```
    if(!localStorage.getItem('name')) {
      setUserName();
    } else {
      let storedName = localStorage.getItem('name');
      myHeading.textContent = 'Mozilla 酷毙了，' + storedName;
    }
    ```

    Copy to Clipboard这里首次使用了取非运算符（逻辑非，用 `!` 表示）来检测 `'name'` 数据是否存在。若不存在，调用 `setUserName()` 创建。若存在（即用户上次访问时设置过），调用 `getItem()` 获取保存的名字，像上文的 `setUserName()` 那样设置 `textContent`。
5.  最后，为按钮设置 onclick 事件处理器。按钮按下时运行 setUserName() 函数。这样用户就可以通过按这个按钮来自由设置新名字了：

    ```
    myButton.onclick = function() {
       setUserName();
    }
    ```

    Copy to Clipboard

第一次访问网页时，页面将询问用户名并发出一段个性化的信息。可随时点击按钮来改变用户名 。告诉你一个额外的福利，因为用户名是保存在 `localStorage` 里的，网页关闭后也不会丢失，所以重新打开浏览器时所设置的名字信息将依然存在:)

#### [用户名为 null?](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E7%94%A8%E6%88%B7%E5%90%8D%E4%B8%BA\_null) <a href="#yong-hu-ming-wei-null" id="yong-hu-ming-wei-null"></a>

运行示例代码，弹出输入用户名的对话框，试着按下 取消 按钮。此时标题会显示为 “Mozilla 酷毙了，null”。这是因为取消提示对话框后值将设置为 `null`，这是 JavaScript 中的一个特殊值，表示引用不存在。

也可以不输入任何名字直接按 确认，你的标题会显示为“Mozilla 酷毙了，”，原因么显而易见。

要避免这些问题，应该更新 `setUserName()` 来检查用户是否输入了 `null` 或者空名字：

```
function setUserName() {
  let myName = prompt('请输入你的名字。');
  if(!myName || myName === null) {
    setUserName();
  } else {
    localStorage.setItem('name', myName);
    myHeading.innerHTML = 'Mozilla 酷毙了，' + myName;
  }
}
```

Copy to Clipboard

用人话说就是：如果 `myName` 没有值或值为 `null`，就再次从头运行`setUserName()`。如果有值（上面的表达式结果不为真），就把值存储到 `localStorage` 并且设置标题。

### [小结](https://developer.mozilla.org/zh-CN/docs/Learn/Getting\_started\_with\_the\_web/JavaScript\_basics#%E5%B0%8F%E7%BB%93) <a href="#xiao-jie" id="xiao-jie"></a>

如果你按部就班完成本文的实践，那么最终可以得到以下页面 （可以 [查看我们的版本](https://roy-tian.github.io/learning-area/extras/getting-started-web/beginner-html-site-scripted/)）：

![测试页面，添加了 一个 js 脚本，可以显示用户名、更改 Firefox 图片。](https://mdn.mozillademos.org/files/16484/beginner-site-scripted.png)

若遇到问题，可以参考 GitHub 上的 [完整示例代码](https://github.com/roy-tian/learning-area/tree/master/extras/getting-started-web/beginner-html-site-scripted) 进行对比。

本章介绍的 JavaScript 知识非常有限，更多内容请访问 [Javascript 学习页面](https://developer.mozilla.org/zh-CN/docs/learn/JavaScript)。
