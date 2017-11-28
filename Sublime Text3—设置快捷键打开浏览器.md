## 摘要
用浏览器查看代码效果可谓是家常便饭，所以用不同快捷键对应打开不同浏览器可以大大提高工作效率。本篇分享个简单的方法只需二步。

<br>
## 一、安装插件SideBarEnhancements

**Ctrl+Shift+P** 转 **Package Control: Install Package** 搜**SideBarEnhancements**安装。

没装Package Control？请看：[Sublime Text3—软件安装、package control插件管理][1]。

![安装SideBarEnhancements.png](http://upload-images.jianshu.io/upload_images/4260407-6b08ce3274f54505.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

<br>
## 二、设置快捷键
菜单打开**Key Bindings | user**复制下面代码，然后修改为你的浏览器路径，重启软件。

![菜单选择.png](http://upload-images.jianshu.io/upload_images/4260407-d7ea7137b73bf073.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
[
	{
		"keys": ["f1"],
		"command": "side_bar_files_open_with",
		"args": {
			"application": "D:\\Program Files (x86)\\Mozilla Firefox\\firefox.exe",
			"extensions": ".*",
			"paths": []
		}
	},
	{
		"keys": ["f2"],
		"command": "side_bar_files_open_with",
		"args": {
			"application": "C:\\Users\\delll\\AppData\\Local\\Google\\Chrome\\Application\\chrome.exe",
			"extensions": ".*",
			"paths": []
		}
	},
	{
		"keys": ["f5"],
		"command": "side_bar_files_open_with",
		"args": {
			"application": "C:\\Program Files\\Internet Explorer\\iexplore.exe",
			"extensions": ".*",
			"paths": []
		}
	}
]
```
keys是按键，application是浏览器程序路径，extensions是匹配所有的文件后缀格式。
<br>
### Tips

1.`f3`是查找下一个的快捷键，`f11`是全屏的快捷键，设置时小心冲突！更多快捷键请看：[Sublime Text—自带快捷键介绍][2]。

![f3默认是findnext.png](http://upload-images.jianshu.io/upload_images/4260407-fa30b3852a8aaf68.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2.桌面的快捷图标怎么看路径？**选中图标 | 右键 | 属性**，反斜杠需转义把`\`改为`\\`。

![查看浏览器路径.png](http://upload-images.jianshu.io/upload_images/4260407-4fd75924bdb79314.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

<br>

[1]: http://www.cnblogs.com/easy-blue/p/5148596.html "Sublime Text3—软件安装、package control插件管理"

[2]: http://www.cnblogs.com/easy-blue/p/5809760.html "Sublime Text—自带快捷键介绍"

**掘金：**[Sublime Text3—设置快捷键打开浏览器](https://juejin.im/post/59c5f7b4f265da06670c86e9#heading-3)
**简书：**[Sublime Text3—设置快捷键打开浏览器](http://www.jianshu.com/p/8a41b97514f4)
**博客园：**[Sublime Text3—设置快捷键打开浏览器](http://www.cnblogs.com/easy-blue/p/5616686.html)
