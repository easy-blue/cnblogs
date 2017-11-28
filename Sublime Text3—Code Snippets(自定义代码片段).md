## 摘要
程序员总是会不断的重复写一些简单的代码片段，为了提高编码效率，我们可以把经常用到的代码保存起来再调用。

平时用sublime安装各种插件，使用Tab键快速补全，便是snippets（可译为代码片段）的一种。

Sublime编辑器还提供了自定义代码片段的功能（当然不止Sublime有此功能），其[官方文档][1]中定义如下：
>Whether you are coding or writing the next vampire best-seller, you’re likely to need certain short fragments of text again and again. Use snippets to save yourself tedious typing. Snippets are smart templates that will insert text for you and adapt it to their context.

<br>

## 一、创建snippets

### 1. 新建和保存
- 菜单栏中依次选择**Tools | Developer | New Snippet...**就会新建一个扩展名为`.sublime-snippet`的XML语法的文档，注意后缀是识别snippets的关键。

- 代码片段可以任意存储在packages文件夹下，默认会保存在**Packages\User**文件夹里，为了方便管理和使用建议再新建个文件夹例如snippets，则路径为**Packages\User\snippets**。

- 默认结构如下：

```
<snippet>
	<content><![CDATA[
Hello, ${1:this} is a ${2:snippet}.
]]></content>
	<!-- Optional: Set a tabTrigger to define how to trigger the snippet -->
	<!-- <tabTrigger>hello</tabTrigger> -->
	<!-- Optional: Set a scope to limit where the snippet will trigger -->
	<!-- <scope>source.python</scope> -->
</snippet>
```

<br>

### 2. content
- `<content></content>`中必须包含`<![CDATA[…]]>`，在这里面写自定义的代码片段。

- 代码片段如果含有`]]>`，需写成`]]$NOT_DEFINED>`。

- 如果含有`$`，需写成`\$`。

<br>

### 3. tabTrigger
- 在`<tabTrigger></tabTrigger>`中设置让Sublime自动补全的触发词（trigger keyword）。

<br>

### 4. scope
- 设置代码片段在何种语言环境下激活，默认写的是python。

- 想指定多个scope，可以使用英文逗号`,`来分隔。

- 如何知道文档的`Scope`是什么？菜单栏依次选择**Tools | Developer | Show Scope Name...**，快捷键是**Ctrl+Alt+Shift+P**。

<br>

### 5. description
- 如果加了`<description>描述内容</description>`，点开**Tools | Snippets...**会显示你定义的描述内容。

- 如果不写则显示文件名。

<br>

### 6. 设置光标位置`Fields`
```
<snippet>
    <content><![CDATA[
First Name: $1
Second Name: $2
Address: $3
]]></content>

```
- 美元符加数字即可设置field markers即光标的位置，按Tab键光标按数字依次从小到大循环，如上从1到2到3再到1。

- Shift+Tab可以进行向上跳转。

- Esc结束跳转。

- $0表示最后一个位置。

<br>

### 7. 镜像域`Mirrored Fields`
- 相同编号的位置即是镜像域，可同时选中进行编辑。

<br>

### 8. 占位符`Placeholders`
- `{数字编号}`可以得到一个Tab占位符。

- `{1:default}`可以得到一个默认值。

- 按Tab键依次循环选中代码片段中的默认值。

如默认的代码片段`Hello, ${1:this} is a ${2:snippet}.`会依次循环选中单词`this` `snippet`。

<br>

## 二、使用snippets
- 方法1：菜单栏点击**Tools | Snippets...**,弹出为当前语法可用的Snippet，点击即插入。

- 方法2：输入**触发词**然后按**Tab键**。

<br>

## 三、安装snippets
- 方法1：进入Package Control:install Package搜索选择安装已有的代码片段扩展包。

- 方法2：菜单选择**Preferences | Browse Packages...**打开，建议新建文件夹snippets方便管理，路径为**Sublime Text3\Packages\User\snippets**，将写好的代码片段拷贝进去。

<br>

## 参考
- [sublimetext官方文档Snippets介绍][1]

- [手把手教你写Sublime中的Snippet][2]

- [Sublime Text自定制代码片段(Code Snippets)][3]

[1]: http://docs.sublimetext.info/en/latest/extensibility/snippets.html "sublimetext官方文档Snippets介绍"
[2]: http://www.jianshu.com/p/356bd7b2ea8e "手把手教你写Sublime中的Snippet"
[3]: https://9iphp.com/web/html/sublime-text-code-snippets.html "Sublime Text自定制代码片段(Code Snippets)"

<br>

**掘金：**[Sublime Text3—Code Snippets(自定义代码片段)](https://juejin.im/post/59c36c41f265da0669086225)
**简书：**[Sublime Text3—Code Snippets(自定义代码片段)](http://www.jianshu.com/p/bbebd843ed9b)
**博客园：**[Sublime Text3—Code Snippets(自定义代码片段)](http://www.cnblogs.com/easy-blue/p/7515088.html)