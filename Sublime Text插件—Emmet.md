#### 摘要：
安装请看上一篇[Sublime Text—安装](http://www.cnblogs.com/easy-blue/p/5148596.html)，和[sublime自带快捷键](http://www.cnblogs.com/easy-blue/p/5809760.html)一起用，写html简直快的飞起。

下面整理的是常用的，完整的可看[emmet官方文档](https://docs.emmet.io/cheat-sheet/)。

## 生成标签
### 1.快速生成文档结构

- `!`或`html:5`，快速生成 HTML5 结构(都需要再按tab键)

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>

</body>
</html>
```

- `html:xt` 生成 HTML4 过渡型

- `html:4s` 生成 HTML4 严格型

### 2.生成带 id 的元素

标签 # ID名，如：`div#header`
```
<div id="header"></div>
```

### 3.生成带 class 的元素

标签 . 类名，如：`div.title`
```
<div class="title"></div>
```

### 4.生成后代元素：>
如：`nav>ul>li`
```
<nav>
	<ul>
		<li></li>
	</ul>
</nav>
```

### 5.生成兄弟元素：+
如：`div+p+div`
```
<div></div>
<p></p>
<div></div>
```

### 6.生成上级元素：^
如：`p^div`
```
<p></p>
<div></div>
```

### 7.重复生成多个元素：*
如：`ul>li*5`
```
<ul>
	<li></li>
	<li></li>
	<li></li>
	<li></li>
	<li></li>
</ul>
```

### 8.生成带自定义属性：[attr]
如：`div[value=1] `
```
<div value="1"></div>
```

### 9.生成带文本内容：{}
如：`a{Click me}`
```
<a href="">Click me</a>
```

### 10.加编号：$

- 从1开始：加$

如：`div.item${$$}*3`
```
<div class="item1">01</div>
<div class="item2">02</div>
<div class="item3">03</div>
```

- 倒序： $ 后面增加 @-

如：`div.item$@-{$$@-}*3`
```
<div class="item3">03</div>
<div class="item2">02</div>
<div class="item1">01</div>
```

- 指定序号：可以使用 @N

如：`div.item$@4{$$@4}*3`
```
<div class="item4">04</div>
<div class="item5">05</div>
<div class="item6">06</div>
```

### 11.分组：()
如：`(ul>ol)*3 `
```
<ul>
	<ol></ol>
</ul>
<ul>
	<ol></ol>
</ul>
<ul>
	<ol></ol>
</ul>
```

### 来个综合案例
`table#tab[value=1].a>tr*3>(td{$$}>span)*3`
```
<table id="tab" value="1" class="a">
	<tr>
		<td>01<span></span></td>
		<td>02<span></span></td>
		<td>03<span></span></td>
	</tr>
	<tr>
		<td>01<span></span></td>
		<td>02<span></span></td>
		<td>03<span></span></td>
	</tr>
	<tr>
		<td>01<span></span></td>
		<td>02<span></span></td>
		<td>03<span></span></td>
	</tr>
</table>
```

## 生成css
css样式多，缩写自然也很多，列举常用的举一反三即可。

其中css缩写是采用模糊搜索匹配的，比如ov:h == ov-h == ovh == oh。

- w10 `width: 10px;` w10p `width: 10%;` w10e `width: 10em;` w10x `width: 10xe;`
- h10 `height: 10px;`
- por `position: relative;` poa `position: absolute;`
- fll `float: left;` fr `float: right;`
- dt `display: table;` db `display: block;` dib `display: inline-block;`
- ovy `overflow-y: hidden;`
- cb `clear: both;`
- mt `margin-top: ;`  mb `margin-bottom: ;`
- pt `padding-top: ;`  pb `padding-bottom: ;`
- tac `text-align: center;`
- lh `line-height:;`
- tsn `text-shadow: none;`
- tja `text-justify: auto;`
- c `color: #000;` cr `color: rgb(0, 0, 0);` cra `color: rgba(0, 0, 0, .5);`
- op `opacity: ;`
- cnt `content: '';`
- ol `outline: ;`
- bd+ `border: 1px solid #000;` bdb+ `border-bottom: 1px solid #000;`
- bd2px#333s `border: 2px #333 solid;`

## 快捷键

如果没作用请检查快捷键是否冲突

- 快速生成包裹标签：Ctrl+Shift+G

只有文本没有结构时，如下
```
首页
简介
动态
```
选中文本按快捷键Ctrl+Shift+G，再弹出的：Enter Wrap Abbreviation（输入扩展缩写）中输入`nav>ul>li.item$*>a`就会生成
```
<nav>
	<ul>
		<li class="item1"><a href="">首页</a></li>
		<li class="item2"><a href="">简介</a></li>
		<li class="item3"><a href="">动态</a></li>
	</ul>
</nav>
```
如果原先的文本带编号，不想要则可以在上面的基础上加`|t`,`nav>ul>li.item$*>a|t`即可生成如上结果。
```
1首页
2简介
3动态
```

- 自动添加/更新图片尺寸：ctrl+U

光标移到标签上的任意位置，按下快捷键`ctrl+U`即可。
```
<img src="img/x1.png" />
<img src="img/x1.png" width="100" height="200" />
```

- 删除标签：shift+ctrl+;

- 定位到上个编辑点：ctrl+alt+left

- 定位到下个编辑点：ctrl+alt+right

- 选中下一项：shift+ctrl+.

- 加/减1：ctrl+up/ctrl+down

- 加/减10：shift+alt+up/shift+alt+down


- 展开缩写：ctrl+e（和tab键作用相同）

- 重命名标签(rename_tag)：ctrl+shift+'

- 更换标签(update_as_you_type)：ctrl+Shift+U

- 匹配标签对：ctrl+alt+j

### 生成测试文本
输入`lorem`再按tab会随机生成一段英文,默认是生成30个单词，可以加上数字控制单词数量，如`lorem5`。
```
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perferendis incidunt, expedita voluptates ratione praesentium error a accusamus corporis deleniti. Cum, debitis id, in rem exercitationem at voluptatum illum minima corporis!
```
```
Lorem ipsum dolor sit amet.
```

