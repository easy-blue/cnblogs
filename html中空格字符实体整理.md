## 摘要

>浏览器总是会截短 HTML 页面中的空格。如果您在文本中写 10 个空格，在显示该页面之前，浏览器会删除它们中的 9 个。如需在页面中增加空格的数量，您需要使用`&nbsp;`字符实体。

本篇就单介绍**空格的字符实体**，HTML提供了6种空格实体（space entity）：

```
&nbsp;
&ensp;
&emsp;
&thinsp;
&zwnj;
&zwj;
```

在web页面上，一般有3种书写：

```
1. 直接输入法输入例如“版权” – ©.
2. 字符：&copy;
3. charCode：&#xa9;
```
<br>

## 正文

### `&nbsp;`
不间断空格（non-breaking space）字符编码`&#160;`：在HTML中，按下space键产生，空格不累加（只算1个），要使用html实体表示才可累加。
<br>

### `&emsp;`
全角空格（Em Space）字符编码`&#x2002;`：em是字体排印学的计量单位。相当于当前指定的点数，如1em在16px的字体中就是16px。此空格有个相当稳健的特性，**其占据的宽度正好是1个中文宽度**。
<br>

### `&ensp;`
半角空格（En Space）字符编码`&#x2003;`：en是字体排印学的计量单位。为em宽度的一半，如1en在16px的字体中就是16px，名义上是小写字母n的宽度。此空格有个相当稳健的特性，**其占据的宽度正好是1/2个中文宽度**。
<br>

### `&thinsp;`
窄空格（Thin Space）占据的宽度比较小，它是em之六分之一宽。
<br>

### `&zwnj;`
零宽不连字（Zero Width Non Joiner）字符编码`&#x200C`：简称“ZWNJ”，是一个不打印字符，放在电子文本的两个字符之间，抑制本来会发生的连字，而是以这两个字符原本的字形来绘制。HTML字符值` &#8204;` 。
<br>

### `&zwj;`
零宽连字（Zero Width Joiner）字符编码`&#x200D`：简称“ZWJ”，是一个不打印字符，放在某些需要复杂排版语言（如阿拉伯语、印地语）的两个字符之间，使得这两个本不会发生连字的字符产生了连字效果。HTML字符值`&#8205;`。
<br>

## 其它
- 浏览器还会把以下字符当作空白进行解析：空格`&#x0020;`、制表位`&#x0009;`、换行`&#x000A;`和回车`&#x000D;`还有`&#12288;`等等。

- `&#x+16进制/十进制`表示是 Numeric Character References

- `&+实体名`表示是 Character Entities References，html字符实体的名字必须是在html中已经定义的才能被使用。

- 使用实体名而不是数字的好处是，名称易于记忆。坏处是，浏览器也许并不支持所有实体名称（对实体数字的支持却很好）。

- 实体名称对大小写敏感。

<br>

## 参考

- 张鑫旭 [web页面相关的一些常见可用字符介绍](http://www.zhangxinxu.com/wordpress/2011/05/web页面相关的一些常见可用字符介绍/)

- 张鑫旭 [小tips: 使用`&#x3000;`等空格实现最小成本中文对齐](http://www.zhangxinxu.com/wordpress/2015/01/tips-blank-character-chinese-align/)

- w3school [HTML 字符实体](http://www.w3school.com.cn/html/html_entities.asp)

- w3school [HTML 实体符号参考手册](http://www.w3school.com.cn/tags/html_ref_entities.html)

<br>

**掘金：**[html中空格字符实体整理](https://juejin.im/post/59c36b445188254f962cc40d)
**简书：**[html中空格字符实体整理](http://www.jianshu.com/p/b0f3e684d3bb)
**博客园：**[html中空格字符实体整理](http://www.cnblogs.com/easy-blue/p/6656876.html)