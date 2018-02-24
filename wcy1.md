### 1、html

Hyper Text markup language 超文本标记语言

###2、标记/标签

####1）行标签

​	不会独占一行

​	不能设置宽高

​	a (href title target)、 span、 i、 em、 b、 strong、 time、 address、 progress（进度）

####2）块标签
​	独占一行 

​	div、h1-h6、p、pre、ul、li、ol、dl、dt、dd、header、footer 、section、 main、 video 、audio(视频、音频的播放）  form

####3）行内块级标签

​	不会独占一行，可设置宽高

​	img（src alt title width height border） input textarea  select  option  fieldset

###3、实体(双击实体名称)
| 显示结果 | 描述            | 实体名称           | 实体编号    |
| :--- | ------------- | -------------- | ------- |
|      | 空格            | &nbsp;         | &#160;  |
| <    | 小于号           | &lt;           | &#60;   |
| >    | 大于号           | &gt;           | &#62;   |
| &    | 和号            | &amp;          | &#38;   |
| "    | 引号            | &quot;         | &#34;   |
| '    | 撇号            | &apos; (IE不支持) | &#39;   |
| ￠    | 分（cent）       | &cent;         | &#162;  |
| £    | 镑（pound）      | &pound;        | &#163;  |
| ¥    | 元（yen）        | &yen;          | &#165;  |
| €    | 欧元（euro）      | &euro;         | &#8364; |
| §    | 小节            | &sect;         | &#167;  |
| ©    | 版权（copyright） | &copy;         | &#169;  |
| ®    | 注册商标          | &reg;          | &#174;  |
| ™    | 商标            | &trade;        | &#8482; |
| ÷    | 除号            | &divide;       | &#247;  |
| ×    | 乘号            | &times;        | &#215;  |

###4、表单：提交
​	form  （action提交地址、method提交方式）
​	表单控件:input 

​	控件类型:（text password radio checkbox file文件 hidden submit提交按钮 reset button）（email url地址、date、week month time datetime-local number range search color)

  	属性:（type  name当前表单的值，用于前后台数据对接 value默认值 readonly只读 disable checked selected max length）（require placeholder）

### 5、引用方式

  行内样式 style=“width：100px； higth：100px；”
  嵌入样式 <style>.ine{} </style>
  外部样式  <link rel=‘stylesheet’ href=“”>
  引入样式 @import url（”hhh.css“）；

### 6、选择器

 标签选择器; div body a 
 类名选择器 ：.one
 id选择器：#one
 后代选择器 ul li、.one
 群组选择器 .one,.two
 交叉选择器 ul.one  .one.two
 伪类选择器 ：hover（交互）、：active（鼠标 link ：visited
 子选择器   div>a   .one>.two{前一个元素的子元素}
 同级选择器 div+p div-p
 根据位置选择第几个子元素 ：nth-child（2n-1）第二个子元素                      ：first-child    ：last-child 

​                                                ：nth-last-child（2）                                            ：only-child父元素唯一子元素

​                                                 ：nth-of-type（2）同类型第二个                         ：last-of-type  

​                                                  ：nth-of-type（2）同类型第二个                          ：last-of-type 

​                                                   ：nth-last-of-type（）                          ：only-of-type（2）同类型第二个  ：first-of-type                

 属性选择器 【data】 【data=a】 【data^=a】【data$=a】 【data*=a】
 :before   :after
 被选中的表单  :checked 
 ：target  ：root

### 7、属性

#### 布局：

width  height  margin  padding  float  position  box-sizing：border-box；（移动端）、display（行块转化）、left、right、投票、bottom、z-index

#### 样式：

background、background-color、background-image、background-repeat、background-position、background-attachment、border、 border-width、border-style、border-color、background-clip、background-origin、background-size、border-image、border-radius圆角：10px 20px；、box-shadow 阴影、outline轮廓线，不占位置、outline-offset轮廓线偏移

#### 径向渐变

 background-image: linear-gradient(to left,red,orange,yellow,green,cyan,blue,plum); 

repeating-linear-gradient     radial-gradient()、repeating-radial-gradient()

#### 文字 

font-size、text-indent缩进、text-align、text-decoration、line-height、word-break、letter-apacing字间距、vertical-align垂直对齐、

#### 动画

 transition 过度动画    transition-property过度属性 、 transition-duration过度时间、 transition-timing-function持续的时间、 transition-delay动画延迟、

@keyframe    animation

#### 转化

transform、transform -origin、transform -style、perspective、perspective-origin、translate、 translateX 、 translateY、translate3d()、rotate（）、rotateX（）、scaleX放大缩小、skew（）、skewX()斜切、skewY()、matrix（）居正、

#### table

	<title>表格</title>
	<style>
		.mytable{
			width: 600px;
			height: 300px;
			border: 1px solid red;
			margin: 0 auto;
			/*布局方式，单元格固定*/
			table-layout:fixed;
			/*文字强制换行*/
			word-break: break-all; 
			text-align: center;
			/*为表格设置合并边框模型，默认会被分开*/
			border-collapse: collapse;
		}
		.mytable td,th{
			border: 2px solid yellow;
			width: 200px;
		}
		.mytable tr:first-child{
			height: 150px;
		}
		caption{
			font-size: 36px;
		}
		.mytable2{
			border-collapse: collapse;
			border: none;
		}
		.mytable2 td{
			border: none;
			border-bottom: 1px solid red;
		}
		.mytable2 tr:last-child td{
			border: none;
		}
	</style>
	<body>
	<table width="600" height="300" border="1" cellpadding="0" align="center" bgcolor="#eee" >
		<tr height="150" align="center" valign="top" bgcolor="red">
			<td width="300" align="left" valign="bottom" bgcolor="pink">展示的内容</td>
			<td>展示的内容</td>
			<td>展示的内容</td>
		</tr>
		<tr>
			<td>展示的内容</td>
			<th>展示的内容</th>
			<th>展示的内容</th>
		</tr>
	</table>
	<!-- valign="center"垂直居中 td与th区别：th文字自动居中（标题） -->
	<table class="mytable">
		<caption>成绩表</caption>
		<tr>
			<!-- 行的合并 -->
			<td colspan="3">展示的内容ddddddddddddddddddd</td>
			<!-- <td>展示的内容</td>
			<td>展示的内容</td> -->
		</tr>
		<tr>
			<td>展示的内容</td>
			<td>展示的内容</td>
			<!-- 列的合并 -->
			<td rowspan="2">展示的内容</td>
		</tr>
		<tr>
			<td>展示的内容</td>
			<td>展示的内容</td>
		</tr>
		<tr>
			<td>展示的内容</td>
			<td>展示的内容</td>
			<!-- 单元格的拆分 -->
			<td>
				<table class="mytable2">
					<tr>
						<td>qfsfs</td>
					</tr>
					<tr>
						<td>wsfsf</td>
					</tr>
					<tr>
						<td>efsfs</td>
					</tr>
				</table>
			</td>
		</tr>
	</table>
	</body>
#### 响应式

	<style>
	.box{
			width: 1000px;
			height: 300px;
			margin: 0 auto;
		}	
		.item{
			/*width: 50%;*/
			width: 33.33%;
			height: 300px;
			background-color: red;
			float: left;
		}
		.item:nth-child(2){
			background-color: yellow;
		}
		/*媒体查询  根据当前设备的分辨率来控制某一部分是否显示*/
		/*阀值 min-width:   max-width:*/
		@media screen and (max-width: 1040px){
			.box{
				width:100%;
			}
		}
	</style>
	<div class="box">
		<div class="item"></div>
		<div class="item"></div>
		<div class="item"></div>
	</div>	
#### 流式布局

	<title>流式布局,内容跟着屏幕的变化而变化</title>
	<style>
		*{
			box-sizing: border-box;
		}
		.container{
			width: 1200px;    
			height: auto;
			margin: 0 auto;
		}
		.item{
			width: 25%;
			height: 300px;
			float: left;
			background-color: yellow;
			text-align: center;
			line-height: 300px;
			color: red;
			font-size: 36px;
			border: 10px solid #333;
		}
		@media screen and (max-width: 1180px){
			.container{
				width: 900px;				
			}
			.item{
				width: 33.3333%;
			}
			.item:last-chlid{
				display: none;
			}
		}
		@media screen and (max-width: 960px){
			.container{
				width: 600px;
			}
			.item{
				width: 50%;
			}
		}
		@media screen and (max-width: 640px){
			.container{
				width: 300px;
			}
			.item{
				width: 100%;
			}
		}
	</style>
	<div class="container">
		<div class="item">1</div>
		<div class="item">2</div>
		<div class="item">3</div>
		<div class="item">4</div>
	</div>
#### 流式布局+响应式

	<title>流式布局+响应式</title>
	<style>
		*{
			box-sizing: border-box;
		}
		.container{
			width: 1200px;    
			height: auto;
			margin: 0 auto;
		}
		.item{
			/*高是宽的一半的设置*/
			width: 50%;
			height: auto;
			float: left;
			background-color: skyblue;
			text-align: center;
			color: red;
			font-size: 36px;
			border: 10px solid #fff;
			padding-top: 25%;
			position: relative;
		}
		.content{
			width: 100%;
			height: 100%;
			position: absolute;
			top: 0;
			left: 0;
		}
		@media screen and (max-width: 1200px){
			.container{
				width: 1000px;				
			}
		}
		@media screen and (max-width: 1080px){
			.container{
				width: 600px;
			}
			.item{
				width: 100%;
				padding-top: 50%;
			}
		}
		@media screen and (max-width: 640px){
			.container{
				width: 100%;
			}
			.item{
				width: 100%;
			}
		}
	</style>
	<div class="container">
		<div class="item">
			<div class="content">ddd</div>
		</div>
		<div class="item"></div>
		<div class="item"></div>
		<div class="item"></div>
	</div>
#### 动画

	<title>动画</title>
	<style>
		@keyframes rotate {
			/*from{}to{}*/
			0%{
				transform: rotate(0deg);
				}100%{
					transform: rotate(180deg);
				}
			}
		.box{
			width: 300px;
			height: 300px;
			background-color: red;
			/* 动画名字，与上保持一致 */
			animation-name: rotate;
			/* 过度时间 */
			animation-duration: 5s;
			/* 匀速转动 */
			animation-timing-function: linear;
			/* 延时 */
			animation-delay: 2s;
			/* 无限次运动 */
			animation-iteration-count: infinite;
			/* 顺逆时针交替转 */
			animation-direction: alternate;
			/* 转一定角度停下来时返回的角度*/
			animation-fill-mode: forwards;
			animation-fill-mode: backwards;
		}
		div:hover{
			/*鼠标经过时暂停*/
	        animation-play-state: paused;
		}
	</style>
	
	<div class="box">dd</div>

