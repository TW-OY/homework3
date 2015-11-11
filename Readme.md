#1、position 四个属性
+ absolute 	以非static的祖先作为参照
+ relative	以自身为参照
+	fixed		以浏览器为参照
+	static		以窗口为参照

#2、响应式页面设计	

##设计模式
1. Mostly fluid    流体式布局
2. Column drop
3. Layout shift	灵活布局   <http://foodsense.is>
4. 另外两种不重要。

##设计方法：

###百分比

	 width:10%

###Flex(不常用)

 	display:flex
 	flex-flow:
 	.main{
 		width:xxpx}
 	.left{
 		flex:1}	#比例 设成2  则比设成1大一倍

这样设置的 中间大小固定为xx像素不变，两边大小可浮动

###媒体查询（主流）
####设计出发
针对不同设备 来设计两套css

####设计实现
媒介查询-Media Queries
        
CSS3 Media Query-媒介查询是响应式设计的核心。它根据条件告诉浏览器如何为指定视图宽度渲染页面。

1. 当视图宽度为小于等于980像素时，如下规则将会生效。基本上，我会将所有的容器宽度从像素值设置为百分比以使得容器大小自适应。![text1](http://7xn8xc.com1.z0.glb.clouddn.com/980px-or-less.png)
 
2. 然后为小于等于700像素的视图指定#content和#sidebar的宽度为自适应并且清除浮动，使得这些容器按全宽度显示。![text2](http://7xn8xc.com1.z0.glb.clouddn.com/700px-or-less.png)
 
3. 对于小于等于480像素（手机屏幕）的情况，将#header元素的高度设置为自适应，将h1的字体大小修改为24像素并隐藏侧边栏。![text3](http://7xn8xc.com1.z0.glb.clouddn.com/480px-or-less.png)
 
你可以根据你的喜好添加足够多的媒介查询。我在示例中仅仅展示了3个媒介查询。媒介查询的目的在于为指定的视图宽度指定不同的CSS规则，来实现不同的布局。媒介查询可以写在同一个或者单独的样式表中。

***

#推荐阅读
响应式网页设计简单入门  <http://www.cnblogs.com/Wayou/p/responsive_design_step_by_step.html>

Responsive Design with CSS3 Media Queries 243  <http://webdesignerwall.com/tutorials/responsive-design-with-css3-media-queries>