# CSS3 2D 转换

## 新的转换属性
下面的表格列出了所有的转换属性：

属性     | 描述
-------- | ---
transform | 向元素应用 2D 或 3D 转换
transform-origin    | 允许你改变被转换元素的位置

## 2D Transform 方法

函数     | 描述
-------- | ---
matrix(n,n,n,n,n,n) | 定义 2D 转换，使用六个值的矩阵
translate(x,y)   | 定义 2D 转换，沿着 X 和 Y 轴移动元素
translateX(n)	 | 定义 2D 转换，沿着 X 轴移动元素
translateY(n)    | 定义 2D 转换，沿着 Y 轴移动元素
scale(x,y) | 定义 2D 缩放转换，改变元素的宽度和高度
scaleX(n)    | 定义 2D 缩放转换，改变元素的宽度
scaleY(n)   | 	定义 2D 缩放转换，改变元素的高度
rotate(angle)	 |定义 2D 旋转，在参数中规定角度
skew(x-angle,y-angle)    | 定义 2D 倾斜转换，沿着 X 和 Y 轴
skewX(angle) |定义 2D 倾斜转换，沿着 X 轴
skewY(angle)    | 定义 2D 倾斜转换，沿着 Y 轴

找到了一个详解matrix的文章
[理解CSS3 transform中的Matrix(矩阵)](http://www.zhangxinxu.com/wordpress/2012/06/css3-transform-matrix-%E7%9F%A9%E9%98%B5/)
