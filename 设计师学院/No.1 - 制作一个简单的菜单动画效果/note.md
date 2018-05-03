# CSS3过渡属性

- 属性	描述	CSS
		transition	简写属性，用于在一个属性中设置四个过渡属性。	
		transition-property	规定应用过渡的 CSS 属性的名称。	
		transition-duration	定义过渡效果花费的时间。默认是 0。	
		transition-timing-function	规定过渡效果的时间曲线。默认是 "ease"。	
		transition-delay	规定过渡效果何时开始。默认是 0。
# 贝塞尔曲线用法
- 需用 transition-timing-function 来规定过渡曲线效果

- [贝塞尔曲线制作网站](http://cubic-bezier.com/#1,-0.87,0,1.59)

		 linear                        规定以相同速度开始至结束的过渡效果（等于 cubic-bezier(0,0,1,1)）。
		 ease                          规定慢速开始，然后变快，然后慢速结束的过渡效果（cubic-bezier(0.25,0.1,0.25,1)）。
		 ease-in                       规定以慢速开始的过渡效果（等于 cubic-bezier(0.42,0,1,1)）。
		 ease-out                      规定以慢速结束的过渡效果（等于 cubic-bezier(0,0,0.58,1)）。
		 ease-in-out                   规定以慢速开始和结束的过渡效果（等于 cubic-bezier(0.42,0,0.58,1)）。
		 cubic-bezier(n,n,n,n)         在 cubic-bezier 函数中定义自己的值。可能的值是 0 至 1 之间的数值
		 如：transition-timing-function: cubic-bezier(1,-0.87,0,1.59);
		 

# HTML DOM classList 属性
[ classList 属性](http://www.runoob.com/jsref/prop-element-classlist.html)

语法
element.classList

## 方法
方法   | 描述
-------- | ---
add(class1, class2, ...) | 在元素中添加一个或多个类名。如果指定的类名已存在，则不会添加
contains(class)    | 返回布尔值，判断指定的类名是否存在。可能值：true - 元素包已经包含了该类名false - 元素中不存在该类名
item(index)     | 返回类名在元素中的索引值。索引值从 0 开始。如果索引值在区间范围外则返回 null
remove(class1, class2, ...)     | 移除元素中一个或多个类名。注意： 移除不存在的类名，不会报错。
toggle(class, true|false)   在元素中切换类名。第一个参数为要在元素中移除的类名，并返回 false。 如果该类名不存在则会在元素中添加类名，并返回 true。 第二个是可选参数，是个布尔值用于设置元素是否强制添加或移除类，不管该类名是否存在。例如：移除一个 class: element.classList.toggle("classToRemove", false); 添加一个 class: element.classList.toggle("classToAdd", true);注意： Internet Explorer 或 Opera 12 及其更早版本不支持第二个参数。

下面是代码部分

HTML

	<div class="text-center">
				<h1 id="text" >前端学院<span id="underline"></span></h1>
				<button class="btn"  onclick="changeStyle()">切换样式</button>
	</div>
	
CSS

	h1{
	transition: color 0.2s linear;
	-moz-transition: color 0.2s linear;    /* Firefox 4 */
	-webkit-transition: color 0.2s linear;    /* Safari 和 Chrome */
	-o-transition: color 0.2s linear;    /* Opera */
	}
	span{
		width: 0;
		display: block;
			/*边框粗细颜色*/
		border-bottom: 4px #1C86EE solid;
		transition:width 0.5s;
		margin: 0 auto;

	}
	.text{
		/*过度完成后的文本颜色*/
		color:#1C86EE;
	}
	.text-center{
		text-align:center;
	}
	.underline{
		/*下划线长度*/
			width:140px;
	}
	.btn{
		margin-top: 60px;
		outline-style:none;
		background-color:white;
			border-style:solid;
			border-width:2px;
			border-radius:10px;
			font-size:26px;
	}
	
JavaScript

	var changed = false;
	function changeStyle(){
		if (changed == false) {
			document.getElementById("underline").classList.add('underline');
			document.getElementById("text").classList.add('text');
			changed = true;
		}else{
			document.getElementById("underline").classList.remove('underline');
			document.getElementById("text").classList.remove('text');
			changed = false;
		}

	}
