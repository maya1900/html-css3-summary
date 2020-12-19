# HTML&CSS3

## HTML

### 基本概念

- 超文本标记语言
- XHTML可扩展标记语言
- 区别

	- XHTML以斜杠结尾
	- XHTML标签小写
	- XHTML属性要用双引号

### 基本组成

- 结构html
- 样式css
- 行为js ECMA

### 基本结构

<!-- 声明文档类型 -->
<!DOCTYPE html>
<html>
 <!-- 头部 -->
 <head>
  <meta charset="utf-8" />
  <title>我的第一个网页</title>
 </head>
 <body>
  图片/文字
 </body>
</html>

- 自动生成  !+Tab

### 基本语法

- 标签/标记/元素

	- 单标签
	- 双标签

- 属性

	- 标签与属性用空格隔开
	- 属性与属性值用等号连接
	- 一个元素可以有多个属性，用空格隔开，不分先后

### 基本标签

- 文章类标签

	- 标题标签h1-h6

		- 双标签
		- 加粗
		- 字号逐渐减小
		- 独占一行

- 段落标签

	- p标签

		- 双标签/独占一行

	- 加粗

		- <b></b>
		- <strong></strong>
		- 区别：strong重在强调，有语义化

	- 倾斜

		- <i></i>
		- <em></em>
		- 区别：em重在强调，有语义化

	- 下划线 `<u></u>`
	- 删除线 `<del></del>`
	- 上标 `<sup></sup>`
	- 下标 `<sub></sub>`
	- 强制换行 `<br>`
	- 水平线 `<hr>`
	- 特殊字符

		- 空格：` `
		- 左尖括号：`&lt;`
		- 右尖括号：`&gt;`
		- 版权：`&copy;`
		- 商标：`&reg;`

	- 超链接 a

		- 双标签/自带下划线/可以在一行显示
		- href 链接地址

			- #固定链接

		- target打开方式

			- _blank 新窗口打开
			- _self 本窗口打开

	- 图片 image

		- src 图片路径
		- alt 图片未加载显示
		- title 鼠标指时显示标题
		- 图片bug

			- 图片会自带底部3px的留白
			- 给图片设置 vertical-align除baseline的值
			- 给图片设置 display:block;
			- 给图片设置 float:left;
			- 给图片的父元素设置 font-size:0;

- 列表

	- 无序列表ul>li

		- 1.快速生成ul和li  ul>li*10{哈哈哈$} 回车
		- 2.应用场景：新闻列表/网页导航/商品列表

	- 有序列表ol>li

	  <ol type="A" start="3">
	      <li>嘿嘿嘿1</li>
	      <li>嘿嘿嘿2</li>
	     </ol>

		-  1.type 排序方式 默认是数值1 A/a/I/i
		- 2.start 排序的起始值，**只能设置成数字**

	- 自定义列表dl>dt+dd

	  <dl>
	      <dt>
	        <img src="下载.jpg" alt="" width="300">
	      </dt>
	      <dd>angela大宝贝真漂亮</dd>
	     </dl>

		- 1.dt里面一般放图片，dd一般放图片说明
		- 2.应用场景：上面是图片下面是文字 或者 左边是图片 右边是文字     

- 布局标签

	- div
	- span

- 表格标签

  <table width="100%" border="1">
   <tr>
     <td colspan="3">HTML5</td> </tr>
   <tr> 
      <td rowspan="2">web前端</td>
     <td>HTML</td>
     <td>99</td>
   </tr>
  </table>

	- 表格table

		- 边框 border
		- 宽width高height
		- 单元格间隙cellspacing=0
		- 文字距单元格距离cellpadding
		- 水平对齐align

	- 行 tr

		- 水平对齐align
		- 垂直对齐valign 居中/top/bottom

	- 列 td
	- 列合并 colspan
	- 行合并 rowspan
	- 表格补充

		- 行分组

			- thead
			- tbody
			- tfoot

		- 列分组

			- colgroup

			  <colgroup>
			   <col span="划分几列为一组的个数">
			   <col span="划分几列为一组的个数">
			  </colgroup>

		- 表格标题caption

		  <caption>标题</caption>
		  caption-side: bottom;

		- 列标题th

- 表单

	- 表单集 form

	  <form action="" method="POST"></form>

	- action 表单提交路径
	- method 表单提交方式

		- get传送数量一般不超过2kb
		- post不受限制

	- 文本输入

	  <input type="text" name="xm" value="包子" placeholder="请输入姓名">
	   value: 默认值
	   placeholder：提示信息
	   name：和后端交互用的

	- 密码输入

	  <input type="password" name="mm" placeholder="请输入密码" value="123">
	   value: 默认值
	   placeholder：提示信息
	   name：和后端交互用的

	- 提交

	  <input type="submit" value="注册">
	   value: 按钮文本

		- 要放在form里面才生效，提交到action对应的路径里

	- 重置

	  <input type="reset" value="清空">

	- 普通按钮

	  <input type="button" value="普通按钮">

	- 表单新增

		- 单选框radio

		  <input type="radio" name="sex" checked id="man" />男
		  <input type="radio" name="sex" id="woman" disabled />女 checked: 默认选中
		  disabled: 禁止选中

			- 必须加 name 属性，且值一样才可以互斥

		- 多选框 checkbox

		  <input type="checkbox" />盲僧 <input type="checkbox" />劫
		  <input type="checkbox" />德莱文

			-  也可以设置默认选中和禁止选中

		- 下拉列表select

		  <select name="sg" id="">
		   <option value="1">170cm</option>
		   <option value="2">175cm</option>
		  </select>

		- 多行文本域 textarea

		  <textarea></textarea>

			- 设置禁止用户缩放 textarea{resize:none}

		- 文件上传 file

		  <input type="file" />

		- 绑定选中 label

		  <label for="man">
		   <input type="radio" name="sex" checked id="man" />男
		  </label>

			- for 属性指向 input 的 id 名

		- 表单集和标题 fieldset

		  <fieldset>
		   <legend>基本信息</legend>
		   表单元素
		  </fieldset>

### vscode快捷键

- Ctrl+/ 注释
- Ctrl+S 保存
- Ctrl+Z 撤消
- Ctrl+Y 反撤消
- shift+end:从头选中一行
- shift+home:从尾选中一行
- shift+alt+↓:快速复制一行
- alt+↑或↓:快速移动一行
- alt+鼠标左键:多光标
- ctrl+d:选择相同元素的下一个

### H5新增内容

- 多媒体标签

	- 音频 <audio src=""></audio>

	  <audio src="zy/梦然-少年.mp3" controls autoplay muted loop></audio>

		- controls 控件
		- autoplay 自动播放 ie支持,谷歌和火狐不支持
		- muted 静音播放 火狐设置静音之后,支持自动播放
		- loop 循环播放

	- 视频 <video src=""></video> 

	  <video src="zy/zyx.mp4" controls autoplay loop poster="zy/7.jpg"></video>

		- controls 控件
		- autoplay 自动播放 ie支持,谷歌和火狐不支持
		- muted 静音播放 设置静音之后,支持自动播放
		- loop 循环播放
		- poster 未播放之前显示的图片路径

- 语义化标签

	- 头部 header  
	- 导航 nav
	- 区域 section 
	- 主要内容 main 
	- 文章类 article
	- figure类似与dl 一般和figcaption结合使用 一般放标题
	- mark 标记 内联元素
	- article文章
	- aside侧边栏
	- time时间标签

- 表单

	- type属性

		- email
		- url
		- range滑动条
		- number
		- color
		- time

			- datetime-local当前时间

	- required不为空
	- autocomplete自动提示off/on
	- multiple选择多个
	- placeholder提示信息
	- autofocus自动聚焦
	- pattern正则表达

### SEO优化

- meta标签

  <title>html对seo的优化</title>
  <meta name="title" content="html对SEO的优化">/*不推荐用这个*/
  <meta name="keywords" content="SEO,爬虫，搜索引擎、百度、html优化">
  <meta name="description" content="通过html标签及属性的使用提高网站被爬虫爬取的几率，使用户百度时网站尽量排在前面，提高用户的点击率">
  <meta name="author" content=""> 作者描述

- logo

  <h1>
    //这个href应该是要写线上的首页地址，比项目目录地址要好
  	<a href="https://blog.csdn.net/qq_37291064/article/details/90442991">
  		<img src="images/pagelogo.png" alt="html对seo的优化"/>
  	</a>
  </h1>

	- 给logo图片添加h1标签、a链接连接到首页以及alt

- img标签

	- img标签增加alt属性

- a 标签

	- a标签增加 title 属性，不可以有href="#"这种空指向写法

- h1~h6标签

	- h1要分配给网站名称或给带alt标签的logo使用
	- h2标签用来定义“站点副标题”
	- h3标签用来定义导航栏目名称
	- h4标签用来定义文章列表标题

- 添加robots.txt
- 页面结构清晰

	- 使用语义化标签

- 增加外部链接
- 前后端分离

## CSS

### 概念

- 层叠样式表

### 引入方式

- 行内样式表/内联

  <div style="color: chartreuse;background-color: red;">
    距离美国大选只有十多天时间了
  </div

- 内部样式表

  <head>
   <style>
    p{
     color:red;
    }
   </style>
  </head>

- 外部样式表

  <link rel="stylesheet" href="css/外部样式表.css">
   rel: 关联的文件类型
   href: 引入的css文件路径

	- link
	- @import
	- 区别

		- link属于HTML提供；@import是css提供
		- link和HTML是同时加载；@import是当所有html文件加载后再去加载css
		- @import是ie5以上支持
		- 使用js控制dom改变样式的时候，只能是link引入的样式

- 样式表的选择

	- 行内样式表：样式属性较少
	- 内部样式表：写小案例，做练习，demo
	- 外部样式表：常用，工作开发中，写整页

- 样式表的权重

	- 行内>内部
	- 行内>外部
	- 内部和外部：就近原则，离结构近的样式表优先显示

### 语法

选择器{

css属性名：属性值；

}

### 选择器

- 标签选择器
- id选择器

	- 一个单词小写
	- 多个单词-短线连接或_下划线或驼峰命名
	- 每个标签id名不能重复

- class 类选择器

	- 名称可以重复
	- 多个之间用空格隔开

- 通用选择器
- 伪类选择器：爱恨原则

	-  :link{} 未访问之前
	-  :visited{} 访问之后
	-  :hover{} 鼠标滑过
	-  :active{} 鼠标按下状态

- 群组选择器

  div,
  p,
  a {
  }

- 后代选择器

  ul li {
  }

- css 选择器的权重

  权重值越高,优先级越高,样式就优先显示
  后代选择器的权重是每个选择器的权重值相加
  权重值相同,根据就近原则
  群组选择器的权重是每个选择器自己本身的权重
  继承样式的权重值最低,可以理解为 0,继承样式是不可以覆盖到元素本身自带的样式,如果要修改自带的样式,必须直接选择该元素

	- 行内样式表 1000 （1000）
	- id 选择器 100 （0100）
	- class 类选择器/伪类选择器 10 （0010）
	- 标签选择器 1 （0001）
	- !important 无限大

### 属性

- 文本属性

	- 文本大小：font-size 
	- 文本字体类型：font-family

		- 中文加引号
		- 一个单词不用加引号，多个单词加引号
		- 多个字体之间用逗号隔开，

	- 字体加粗 font-weight

		- normal/bold
		- 100-400  一般; 500 常规字体; 600-900 加粗字体

	- 字体倾斜 font-style

		- normal/italic

	- 文本颜色 color
	- 文本修饰 text-decoration

		- underline:下划线
		- overline 上划线
		- line-through 删除线
		- none 去掉下划线

	- 文本缩进 text-indent

		- 可以设置负数
		- 数值+px
		- 数值+em  一般设置 2em 字体大小的两倍

	- 文本水平对齐 text-align

		- center/left/right
		- justify 两端对齐

	- 行高 line-height

		- 单行文本：将行高和元素高度设置一样的值，实现元素垂直居中
		- 多行文本：实现行与行之间的距离

	- _大小写的转换_ text-transform

		- uppercase 全部大写
		- lowercase 全部小写
		- capitalize 首字母全部大写
		- none 默认值

	- _字符之间的间距_ letter-spacing

		- 英文:加大每个字母之间的距离
		- 中文:加大每个汉字之间的距离
		- 可以设置负数

	- _字间距_ word-spacing
	- 复合写法 font-style font-weight font-size/line-height font-family

		- 常用缩写：font:font-size/line-height font-family；（三者缺一不可顺序不能变）

	- _鼠标样式_ cursor

		- pointer 手型
		- help 帮助
		- wait 等待
		- crosshair 十字

	- vertical-align:(图片支持)

		- baseline:基线(默认值)
		- top/middle/bottom

- 背景属性

	- 背景色 background-color:单词/16 进制/rgb
	- 背景图 background-image:url()

		- 与背景图的区别

			- 图片占位，背景图不占位
			- 背景图一般作为修饰性的图片，图片标签一般作为网页的内容

	- 背景平铺/重复 background-repeat
	- 背景图的位置 background-position:水平 垂直

		- 关键字 水平 left/center/right 垂直 top/center/bottom
		- 只写一个值，第二个值默认为居中

	- 复合写法 background:color url() repeat position;
	- 背景图片固定background-attachment

		- scroll : 　背景图像是随对象内容滚动（默认值）
		- fixed : 　背景图像固定

- 列表属性

	- 列表符号 list-style-type

		- disc 实心圆
		- circle 空心圆
		- square 实心方块
		- none 去掉列表符号

	- list-style-image：url(所使用图片的路径及全称)；
	- list-style-position:outside(外边，默认) inside(里边)；
	- 复合写法 list-style:列表符号 符号位置 图片位置;
	-  **一般只写 list-style:none;去掉列表符号**

- 边框属性

	- 边框宽度 border-width:数值+px
	- 边框样式 border-style:solid(实线)/dotted(点线)/dashed(虚线)/double(双实线)
	- 边框颜色 border-color
	- **复合写法 border: 边框宽度 边框样式 边框颜色;顺序不固定**
	- 去掉边框 border/border-方向:none;

- 浮动

	- float:none/left/right;
	- 应用场景：将纵向排列的元素横向排列
	- 特点

		- 浮动元素会从父元素的边缘开始排列,并且挨着排列
		- 浮动元素会脱离文档，遮挡未浮动的元素，但是不会遮挡文字
		- 父元素宽度放不下的时候，元素会掉下来，且掉到浮动设置的位置
		- 浮动元素前面的兄弟没有浮动，自己浮动的话 是不会超过前面兄弟的  
		- 给在同一行显示的元素添加了浮动之后,宽高是可以生效

- 标准盒模型

	- 盒模型是css布局的基石，它规定了网页元素如何显示以及元素间相互关系。css定义所有的元素都可以拥有像盒子一样的外形和平面空间
	- 内容区(content) 主要由宽度和高度形成，是文字/图片/视频等的显示区域
	- 内填充(padding)

		- 值

			- 一个值 padding:10px 四周
			- 两个值 padding:10px 20px 上下 左右
			- 三个值 padding:10px 20px 30px 上 左右 下
			- 四个值 padding: 10px 20px 30px 40px; 上 右 下 左
			- 单方向 padding-方向(left/right/top/bottom):数值+px;

		- 特点

			- padding是在盒子里面，在盒子与内容之间。
			- 不可以设置负数
			- padding会把盒子撑大，如果想让盒子保持原有的大小，在宽高基础上减掉（宽高不设置不用减）
			- 背景图的位置不受padding的影响
			- **主要用来调整内容区距离盒子边缘的位置**

	- 外边距(margin)

		- 值的设置和 padding 一样
		- 特点

			- 盒子不会被撑大，但是会影响到别人
			- margin 区域不显示背景图/背景色
			- margin 可以设置负数
			- **主要用来调整盒子到盒子之间的距离**
			- margin:auto 实现左右居中

		- bug

			- margin 的重叠

			  给上面的盒子添加下边距，给下面的盒子添加上边距，会产生 margin 的重叠，且取值为最大值,**左右会相加，不会重叠**

				- 解决单独给一个加边距

			- margin 的传递

			  给父元素里面的**第一个子元素**添加**上边距**，会错误加再父元素的身上

				- 给父元素添加边框
				- 给父元素或者该元素加浮动
				- **给父元素添加 overflow:hidden;(溢出隐藏)**
				- 用 padding 来替代

	- 边框border

- css属性继承

	- 可以继承

		- 字体类：字体大小(font-size) 字体倾斜(font-style) 字体加粗(font-weight) 字体类型(font-family)
		- 文本类：文本颜色(color) 文本水平对齐(text-align) 行高(line-height) 字间距(letter-spacing) 词间距(word-spacing) 缩进(text-indent)
		- 列表：list-style-type(列表类型) list-style-position(列表符号的位置) list-style-image:url() list-style

	- 不可继承

		- 宽度(width) 高度(height) 浮动(float) padding(内填充) margin(外边距) 边框(border)

- 溢出属性 overflow

	-  (overflow-x/overflow-y)
	- visible 溢出正常显示 默认值
	- hidden 溢出隐藏
	- scroll 溢出显示滚动条
	- auto 没有溢出之前正常显示 溢出之后显示滚动条
	- **单行文本溢出显示省略号**

		- 设置宽度 width
		- 设置不换行 white-space:nowrap
		- 设置溢出隐藏 overflow: hidden
		- 设置文本溢出显示省略号 text-overflow: ellipsis

- 元素类型的转换

	- display:none/block/inline-block/inline/list-item

- 宽高自适应

	- 宽度自适应

		- 不写宽度 参考父元素
		- 设置百分比 参考父元素
		- min-width/max-width

	- 高度自适应

		- 不写高度或者值为auto 由内容撑开
		- 设置百分比 参考父元素 
		- min-height/max-height
		- 设置一屏页面

			- 当前元素设置高度100% 宽度不设置或者设置100%
			- 给html和body都设置height为100% 

- 高度塌陷

	- 条件：(1)父元素不设置高；(2)子元素浮动
	- 解决：

		- 给父元素设置溢出隐藏 overflow:hidden; （触发BFC）

			- 弊端：会把溢出父元素的内容裁切掉

		- 给浮动元素的后面添加一个块级元素，需要给块级元素添加一个clear(清除浮动) 

		  浮动元素的下添加空的div
		  <style style=clear:both></style>

			- 弊端：会出现大量的空的div，造成代码的冗余

		- 万能清除法

		  高度塌陷的父元素::after{
		   content:"";
		   display:block;
		   clear:both;
		  }

- 伪元素

	- 元素::after{ 给该元素后面添加最后一个孩子
	- 元素::before{ 给该元素后面添加第一个孩子
	- 元素::first-letter{ 选中当前文本的第一个汉字或者字母
	- 元素::first-line{ 选中当前文本的第一行

- 定位 position

	- static 静态 相当于没有定位
	- relative 相对定位

		- 参考物：自己本身
		- 特点: 移走之后依然占位

	- absolute 绝对定位  

		- 参考物：有定位属性(relative/absolute)的祖先元素**子绝父相**
		- 特点

			- 脱离文档流，遮挡住后面的元素，也可以遮挡文字
			- 给内联元素添加绝对定位之后可以变成块级元素
			- 给块级元素设置margin:auto;又设置绝对定位，水平居中会失效

		- 应用场景

			- 实现元素的水平垂直居中方法

				- 给该元素设置绝对定位 
				- 设置top：50%; margin-top:-高度的一半
				- 设置left:50%;margin-left:-宽度的一半

			- 实现元素的水平垂直居中方法2

				- 给该元素设置绝对定位
				- 设置left:0;top:0;right:0;bottom:0
				- 设置margin:auto

			- 图文重叠
			- 二级导航

	- fixed 固定定位

		- 参考物 浏览器窗口
		- 特点

			- 脱离文档流，遮挡住后面的元素，也会遮挡文字
			- 不会跟随滚动条滚动
			- 如果不设置宽度，不会自适应，需要重新设置宽度 width:100%

		- 应用场景

			- **侧边工具栏/头部导航/广告**

	- sticky 粘性定位

		- 参考物 浏览器窗口
		- 没有达到 top 值之前，正常显示，达到 top 值后，类似于固定定位，不会跟随滚动条滚动

- 层级关系z-index

	- 值越大，层级越高，盒子就越在上面
	- 只对定位元素才有作用

- 锚点

	- 在同一个页面中，实现不同板块的跳转

		- #和id属性

		  <a href="#product">产品大全</a>
		  必须是id名
		  <div id="product">产品大全</div>

		- #和name属性

		  <a href="#html">HTML</a>
		  <a name="html"></a>   
		  <h2>HTML超文本标记语言</h2>
		  <p>模拟的段落</p>
		  <p>模拟的段落</p>

- 表格属性

	- 单元格间距 border-spacing:value;

	  单元格间距(该属性必须给table添加) 表示单元格边框之间的距离， 不可取负值

	- 合并相邻单元格边框 border-collapse:separate/collapse;

	  合并相邻单元格边框 (该属性必须给table添加) separate(边框分开)默认值； collapse(边框合并)

	- 无内容时单元格的设置 empty-cells:show/hide;
	- 显示单元格行和列的算法(加快运行的速度)： table-layout:auto/fixed

	  (固定：单元格的宽度不会跟随内容变多而变大)加速渲染的特点

- BFC

	- 块级格式化上下文
	- 触发条件

		- float的值为left/right
		- position的值absolute/fixed
		- display的值inline-block/table-cell(单元格)/table-caption(表格表格)/flex(弹性盒)/inline-flex(弹性盒)
		- overflow的值为hidden/auto/scroll

	- 特点

		-  在BFC的区域，浮动元素的高度会计算在内（解决高度塌陷）
		- BFC的区域不会和浮动盒子重叠（实现两栏布局）

- 计算属性calc

	-  calc(值 - 值);减号旁边必须有空格  width: calc(100% - 300px);  

- css3属性

	- 怪异盒模型 box-sixing: border-box

		- 标准盒模型的宽：width + padding的左右 + border的左右 + margin的左右
		- 怪异盒模型的宽：width + margin的左右

	- 盒子阴影

		- box-shadow: 水平方向偏移 垂直方向偏移 阴影模糊程度 阴影大小 阴影颜色 阴影位置(inset盒子里面);

	- 文本阴影 

		- text-shadow: 水平方向偏移 垂直方向偏移 阴影模糊程度 阴影颜色

	- 背景属性

		- background-size: 宽度 高度;

			- 百分比/数值

				- 一个值: 这个值指定图片的宽度，那么第二个值为auto，可能会拉伸图片（在图片较小时）
				- 两个值: 第一个值指定图片的宽度，第二个值指定图片的高度

			- contain

			  contain，按比例调整背景图片，使得其图片宽高比自适应整个元素的背景区域的宽高比，因此假如指定的图片尺寸过大，而背景区域的整体宽高不能恰好包含背景图片的话，那么其背景某些区域可能会有空白

			- cover

			  cover，按比例调整背景图片，这个属性值跟contain正好相反，背景图片会按照比如自适应铺满整个背景区域。假如背景区域不足以包含背景图片的话，那么背景图片就会被咔嚓。

		- 背景图的原点 background-origin

			- padding-box 背景图从padding区域开始显示
			- border-box 背景图从border区开始显示
			- content-box 背景图从内容区开始显示

		- 背景图的裁切 background-clip

			- border-box 从边框区开始裁切
			- padding-box 从padding区域开始裁切
			- content-box 从内容区开始裁切

	- 边框圆角

		- **圆角 border-radius: px/百分比**

			- 一个值 四周
			- 两个值 对角
			- 三个值 左上角 对角 右下角
			- 四个值 顺时针  

	- 图片边框border-image

		- border-image：路径 偏移 重复

			- border-image-source
边框图片路径
			- border-image-slice
图片的裁切
			- border-image-repeat
平铺(repeat)
铺满(round)
拉伸(stretch)

	- 字体图标库的使用

		- 阿里巴巴iconfont

			- unicode引用
			- class引用
			- symbol引用

		- icommon

	- 多列属性

	  <!DOCTYPE html>
	  <html>
	  <head>
	  <meta charset="utf-8"> 
	  <title>菜鸟教程(runoob.com)</title> 
	  <style> 
	  .newspaper
	  {
	  	-moz-column-count:3; /* Firefox */
	  	-webkit-column-count:3; /* Safari and Chrome */
	  	column-count:3;
	  
	  	-moz-column-gap:40px; /* Firefox */
	  	-webkit-column-gap:40px; /* Safari and Chrome */
	  	column-gap:40px;
	  
	  	-moz-column-rule:4px outset #ff00ff; /* Firefox */
	  	-webkit-column-rule:4px outset #ff00ff; /* Safari and Chrome */
	  	column-rule:4px outset #ff00ff;
	  }
	  </style>
	  </head>
	  <body>
	  
	  <p><b>注意:</b> Internet Explorer 9及更早 IE 版本浏览器不支持 column-count 属性。</p>
	  
	  <div class="newspaper">
	  当我年轻的时候，我梦想改变这个世界；当我成熟以后，我发现我不能够改变这个世界，我将目光缩短了些，决定只改变我的国家；当我进入暮年以后，我发现我不能够改变我们的国家，我的最后愿望仅仅是改变一下我的家庭，但是，这也不可能。当我现在躺在床上，行将就木时，我突然意识到：如果一开始我仅仅去改变我自己，然后，我可能改变我的家庭；在家人的帮助和鼓励下，我可能为国家做一些事情；然后，谁知道呢?我甚至可能改变这个世界。
	  </div>
	  
	  </body>
	  </html>

		- column-count分隔列数
		- column-gap列之间间隔大小
		- column-rule指定列之间的规则：宽度，样式和颜色：
		- break-inside: avoid; 防止瀑布流的折断

	- 透明属性

		- 使用rgba不会模糊里面的文字。 opacity会   
		- rgba/opacity在ie8及以下就不生效,但是ie有兼容写法

		  filter: alpha(opacity=50); opacity等于的值取值未1-100；1相当于之前设置opacity值的0 100相当于1 必须是整数10 20 30

### css3选择器

- 属性选择器

	- [属性名] 拥有该属性名
	- [属性名="属性值"] 属性名和属性值匹配
	- [属性名^="值"] 以该值开头
	- [属性名$="值"] 以该值结尾
	- [属性名*="值"] 包含该值
	- 可以把标签名加在方括号的前面限制元素 eg div[属性名="属性值"]

- 层级选择器

	- 后代选择器 选择器 选择器{} 
	- 子代选择器 选择器>选择器{}
	- 相邻的兄弟 选择器+选择器{} 该元素的后面的相邻的一个兄弟
	- 相邻的兄弟们 选择器~选择器{} 该元素的后面的相邻的兄弟们

- 伪类选择器

	- 结构性的伪类

		- child系列

			- 父元素 子元素:first-child{} 
			- 父元素 子元素:last-child{} 
			- 父元素 子元素:nth-child(n){} 

		- type系列

			- 父元素 子元素:first-of-type{} 
			- 父元素 子元素:last-of-type{} 父元素中的多个该子元素的最后一个
			- 父元素 子元素:nth-of-type(n){} 父元素中的多个该子元素的第几个

	- 目标伪类

		- 目标元素(跳转的板块):target{css属性:css属性值}   

	- 状态伪类

		- 选中可编辑的表单 input:enabled{}
		- 禁止选中的表单 input:disabled{}
		- 获取焦点的表单 input:focus{}
		- 选中状态的表单 input:checked{}
		- 元素::selection{一般改背景色和字体颜色}  

### 高级技巧

- margin负值

	- -1px实现行内块都有边框

		- 1.记每个盒子margin 往左侧移动-1px 正好压住相邻盒子边框
		- 2.鼠标经过某个盒子的时候,提高当前盒子的层级即可.(如果没有定位,则加相对定位,如果有定位,则加z-index)

- 文字围绕浮动元素运用

	- 首先准备一个盒子,里面放文字,再放上一个图片让它左浮动,文字就会围绕图片靠右显示.

- css 三角

  .box1 {
      width: 0;
      height: 0;
      /* 四面三角:哪个三角需要就把其它方向三角的颜色改透明
      border-top: 50px solid green;
      border-right: 50px solid orange;
      border-bottom: 50px solid red;
      border-left: 50px solid pink; */
      /* 直角:底部变为0,再加大上面三角宽度,最后将对应一侧宽度变为0,最后上面三角颜色改为透明 */
      border-color: transparent red transparent transparent;
      border-style: solid;
      border-width: 100px 50px 0 0;
     }

	- 1.盒子宽高为0
	- 2. 四面三角:哪个三角需要就把其它方向三角的颜色改透明
	- 3.直角三角:底部变为0,再加大上面三角宽度,最后将对应一侧宽度变为0,最后上面三角颜色改为透明

## 移动端

### 浏览器的前缀

- 谷歌浏览器 -webkit-
- 欧鹏浏览器 -o-
- 火狐浏览器 -moz-
- ie浏览器 -ms-

### 过渡transtion

**注意:1. 结合hover使用 2. 要加在需要过渡的元素本身身上,不要加在hover里面3. 对元素的display属性过渡不生效,可以通过设置透明度实现**

- ie9以上
- transition-property: 需要过渡的属性
- transition-duration: 过渡需要的时间
- transition-delay: 延迟时间
- transition-timing-function: 过渡效果

	-  linear(匀速)
	- ease(先慢/再快/后慢)
	- ease-in(慢速开始)
	- ease-out(慢速结束)
	- ease-in-out(慢开慢结尾)

- 复合写法 transition: 需要过渡的属性 过渡需要的时间  延迟时间 过渡效果;

### 渐变

- 线性渐变 background-image/background:linear-gradient(方向,颜色值,颜色值)

  0-50是红色的纯色,50-100px 属于渐变范围 100以上蓝色的纯色,对50-100的渐变范围进行重复,重复的次数和宽高相关
   background-image: repeating-linear-gradient(red 50px,blue 100px);

- 重复性的线性渐变 background-image/background:repeating-linear-gradient(方向,颜色值,颜色值)
- 径向渐变 background-image/background:radial-gradient(位置,颜色值,颜色值)     
- 重复性的径向渐变 background-image/background:repeating-radial-gradient(位置,颜色值,颜色值)  
- 移动端兼容写法:  background-image: -webkit-linear-gradient(开始位置，颜色，颜色 );

### 2d变形transform

- 位移

	- x轴位移 transform: translateX(数值+px/百分比) 向右为正,反之
	- y轴位移 transform: translateY(数值+px/百分比) 向下为正,反之
	- transform: translate(x,y)
	- 只设置一个值,代表的水平方向
	- 利用位移实现水平垂直居中

	  p{
	    width:300px;
	    height:200px;
	    position:absolute;
	    left:50%; 参考父元素的宽
	    top:50%; 参考父元素的高
	    transform:translate(-50%,-50%) 参考自己本身的宽和高
	   }

- 旋转

	- x轴的旋转 transform: rotateX(数值+deg); 在3d空间看
	- y轴的旋转 transform: rotateY(数值+deg); 在3d空间看
	- z轴的旋转 transform: rotateZ(数值+deg);

- 缩放

	- x轴的缩放 transform: scaleX(数字) 0相当于隐藏 1 不放大也不缩小 0-1缩小 >1放大
	- y轴的缩放 transform: scaleY(数字)
	- transform: scale(1.5,2);
	- 只写一个值代表的是x轴和y轴

- 倾斜 

	- x轴倾斜 transform:skewX(数值+deg)
	- y轴倾斜 transform:skewY(数值+deg)

- 变形原点

	- transform-origin:水平 垂直

		- **加在原本的元素身上，不要加hover里面**
		- 设置一个值，第二个值默认为居中

### 动画animation

- 1.定义动画@keyframes

  @keyframes 动画名{
    关键帧划分的是时间
    from{ 0%
     css属性: css属性值;
    }
    to{ 100%
     css属性: css属性值
    }
   }
   动画执行时间 5s
   @keyframes 动画名{
    关键帧划分的是时间 百分比是由自己定义的
    0%{} 0s
    20%{} 1s
    30%{} 1.5s
    50%{} 2.5s
    70%{}
    100%{}
   }

- 2.使用动画

	- animation-name: 动画名
	- animation-duration: s/ms 动画执行时间
	- animation-delay: s/ms 动画延迟时间
	- animation-timing-function: 动画的执行效果/steps()步长
	- animation-iteration-count: 数字/infinate(无限循环)
	- **复合写法 animation: 动画名 动画执行时间 动画延迟时间 动画的执行效果 执行次数;**
	- animation-direction：normal(from-to)/reverse(to-from)/alternate(交替运行from-to-from-to) 需要设置次数
	- animation-fill-mode: backwords(停留到第一帧)/forwords(停留到最后一帧) 不要设置无限循环
	- animation-play-state: running/paused(暂停);

### 3d变形

- 位移

	- z轴位移 transform: translateZ(数值+px) 
	- xyz位移 transform: translate3d(x,y,z) 

- 旋转

	- x轴旋转 transform: rotateX(数值+deg)
	- y轴旋转 transform: rotateY(数值+deg)
	- xyz都旋转 transform: rotate3d(a,b,c,d) abc的取值为0或者1 0表示不旋转 1表示旋转 d三个旋转的角度

- 缩放

	- z轴缩放 transform:scaleZ(数值)
	- xyz都缩放 transform:scale3d(x,y,z)  xyz代表缩放倍数，不缩放直接写1

- 景深/透视

	- perspective: 数值+px;要加在变形元素的父元素身上，近大远小

- 形成3d舞台 transform-style:flat(2d)/preverse-3d(3d)
- 背部隐藏:  backface-visibility: hidden;  加在变形元素身上

### 弹性盒(flex)  

- 父元素

	- 形成弹性盒 display:flex;
	- 主轴方向 flex-direction

		- row 默认从左向右
		- row-reverse 从右向左
		- column 从上到下
		- colum-reverse 从下到上

	- **主轴**的对齐方式 justifiy-content

		- flex-start 从主轴的起点开始排列
		- flex-end 从主轴的终点排列
		- space-between 两端对齐
		- space-around 中间的留白的两边的2倍
		- space-evenly 平均分配留白

	- **交叉轴**的对齐方式 align-items

		- stretch 拉伸 交叉轴是纵向的话，看到该效果需要去掉高度，横向去掉宽度
		- flex-start 交叉轴的起点
		- flex-end 交叉轴的终点
		- center 交叉轴的中间 

	- 换行 flex-wrap 

		- nowrap 不换行 默认值
		- wrap 换行

	- **多行**之间的对齐方式 align-content

		- stretch 拉伸  
		- flex-start 从主轴的起点开始排列
		- flex-end 从主轴的终点排列
		- space-between 两端对齐
		- space-around 中间的留白的两边的2倍
		- space-evenly 平均分配留白

- 子元素

	- 单独调整某个元素在交叉轴的对齐方式 align-self

		- stretch 拉伸 交叉轴是纵向的话，看到该效果需要去掉高度，横向去掉宽度
		- flex-start 交叉轴的起点
		- flex-end 交叉轴的终点
		- center 交叉轴的中间

	- 调整某个元素前后的位置 order
	- 分配剩余的空间 flex-grow
	- 压缩 flex-shrink

		- 1 压缩
		- 0 不压缩 
		- 设置在同一行显示且可以滚动

			- 设置子项不压缩
			- 给父元素设置溢出显示滚动条

		- flex: flex-grow(0) flex-shrink(1) flex-basic(auto); 

			- **flex:1** 占满整个剩余空间  

### 布局方案

- 响应式布局

	- 根据不同的设备分辨率，显示不同的样式
	- 媒体查询

	  /* 分辨率>1000 */   
	     @media all and (min-width: 1000px) {
	       body {
	         background-color: blue;
	       }
	     }
	      /* 500-1000 */    
	     @media all and (min-width: 500px) and (max-width:1000px) {
	       body {
	         background-color: green;
	       }
	     }
	     /* 500以下 */   
	     @media all and (max-width:500px) {
	       body {
	         background-color: red;
	       }
	     }

		- 设备类型：all(所有设备)/screen(显示器/笔记本)
		- 媒体特性：最小宽(min-width)/最大宽(max-width)
		- 写法注意：1. and两边必须有空格2. 媒体特性的后面不要加分号 3. 多个媒体特性之间用and连接且空格隔开

	- Bootstrap?未学

- vw+rem布局

	- <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">

		- 视口(移动端/viewport)

			- 布局视口：布局样式参考的视口，一般默认值为980px
			- 可视视口: 设备宽度
			- 完美视口：布局视口的宽=可视视口的宽（width=device-width）

		- initial-scale： 初始的缩放比例（默认设置为1.0）
		- minimum-scale：允许用户缩放到的最小比例（默认设置为1.0）
		- maximum-scale：允许用户缩放到的最大比例（默认设置为1.0）
		- user-scalable：用户是否可以手动缩放（默认设置为no，因为我们不希望用户放大缩小页面）

	- 逻辑像素比(dpr)

		- 物理像素(ps量取的像素)
		- 逻辑像素(css像素)
		- 逻辑像素比(dpr)=物理像素/逻辑像素

			- 320设计图 dpr=1
			- 640/750设计图 dpr=2
			- 1080及以上设计图 dpr=3

	- **单位**

		- em 默认情况下 1em=16px；字体大小设置em单位是参考**父元素的字体大小**；缩进设置em参考的当前元素的字体大小
		- rem 默认情况下 1rem=16px 属性参考的是**根元素html的字体大小**,一般情况下将根元素的大小设置为100px html{font-size:100px}
		- vw(视口的宽)/vh(视口的高)

			- 1vw = 1%视口宽
			- 10vw = 10%视口宽
			- 100vw = 视口宽

		- 100px和vw的转换

			- 750设计图

				- dpr=2,设备宽度为375px
				- 100vw = 375px 
				- 1rem = 100px
				- 1rem = 26.667vw

			- 640设计图 

				- 1rem = 31.25vw 

	- 开发

		- 设置meta标签
		- 确定dpr的值，根据dpr的值，修改图像大小(只修改宽) 图像->图像大小->改宽度即可（单位换成像素）
		- 安装px to rem插件 设置font-size为100px
		- 设置html{font-size:26.667vw} body{font-size:16px}
		- 全部完成后按Alt+Z将px转换为rem单位

- 弹性布局flex
- 流失布局/百分比布局
- rem(等比缩放)布局
- 网格布局

	- 父元素

		- 形成网格 display:grid
		- 形成列 grid-templete-columns

			- 数值+px grid-template-columns: 100px 100px 100px;
			- 百分比  grid-template-columns: 20% 50% 30%;
			- fr  grid-template-columns: 1fr 2fr 1fr;
			- repeat(重复的次数,重复的值)  grid-template-rows: repeat(3, 100px

		- 形成行 grid-templete-rows值的设置和列一样  
		- 划分网页区域 grid-templete-areas

		  父元素{
		     grid-template-areas: "a1 a1 a2 a2" "a1 a1 a2 a2" "a3 a3 a2 a2";
		    }

		- 列和列之间的距离 column-gap:数值+px
		- 行和行之间的距离 row-gap:数值+px 

	- 子元素

		- 指定区域 grid-area: 区域名

		  p:nth-child(1) {
		     grid-area: a1;
		     background-color: pink;
		   }

- 媒体查询+rem+less

  @media screen and (max-width:320px){
     html{
         font-size:12px;
     }
  }
  @media screen and (min-width:321px) and (max-width:375px){
     html{
         font-size:14px;
     }
  }
  @media screen and (min-width:376px){
     html{
         font-size:16px;
     }
  }

- flxible.js+rem
- 混合式布局

### 移动端css初始化

- normalize.css
- 特殊样式

  /*CSS3盒子模型*/
  box-sizing: border-box;
  -webkit-box-sizing: border-box;
  /*点击高亮我们需要清除清除 设置为transparent 完成透明*/
  -webkit-tap-highlight-color: transparent;
  /*在移动端浏览器默认的外观在iOS上加上这个属性才能给按钮和输入框自定义样式*/
  -webkit-appearance: none;
  /*禁用长按页面时的弹出菜单*/
  img,a { -webkit-touch-callout: none; }

### swiper插件使用

