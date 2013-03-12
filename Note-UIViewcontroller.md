#UIViewController



1，说明UIView中 frame与bounds的区别

>frame: UIView实例的位置与大小信息

>bounds: UIView实例的显示内部内容的位置与大小信息 

2，简单讲解UITableView的UITableViewDataSource与UITableViewDelegate的作用

>这两个都是UITableView所需要的协议：

>>UITableViewDataSource，用户定义此tableView的数据获取方法，用来提供数据源
UITableViewDelegate，用来定义显示样式与用户事件相关方法 

3，实现一个带背景UIView的透明渐变动画效果，与移动动画效果

	//动画配制开始
	[UIView beginAnimations:@"animation" context:nil];
	[UIView setAnimationDuration:.5];
	//图片上升动画
	CGRect f = imgView.frame ;
	f.origin.y = 30;
	imgView.frame = f;
	//半透明度渐变动画
	imgView.alpha = 0;
	//提交动画
	[UIView commitAnimations];
	
4，使一个UIImageView的图片视图对象，随着改变它的frame而自适应做拉伸。

	UIImageView *imgView = [[UIImageView alloc] initWithImage:[UIImage imageNamed:@"test.png"]];
	imgView.frame = CGRectMake(0, 0, 200, 200);
	imgView.contentMode = UIViewContentModeScaleToFill;
	
5，使一个UIView对象，在屏幕旋屏后，保持居上位置不变，居左位置自适应，大小不变

	UIImageView *imgView = [[UIImageView alloc] initWithImage:[UIImage imageNamed:@"test.png"]];
	imgView.frame = CGRectMake(20,20, 100, 100);
	imgView.autoresizingMask = UIViewAutoresizingFlexibleTopMargin;
	
6，UIView中所使用的设计模式，越多越好～

7，用UIView的layer中的某个属性，实现一个圆角视图（需要引入Quartz2D库）

	self.view.layer.cornerRadius = 5;
	self.view.clipsToBounds = YES;
8，UIScrollView中contentSize的作用

>用来标识当前内容显示的位置，类型是CGSize 

9，UIViewController与View的关系，在MVC模式中的角色

>一个是Controller层，一个是View层，Controller控制View的显示。 

10，列举几种系统ViewController

`UITabBarController`

`UINavigationController`

`UITableViewController`

`UIImagePickerController`

11，UIView中方法drawRect与layoutSubviews的区别

>当调用view的setNeedsDisplay时，系统异步调用drawRect方法，并配制图形的上下文供在此方法内使用Quartz2D API。
当调用view的setNeedsLayout时，系统异步调用layoutSubviews方法，但不配制图形上下文，只做页面布局使用 

12，UIView中的clipsToBounds属性的作用

>子视图的大小超过父视图时，如果此属值为YES，则把多余的部分隐藏，反之依然。
 
13，如果UIView中的一个子View的位置在此UIView之外，是否还可以获取此UIView的touchesBegan等方法
>获取不到 

14，如何判断用户双击操作

>在touchesBegan方法中，获取UITouch实例:
>>[[touches anyObject ] tapCount]; 

15，在UIView的drawRect方法内，用Quartz2D API绘制一个像素宽的水平直线

	-(void)drawRect:(CGRect)rect{        
	//获取图形上下文    
	CGContextRef context = UIGraphicsGetCurrentContext();        
	//设置图形上下文的路径绘制颜色        
	CGContextSetStrokeColorWithColor(context,[UIColor whiteColor].CGColor);        
	//取消防锯齿        
	CGContextSetAllowsAntialiasing(context, NO);        
	//添加线        
	CGContextMoveToPoint(context, 50, 50);        
	CGContextAddLineToPoint(context, 100, 50);        
	//绘制        
	CGContextDrawPath(context, kCGPathStroke);
	}
16，用UIWebView加载: www.baidu.com

	UIWebView *web = [[UIWebView alloc] initWithFrame:CGRectMake(0, 0, 320, 480)];
	[web loadRequest:[NSURLRequest requestWithURL:[NSURL URLWithString:@"http://www.baidu.com"]]];
	[self.view addSubview:web];[web release];
17，子线程是否也可以修改UIView

>不能，只有主线程有直接修改UI的能力 