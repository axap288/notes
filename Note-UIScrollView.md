UIScrollView
----
*	xib里加入了一个scrollview，要求scrollview里的内容是很长的，可以滚动的。但是运行起来scrollview并没有滚动起来，怎么解决？
解决方法如下：

	在scrollview的inspector里做如下设置
	
	|Key Path|Type|Value|
	|--------|----|-----|
	|ContentSize|Size|{320,500}|

