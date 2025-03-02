## HTML

### 动态网页编程技术

常见的动态网页编程技术有 `JSP`、`ASP.NET`、`PHP` 等等。

- JSP（Java Server Pages），由普通的 HTML 与 基于 Java 语言的嵌入标记组成。
- ASP（Active Server Pages），首选语言是 C# 和 VB.NET。
- PHP（Personal Home Pages / Hypertext Preprocessor），HTML 内嵌语言。



### WEB 特性

- **跨浏览器兼容性**（Cross-browser compatibility）是一种确保你的网页能够在尽可能多的设备上运行的实践。这包括使用所有浏览器都支持的技术，为能提供这些功能（渐进增强）的浏览器提供更好的体验，和/或编写在较旧的浏览器中能回退到更简单但仍可用的体验（平稳降级）的代码。它还涉及大量测试，以查看某些浏览器是否有任何故障，然后进行更多工作来修复这些故障。
- **响应式 Web 设计**（Responsive Web design）是一种使功能和布局变得灵活的实践，这样它们可以自动适应不同的浏览器。一个明显的例子是在桌面上的宽屏浏览器中以一种方式进行布局、但在手机浏览器中以另一种更紧凑的单列布局的网站。现在请尝试调整浏览器窗口的宽度，然后看看会发生什么。
- **性能**（Performance）意味着要尽快加载网站，而且还应使其直观易用，以使用户不会碰壁离开。
- **无障碍**（Accessibility）意味着使你的网站可供尽可能多的不同类型的人使用（相关概念是多样性和包容性，以及包容性设计）。这包括视力障碍，听力障碍，认知障碍或肢体障碍的人。它也不仅仅局限于残疾人——也包含年轻人或老年人、来自不同文化的人、使用移动设备的人、或网络连接不可靠或缓慢的人。
- **国际化**（Internationalization）意味着使网站可以供来自不同文化背景、讲着不同语言的人使用。这一点可以考虑一些技术手段（例如，更改布局以使其对于从右到左甚至垂直的语言仍然可以正常使用）和人为手段（例如，使用简单的非俚语，以便使以你的语言作为第二或第三语言的人更可能理解你的文字）。
- **隐私与安全**（Privacy & Security）这两个概念相关但不同。隐私是指允许人们私下从事其业务，而不是监视他们或收集你绝对不需要的更多数据。安全性是指以安全的方式构建你的网站，以使恶意用户无法从你或你的用户那里窃取信息。



### HTML 的语法结构

`<h1 class="primary">Example Heading</h1>` 语句中，`class="primary"` 是一个特性组，它是一个键值对，常见的特性组有：

- 核型特性组：如 `class`、`id`、`style` 以及 `title` 特性。
- 国际化特性：如 `dir` 和 `lang` 特性。
  - `dir` 允许指定浏览器中文本的特性，比如 `ltr` 和 `rtl` 用来指定文本的阅读方向。
  - `lang` 与 `<html>` 一起使用，作用是告知用户当前网页的语言。
- 辅助访问特性：如 `accesskey` 和 `tabindex` 特性。



### HTML 特殊含义字符

| 原义字符 | 等价字符引用 |
| :------- | :----------- |
| <        | `&lt;`       |
| >        | `&gt;`       |
| "        | `&quot;`     |
| '        | `&apos;`     |
| &        | `&amp;`      |



### HTML 的元信息

元数据的作用主要是在搜索时，可以多样化地展示网站的信息，也便于用户进行索引。

```html
<html>
    <head>
        <meta charset="UTF-8">
        <meta name="author" content="Yikuanzz">
        <meta name="description" content="Test meat.">
    </head>
</html>
```



### HTML 添加网站图标

页面添加网站图标的方式：

- 1、将 16 像素的图片以 `.ico` 格式保存；
- 2、在 `<head>` 中引用 `<link rel="icon" href="favicon.ico" type="image/x-icon">`。

当然，我们可能需要为不同设备来设置不同大小的图标：

```html
<!-- 含有高分辨率 Retina 显示屏的 iPad Pro：-->
<link
  rel="apple-touch-icon"
  sizes="167x167"
  href="/apple-touch-icon-167x167.png" />
<!-- 三倍分辨率的 iPhone：-->
<link
  rel="apple-touch-icon"
  sizes="180x180"
  href="/apple-touch-icon-180x180.png" />
<!-- 没有 Retina 的 iPad、iPad mini 等：-->
<link
  rel="apple-touch-icon"
  sizes="152x152"
  href="/apple-touch-icon-152x152.png" />
<!-- 二倍分辨率的 iPhone 和其他设备：-->
<link rel="apple-touch-icon" href="/apple-touch-icon-120x120.png" />
<!-- 基本图标 -->
<link rel="icon" href="/favicon.ico" />
```



### HTML 引入CSS和JS

用 `link` 来引入 `CSS`：

```html
<link rel="text/css" href="styles.css" />
```

用 `script` 来引入 `JavaScript`：

```html
<script src="script.js"></script>
```



### HTML 网页基本组成

网页基本组成包括：页眉、导航栏、主内容、侧边栏、页脚（可通过提供快速访问链接进行 SEO）。

- 1、记住这些通用的语义元素，`<main>` 、`<artical>`、`<section>`、`<aside>`、`<header>`、`<nav>`、`<footer>`。
- 2、为页面绘制草图，记录每一块区域的租用。
- 3、对期望加进到站点的所有内容进行头脑风暴并罗列出来。
- 4、对内容进行分组，规划要放在哪些页面内。
- 5、绘制站点草图，从主页开始联系到不同的页面。



### HTML 换行和分割线

`<br>`：换行元素。

`<hr>`：分隔线。



### HTML 文本格式处理

除了 `<ul>` 无序列表和 `<ol>` 有序列表外，还有第三种列表就是 `<dl>` 描述列表。

```html
<dl>
  <dt>内心独白</dt>
  <dd>
    戏剧中，某个角色对自己的内心活动或感受进行念白表演，这些台词只面向观众，而其他角色不会听到。
  </dd>
  <dt>语言独白</dt>
  <dd>
    戏剧中，某个角色把自己的想法直接进行念白表演，观众和其他角色都可以听到。
  </dd>
  <dt>旁白</dt>
  <dd>
    戏剧中，为渲染幽默或戏剧性效果而进行的场景之外的补充注释念白，只面向观众，内容一般都是角色的感受、想法、以及一些背景信息等。
  </dd>
</dl>
```



如果想要标记计算机代码，可以用这些标签：

- `<code>`：用于标记计算机通用代码。

- `<pre>`：用于保留空白字符（通常用于代码块）——如果文本中使用了缩进或多余的空白，浏览器将忽略它，你将不会在呈现的页面上看到它。但是，如果你将文本包含在 ` <pre></pre>` 标签中，那么空白将会以与你在文本编辑器中看到的相同的方式渲染出来。
- `<var>`：用于标记具体变量名。
- `<kbd>`：用于标记输入电脑的键盘（或其他类型）输入。
- `<samp>`：用于标记计算机程序的输出。

```html
<pre><code>const para = document.querySelector('p');

para.onclick = function() {
  alert('噢，噢，噢，别点我了。');
}</code></pre>

<pre>$ <kbd>ping mozilla.org</kbd>
<samp>PING mozilla.org (63.245.215.20): 56 data bytes
64 bytes from 63.245.215.20: icmp_seq=0 ttl=40 time=158.233 ms</samp></pre>
```



用 `<time>` 标签来表示时间，这样更加清晰。

```html
<!-- 标准简单日期 -->
<time datetime="2016-01-20">20 January 2016</time>
<!-- 只包含年份和月份-->
<time datetime="2016-01">January 2016</time>
<!-- 只包含月份和日期 -->
<time datetime="01-20">20 January</time>
<!-- 只包含时间，小时和分钟数 -->
<time datetime="19:30">19:30</time>
<!-- 还可包含秒和毫秒 -->
<time datetime="19:30:01.856">19:30:01.856</time>
<!-- 日期和时间 -->
<time datetime="2016-01-20T19:30">7.30pm, 20 January 2016</time>
<!-- 含有时区偏移值的日期时间 -->
<time datetime="2016-01-20T19:30+01:00"
  >7.30pm, 20 January 2016 is 8.30pm in France</time
>
<!-- 提及特定周 -->
<time datetime="2016-W04">The fourth week of 2016</time>

```



### HTML  超链接

如果有需要作为链接的图片，使用 `<a>` 元素来包裹要引用图片的 `<img> `元素：

```html
<a href="https://www.baidu.com" title="百度搜索">
	<img src="baidu.svg" alt="百度一下"/>
</a>
```



超链接除了可以链接到网址、文档外，还可以链接到文档的特定片段：

```html
<!-- contact.html -->
<p>本页面底部可以找到<a href="#Mailing_address">公司邮寄地址</a>。</p>
<h2 id="Mailing_address">邮寄地址</h2>

<!-- index.html -->
<p>
  要提供意见和建议，请将信件邮寄至<a href="contacts.html#Mailing_address">我们的地址</a>。
</p>
```



当你链接到要下载的资源而不是在浏览器中打开时，你可以使用 `download` 属性来提供一个默认的保存文件名。

```html
<a
  href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=zh-CN"
  download="firefox-latest-64bit-installer.exe">
  下载最新的 Firefox 中文版 - Windows（64 位）
</a>
```



用 `<a>` 和 `mailto:` 可以实现邮件发送：

```html
<a href="mailto:nowhere@mozilla.org">向 nowhere 发邮件</a>
```



### HTML 的图片

```html
<figure>
  <img
    src="images/dinosaur.jpg"
    alt="The head and torso of a dinosaur skeleton;
            it has a large head with long sharp teeth"
    width="400"
    height="341" 
/>

  <figcaption>
    A T-Rex on display in the Manchester University Museum.
  </figcaption>
</figure>

```

`<alt>` 会在图片不能正常显示时，出现的替换文字；`<title>` 是鼠标放置在图片上会显示的文字提示。



此外，在 CSS 中也可以使用背景图片，一般是仅仅用于装饰：

```html
p {
  background-image: url("images/dinosaur.jpg");
}
```

我们已经了解到可以使用` <img> `元素显示静态图像，或者通过使用 `background-image` 属性来设置 HTML 元素的背景。你还可以动态生成图形，或在生成后对图像进行操作。浏览器提供了使用代码创建 2D 和 3D 图形的方法，以及包含来自上传文件或用户摄像头实时流的视频。

- Canvas：`<canvas>` 提供了用 JavaScript 绘制 2D 图像的 API。
- SVG：借助缩放矢量图形来用线条、曲线和其他几何形状来渲染 2D 图形。
- WebGL：用于 Web 的 3D 图形 API，可以在 Web 内容中用标准的 OpenGL ES。
- 音视频：`<video>` 和 `<audio>` 标签可以控制音视频的播放。
- WebRTC：实时通信（Real-Time Communication）可以在浏览器客户端之间进行音视频和数据共享的技术。



### HTML 的视频

```html
<video src="vt1.mkv" controls>
    <p>
        你的浏览器不支持 HTML 视频。
    </p>
</video>
```

用 `controls` 允许用浏览器自带的控制器来控制视频的播放、进度等等。



视频的容器格式定义了媒体文件的音频轨道和视频轨道的存储结构，也包括描述这个媒体文件的元数据，以及用什么编码器对其通道进行编码等等。

![从轨道级别看待媒体文件内容的图表](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Structuring_content/HTML_video_and_audio/containersandtracks.png)

需要注意的内容是，移动浏览器和桌面浏览器对格式的支持可能不一样，所以我们需要给不同格式的ship内容：

```html
<video controls>
  <source src="rabbit320.mp4" type="video/mp4" />
  <source src="rabbit320.webm" type="video/webm" />
  <p>你的浏览器不支持此视频。可点击<a href="rabbit320.mp4">此链接</a>观看</p>
</video>

```



另外，视频标签的一些特性也需要去了解：

```html
<video
  controls
  width="400"
  height="400"
  autoplay
  loop
  muted
  preload="auto"
  poster="poster.png">
  <source src="rabbit320.mp4" type="video/mp4" />
  <source src="rabbit320.webm" type="video/webm" />
  <p>你的浏览器不支持此视频。可点击<a href="rabbit320.mp4">此链接</a>观看</p>
</video>
```

- `autoplay` 会让音频和视频内容立即播放。
- `loop` 让视频或音频文件在结束时再次开始播放。
- `muted` 会让视频媒体播放时默认关闭声音。
- `poster` 是在视频播放前显示，通常是粗略的预览或广告。
- `preload` 通常被用来缓冲较大的文件的，"auto" 是在页面加载后缓存媒体文件，"meatdat" 是仅仅缓冲文件的元数据。



### HTML 的音频

音频 `<audio>` 和 视频  `<video>` 仅有一些细微差别：

- `<audio>` 元素不支持 width/heigth 属性——由于其并没有视觉部件，也就没有内容要设置 width/height。
- 它同时也不支持 poster 属性——同样，因为没有视觉部件。

```html
<audio controls>
  <source src="viper.mp3" type="audio/mp3" />
  <source src="viper.ogg" type="audio/ogg" />
  <p>你的浏览器不支持该音频，可点击<a href="viper.mp3">此链接</a>收听。</p>
</audio>

```



### HTML 的视频文本

可以用 `WebVTT` 文件格式和 `<track>` 可以为他人提供音频/视频中的话语文字记录。

> 备注：“转录（transcribe）”是指将视频/音频中说的话记录成文字形式，转录的结果称为“文字记录（transcript）”。



WebVTT 是用来编写文本文件的格式，里面是很多的字符串，有些字符串会携带元数据，用来描述这个字符串将会在视频中显示的时间，甚至是样式以及定位信息，这些字符串叫做 `cue` 比如：

- subtitles：外语材料的翻译字幕；
- captions：同步翻译对白；
- 定时描述：由媒体播放器朗读的文本。



下面是一个典型的 WebVTT 文件：

```html
WEBVTT

1
00:00:22.230 --> 00:00:24.606
第一段字幕

2
00:00:30.739 --> 00:00:34.074
第二段

…
```



1、将文件保存为 `.vtt` 文件；

2、用 `<track>` 标签链接 `.vtt` 文件放置在 `<audio>` 或 `<video> ` 标签中，并且放在 `<source> ` 之后，用 `kind` 属性来指明是 `subtitles`、`captions` 还是 `descriptions` ，然后用 `srclang` 告诉浏览器是用什么语言来编写的，最后添加 `label` 帮助读者识别语言。

```html
<video controls>
  <source src="example.mp4" type="video/mp4" />
  <source src="example.webm" type="video/webm" />
  <track kind="subtitles" src="subtitles_es.vtt" srclang="es" label="Spanish" />
</video>

```



### HTML 的表格

```html
    <table>
      <tr>
        <th>&nbsp;</th>
        <th>Knocky</th>
        <th>Flor</th>
        <th>Ella</th>
        <th>Juan</th>
      </tr>
      <tr>
        <td>Breed</td>
        <td>Jack Russell</td>
        <td>Poodle</td>
        <td>Streetdog</td>
        <td>Cocker Spaniel</td>
      </tr>
      <tr>
        <td>Age</td>
        <td>16</td>
        <td>9</td>
        <td>10</td>
        <td>5</td>
      </tr>
      <tr>
        <td>Owner</td>
        <td>Mother-in-law</td>
        <td>Me</td>
        <td>Me</td>
        <td>Sister-in-law</td>
      </tr>
      <tr>
        <td>Eating Habits</td>
        <td>Eats everyone's leftovers</td>
        <td>Nibbles at food</td>
        <td>Hearty eater</td>
        <td>Will eat till he explodes</td>
      </tr>
    </table>
```

- `<table>` 存放表格的标签；
- `<th> ` 表示表格的标题头部，用 `scope` 属性来指明是行标题还是列标题，比如 `scope="col"` 就是列标题，如果是跨列的，可以用 `scope="colgroup"` 属性。
- `<td>` 表示一个单元格；
- `<tr>` 表示表格的一行内容。

> `scope` 属性可以帮助屏幕阅读器来去阅读表格，更好地辅助视障人士。



我们用 `colspan` 和 `rowspan` 两种属性来实现跨单元格的合并，比如 `colspan=2` 决定了该单元格的宽度是 2。



如果我们想让某一列的每个数据样式都一样，可以用 `<col>` 和`<colgroup>` 元素。



如果想要添加表头可以用 `<caption>` 元素。



为了让表格的结构更加明确，建议用 `<thead>`、`<tbody>`、`<tfoot>` 来标记表格。

- `<thead>` 元素必须包住表格的表头部分。一般是第一行，往往都是每列的标题，但是不是每种情况都是这样的。如果你使用了 `<col>/<colgroup>` 元素，那么 `<thead>` 元素就需要放在它们的下面。
- `<tbody>` 元素需要包住表格内容的主要部分（不是表头和表尾）。
- `<tfoot> `元素需要包住表格的表尾部分。一般是最后一行，往往是对前面所有行的总结。



## CSS

### 浏览器加载网页的简要流程

1、浏览器载入 HTML 文件（比如从网络获取）。

2、将 HTML 文件转化成一个 **DOM（Document Object Model）** ，DOM 是文件在计算机内存的表现形式。

3、浏览器会拉取 HTML 相关的大部分资源，比如嵌入到页面的图片、视频和 CSS 样式，JavaScript 会稍后处理。

4、浏览器拉去 CSS 后会进行解析，根据不同选择器（比如 element、class、id 等等）把他们分到不同的“桶”中。浏览器基于它找到的不同选择器，将不同的规则应用在对应的 DOM 节点上，并添加节点依赖样式（过程也叫渲染树）。

5、上述规则应用于渲染树之后，渲染树会依照应该出现的结构进行布局。

6、网页显示在屏幕上（过程叫着色）。

![img](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/Styling_basics/What_is_CSS/rendering.svg)



****

一个 DOM 有一个树形结构，标记语言中的每一个元素、属性以及每一段文字都对应着结构树中的一个节点（Node/DOM 或 DOM node）。节点由节点本身和其他 DOM 节点的关系定义，有些节点有父节点，有些节点有兄弟节点（同级节点）。

对于 DOM 的理解会很大程度上帮助你设计、调试和维护你的 CSS，因为 DOM 是你的 CSS 样式和文件内容的结合。当你使用浏览器 F12 调试的时候你需要操作 DOM 以查看使用了哪些规则。



### CSS 的选择器

选择器就是所选择的 HTML 元素，有不同的选择器，比如：

- **元素选择器**：`h1`
- **类选择器**：`.special`
- **ID选择器**：`#unique`
- **属性选择器**：`a[title]` ，`a[href="https://example.com"]`
  - 解释：如果存在 `title` 标签就会进行选择；如果 `href` 属性的特性值存在就会进行选择
- **伪类选择器**：`a:hover`
- **伪元素选择器**：`p::first-line`
  - 解释：伪元素就是选择一个元素的某个部分，比如 `first-line` 元素选择的是元素中的第一行
- **运算符选择器**：`article > p`



对于选择器而言，可以进行组合，比如：

- **选择器列表**：`h1, .special`



### CSS 的属性选择器

>  如果你想在大小写不敏感的情况下，匹配属性值的话，你可以在闭合括号之前，使用 `i` 值。这个标记告诉浏览器，要以大小写不敏感的方式匹配 ASCII 字符。

**存否和值选择器**

1、`li[class]` 匹配所有带 class 属性的元素。

2、`li[class="a"]` 匹配带属性值只为 a 的元素。

3、`li[class~="a"]` 匹配带属性值有是 a 的元素。



**子字符串匹配选择器**

1、`li[class^="a"]`匹配了任何值开头为`a`的属性，于是匹配了前两项。

2、`li[class$="a"]`匹配了任何值结尾为`a`的属性，于是匹配了第一和第三项。

3、`li[class*="a"]`匹配了任何值的字符串中出现了`a`的属性，于是匹配了所有项。



### CSS 的伪类和伪元素

**伪类** 是选择器的一种，它用于选择处于特定状态的元素，比如当它们是这一类型的第一个元素时，或者是当鼠标指针悬浮在元素上面的时候。

一些常见的控制：

- `:last-child` 最后一个子元素。
- `:only-child`  没有兄弟元素时。
- `:invalid` 选择未通过验证的表单元素。
- `:hover` 指针悬停在上方。
- `:focus` 当用户点击或轻触一个元素或使用键盘的 Tab 键选择它时，它会被触发。
- `:link` 当链接未访问时。
- `:visited` 当链接访问过后。

- `:nth-child(even/odd/xxx)` 选中偶数个或奇数个或者第某个。



**伪元素** 以类似方式表现。不过表现得是像你往标记文本中加入全新的 HTML 元素一样，而不是向现有的元素上应用类。例如，如果你想选中一段的第一行，你可以把它用一个`<span>`元素包起来，然后使用元素选择器；不过，如果包起来的单词/字符数目长于或者短于父元素的宽度，这样做会失败。由于我们一般不会知道一行能放下多少单词/字符——因为屏幕宽度或者字体大小改变的时候这也会变——通过改变 HTML 的方式来可预测地这么做是不可能的。

此时，`::first-line` 的就可以在单词/字符个数发生改变时，也只会选中第一行。

```css
article p::first-line {
  font-size: 120%;
  font-weight: bold;
}
```



### CSS 的关系选择器

**后代选择器** ——典型用单个空格（" "）字符——组合两个选择器，比如选中 `body` 中的所有 `article` 中的所有 `p` 元素：

```css
body article p
```



**子代关系选择器** 是个大于号（`>`），只会在选择器选中直接子元素的时候匹配。继承关系上更远的后代则不会匹配。例如，只选中作为`<article>`的直接子元素的`<p>`元素：

```css
article > p
```



**邻接兄弟选择器**（`+`）用来选中恰好处于另一个在继承关系上同级的元素旁边的物件。例如，选中所有紧随`<p>`元素之后的`<img>`元素：

```css
p + img
```



如果你想选中一个元素的兄弟元素，即使它们不直接相邻，你还是可以使用 **通用兄弟关系选择器**（`~`）。要选中所有的`<p>`元素后*任何地方*的`<img>`元素，我们会这样做：

```css
p ~ img

```



### CSS 的盒模型

在 CSS 中，我们有几种类型的盒子，一般分为**区块盒子**（block boxes）和**行内盒子**（inline boxes）。类型指的是盒子在页面流中的行为方式以及与页面上其他盒子的关系。盒子有**内部显示**（inner display type）和**外部显示**（outer display type）两种类型。可以用 `display` 来设置显示的类型。

**外部显示类型**

一个 `block` 的盒子：

- 盒子会产生换行；
- 盒子有 `width` 和 `height`。
- 内边距、外边距和边框会将其他元素从当前盒子周围”推开“。
- 没有指定 `width` 的盒子就会沿行拓展，与容器一样宽。

一个 `inline` 的盒子：

- 盒子不会换行。
- 盒子的 `width` 和 `height` 没有用。
- 垂直方向的 `padding` `margin` 和 `border` 不会将其他 `inline` 的盒子推开。
- 水平方向的 `padding` `margin` 和 `border` 会将其他 `inline` 的盒子推开。

**内部显示类型**

内部显示类型决定了盒子内元素的布局方式。

默认以 **标准流** 的方式进行布局，如果设置为 `display: flex` 就会以单行盒子的规范来执行。

****

在 CSS 中组成一个盒子需要：

- **内容盒子**：显示内容的区域，`inline-size` 和 `block-size` 或 `width` 和 `height` 等属性确定大小。
- **内边距盒子**：填充位于内容周围的空白处；使用 `padding` 和相关属性确定其大小。
- **边框盒子**：边框盒子包住内容和任何填充；使用 `border` 和相关属性确定其大小。
- **外边距盒子**：外边距是最外层，其包裹内容、内边距和边框，作为该盒子与其他元素之间的空白；使用 `margin` 和相关属性确定其大小。

****

CSS 提供了两种主要的盒模型：`content-box` 和 `border-box`。默认情况都是 `content-box`：

- 总宽度 = width + padding + border	总高度 = height + padding  + border

我们可以通过设置 `box-sizing: border-box` 来改变计算：

- 总宽度 = width （包含了 padding 和 border）	总高度 = height（包含了 padding 和 border）



### CSS 的层叠、优先级与继承

CSS 代表的是 **层叠样式表（Cascading Style Sheets）**:

- **层叠**：表示当两条同级别的规则应用到一个元素时，写在后面的就是实际使用的规则。
- **优先级**：决定当多个规则有不同选择器对应相同的元素的时候需要使用哪个规则。
- **继承**：一些设置在父元素上的 CSS 属性是可以被子元素继承的，有些则不能。

****

根据以下属性值来控制继承：

- `inherit`：开启继承。
- `initial`：将应用于选定元素的属性值设置为该属性的初始值。

- `unset`：将属性重置为自然值，如果属性是自然继承那么就是 `inherit`，否则和 `initial` 一样。



### CSS 的值和单位

CSS 中有两种类型的长度——**相对长度**和 **绝对长度**。

| 单位 | 名称         | 等价换算                 |
| :--- | :----------- | :----------------------- |
| `cm` | 厘米         | 1cm = 37.8px = 25.2/64in |
| `mm` | 毫米         | 1mm = 1/10th of 1cm      |
| `Q`  | 四分之一毫米 | 1Q = 1/40th of 1cm       |
| `in` | 英寸         | 1in = 2.54cm = 96px      |
| `pc` | 派卡         | 1pc = 1/6th of 1in       |
| `pt` | 磅           | 1pt = 1/72th of 1in      |
| `px` | 像素         | 1px = 1/96th of 1in      |

****

相对长度单位是相对于其他某些东西来说的：

- `em` 相对于本元素的字体大小；`rem` 相对于根元素的字体大小。
- `vh` 和 `vw` 分别是相对于视口的高度和宽度。



### CSS 的溢出内容

`overflow` 属性是用来控制元素溢出的方式，默认值为 `visible` ，也就是元素溢出的时候我们能够看见；如果改为 `hidden`  那我们就看不见溢出的内容；如果改为 `scroll` 就会看见滚动条，设置为 `overflow-y: scroll` 是就是仅在 y 轴上进行滚动，设置为 `auto` 的话，就可以在溢出时才添加滚动条。

****

对于 `img` 元素来说，可以用 `object-fit` 属性来进行处理：

- `cover` 表示保持图像的原始比例，但是多余的内容会被裁剪。
- `contain` 表示包含整个图像，如果与盒子比例不同就会比较难看。



### CSS 的浮动布局

`float` 属性最初只是用在成块的文本内浮动图像，但是现在它已成为在网页上创建多列布局的最常用工具之一。

浮动其实就是脱离正常的文档布局流，比如 `float: left` 就会将元素吸附到父容器的左边，当我们不想让其他元素随着浮动元素进行布局时，可以用 `clear` 属性：

- `left` 停止任何活动的左浮动。
- `right` 停止任何活动的右浮动。
- `both` 停止任何活动的左右浮动。

****

**"clearfix 小技巧"** ，其过程为：先向包含浮动内容及其本身的盒子后方插入一些生成的内容，并将生成的内容清除浮动。

```css
.wrapper::after {
  content: "";
  clear: both;
  display: block;
}

```



**”overflow“**，添加 `overlfow: auto` 可以停止浮动，是因为创建了所谓的 **块格式化上下文（BFC）**。可以把它看作页面内部包含所需元素的一小块布局区域。如此设置可以让浮动元素包含在 BFC 及其背景之内。

> BFC 是一种独立的渲染区域，其中的元素按照特定的规则进行布局，并且不会影响到这个区域之外的元素。比如：根html、浮动、绝对定位等等。

```css
.wrapper {
  background-color: rgb(79, 185, 227);
  padding: 10px;
  color: #fff;
  overflow: auto;
}

```



**”flow-root“**，使用 `display: flow-root` 创建块格式化上下文，在使用上没有副作用。

```css
.wrapper {
  background-color: rgb(79, 185, 227);
  padding: 10px;
  color: #fff;
  display: flow-root;
}

```



### CSS 的定位

默认的元素定位就是**静态定位**，将按照正常的文档流来进行。当我们修改为 `position: relative` 时，与父元素**相对的位置**进行布局。而当我们修改为 `position: absolute` 时，就是脱离正常的文档流，**绝对定位元素**会被包含在**初始块容器**中。这个初始块容器有着和浏览器视口一样的尺寸，并且 `<html>` 元素也被包含在这个容器里面。简单来说，绝对定位元素会被放在 `<html>` 元素的外面，并且根据浏览器视口来定位。

****

网页也有一个 z 轴：一条从屏幕表面到你的脸（或者在屏幕前面你喜欢的任何其他东西）的虚线。因此，我们可以用 `z-index` 来影响定位元素位于该轴上的位置；正值将它们移动到堆栈上方，负值将它们向下移动到堆栈中。默认情况下，定位的元素都具有 z-index 为 auto，实际上为 0。

****

固定定位 `position: fixed` 就是相对于浏览器视口本身的位置；另一个 `position: sticky`  可以让元素滚动到某个阈值就变得固定，所以我们可以用来将某个内容随着滚动显示在视窗上面，或者做滚动索引功能：

```css
.positioned {
  position: sticky;
  top: 30px;
  left: 30px;
}
```



### CSS 的弹性盒子

![在从左到右的语言中，三个 flex 项并排放置在 flex 容器中。主轴——弹性容器布置 flex 方向上的轴——是水平的。主轴的两端是开始端和结束端，分别位于左侧和右侧。交叉轴是垂直的；垂直于主轴。交叉轴的开始端和结束端分别位于顶部和底部。flex 项沿着主轴排列，在这种情况下，宽度称为主轴尺寸，flex 项沿交叉轴排列，在这种情况下，高度称为交叉尺寸。](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/CSS_layout/Flexbox/flex_terms.png)

- **主轴（main axis）**：沿着 flex 元素放置的方向延伸的轴，开始和结束被称为 **main start** 和 **main end** 。
- **交叉轴（cross axis）**：垂直于 flex 元素放置的方向轴，开始和技术被称为 **cross start** 和 **cross end**。
- **flex 容器**：设置了 `display: flex` 是弹性盒子的父容器。
- **flex 项**：父容器中的弹性盒子。
- **行列**，用 `flex-direction: coloum / row` 来指定主轴方向，用 `flex-wrap: wrap` 来处理溢出的弹性盒子，这两个属性可以写成 `flex-flow: row wrap`。

****

在 CSS 的 Flexbox 布局模型中，`flex-grow`、`flex-shrink` 和 `flex-basis` 是三个非常重要的属性，它们共同决定了 **弹性项目（flex items）** 如何在 **弹性容器（flex container）** 中分配空间和调整大小。

- `flex-grow` 定义了弹性项目的扩展比例，取值为 0、1、2 等等。如果所有项目的 `flex-grow` 值相同，那么就会平分剩余的空间；如果某个项目的 `flex-grow` 值更大，则该元素占据更多的剩余空间。

- `flex-shrink` 定义了弹性项目在空间不足时的收缩比例，取值为 0、1、2 等等。如果所有项目的 `flex-shrink` 相同，则同比例缩小；如果某个 `flex-shrink` 值更大，则收缩的空间更大。
- `flex-basis` 定义了弹性项目在分配多余空间之前的大小，默认为 `auto`，取值范围是长度值（如 `100px`, `50%`）、关键字（如 `auto`, `content`）。

通常我们会简写这三个属性：`flex: <flex-grow> <flex-shrink> <flex-basis>;`

****

**主轴控制**，`justify-content` 控制弹性盒子在主轴上的位置。

**交叉轴控制**，`align-items` 控制弹性盒子在交叉轴上的位置。



### CSS 的网格布局

一个网格通常具有许多的**列（column）与行（row）**，以及行与行、列与列之间的间隙，这个间隙一般被称为**沟槽（gutter）**。

![img](https://developer.mozilla.org/zh-CN/docs/Learn_web_development/Core/CSS_layout/Grids/grid.png)

除了长度和百分比，我们也可以用 `fr` 这个单位来灵活地定义网格的行与列的大小。

```css
.container{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr; 
    /* 对于重复的部分，可以用 repeat 
    grid-template-columns: repeat(3, 1fr);
    */
}
```

对于行列之间的间隔，我们可以用 `grid-column-gap`、`grid-row-gap` 或 `grid-gap` 来设定。

```css
.container{
	display: grid;
    grid-template-columns: 2fr 1fr 1fr;
    grid-gap: 20px;
}
```

****

显式网格是我们用 `grid-template-columns` 或 `grid-template-rows` 属性创建的。而隐式网格则是当有内容被放到网格外时才会生成的。显式网格与隐式网格的关系与弹性盒子的 main 和 cross 轴的关系有些类似。

隐式网格中生成的行/列大小是参数默认是 `auto` ，大小会根据放入的内容自动调整。我们也可以用 `grid-auto-rows` 和 `grid-auto-columns` 来设定大小。

- *简单来说，隐式网格就是为了放显式网格放不下的元素，浏览器根据已经定义的显式网格自动生成的网格部分。*



###  CSS 的响应式设计

随着人们使用的屏幕尺寸的种类越来越多，出现了  **响应式网页设计的概念（*responsive web design，RWD*）**，RWD 指的是允许 Web 页面适应不同屏幕宽度因素等，进行布局和外观的调整的一系列实践。

**CSS 媒体查询**为你提供了一种应用 CSS 的方法，仅在浏览器和设备的环境与你指定的规则相匹配的时候 CSS 才会真的被应用，例如“视口宽于 480 像素”的时候。

比如：

```css
@media media-type and (media-feature-rule) {
  /* CSS rules go here */
}

```

**媒体类型**：`all`、`print`、`screen`、`speech`

**媒体特征**：`min-width`、`max-width`、`width`