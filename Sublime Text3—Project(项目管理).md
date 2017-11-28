## 摘要
Project 可以理解为项目、工程或者站点，以下称项目。使用项目管理的好处是：不用将所有文件都放到同一个根目录，可以将相关但不同路径的文件组成一个Project，每个项目都是独立的，文件的状态等都会被保存，因此只需一个窗口便可以在多个项目中随意切换。

<br>
## 一、创建Project
先将文件加进侧边栏创建 Project，以下方式都可：
1. 打开侧边栏，快键键是 **Ctrl+B,Ctrl+K**，直接将文件拖拽进去即可。
2. 点击菜单 **Project | Add Folder to Project** 选择要添加的文件。

建议：推荐装个插件 SideBarEnhancements，这个功能很强大，例如之前介绍的[Sublime Text3—设置快捷键打开浏览器](https://juejin.im/post/59c5f7b4f265da06670c86e9)。
<br>
## 二、保存Project
选好文件后保存当前的 Project ：菜单 **Project | Save Project As...**，选择Project文件的存放位置，填好项目名称，保存后会生成2个文件。
1. name.sublime-project 文件：project（项目）记录了你打开的窗口中包含哪些文件夹，会被记录到版本记录里。

2. name.sublime-workspace 文件：workspace（工作区）记录了当前窗口的一切信息，除了包含文件夹信息外，还有文件的打开状态、文件是否保存、标签的顺序等，如果你有分屏，还会保存 Group 信息。因此有了 workspace，不管什么时候关闭了 Sublime，再次打开时所有的窗口状态都和关闭时一样。

建议：新建个文件夹统一保存以上文件，如：Sublime Text 3\Packages\User\project。

注意：再新建项目时，先关闭当前项目 **Project | Close Project**，再重复以上步骤。

<br>
## 三、切换Project
每个项目都有 project 和 workspace 这2个文件，所以切换项目时，每个项目状态都会独立存储，不用担心切换后没保存。
1. 打开项目： **Project | Open Project** ，选择要打开的sublime-project 文件，如果已有打开项目会在新窗口打开。
2. 打开最近的项目：**Project | Open Recent** ，如果已有打开项目会在新窗口打开。
3. 切换项目：**Project | Switch Project** ，选择要切换的 sublime-project 文件，会在当前窗口切换。
4. 快速切换项目：**Project | Quick Switch Project** ，快捷键是 **Ctrl+Alt+P**，会弹出搜索框如下图：
![快速切换弹出框.png](http://upload-images.jianshu.io/upload_images/4260407-c94dd8727ec1b29a?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

<br>
## 四、编辑Project
1. 添加文件到项目上面已介绍。
2. 选中文件鼠标右键，点 **Remove Folder From Project** 将文件从当前项目删除。
3. 菜单 **Project | Edit Project**，会打开当前的sublime-project文件（sublime点击编辑会直接切换至该项目，建议用其他软件编辑），Json 格式，记录的是当前侧边栏的文件信息，如下：
```
{
	"folders":
	[
		{
			"path": "D:\\public\\fwtz030"
		},
		{
			"path": "D:\\public\\fwkc050"
		}
	]
}
```

<br>
## 五、其他补充
1. 如果觉得以上麻烦可安装插件：ProjectManager。

2. 删除快速切换中已经结束的项目，可编辑文件：
C:\Users\{User}\AppData\Roaming\Sublime Text 3\Local\Session.sublime_session

3. 我现在版本是3143，快速切换的快键键 **Ctrl+Alt+P** 已不在默认设置中，因此没效果，这时可以添加到自定义keymap，菜单 **Preference | Key Bindings**，添加如下，如果还是没效果，可能是快捷键有冲突。
```
{
	"keys": ["ctrl+alt+p"],
	"command": "prompt_select_workspace"
}
```
<br>

**掘金：**[Sublime Text3—Project(项目管理)](https://juejin.im/post/5a0baa0e5188253ee45af950)
**简书：**[Sublime Text3—Project(项目管理)](http://www.jianshu.com/p/259c9db1aa8a)
**博客园：**[Sublime Text3—Project(项目管理)](http://www.cnblogs.com/easy-blue/p/7840885.html)
