*	设置圆角button的代码



		UIButton *btn = [[UIButton alloc]initWithFrame:btnFrame];
		// 设置圆角半径
		btn.layer.masksToBounds = YES;
		btn.layer.cornerRadius = 4;
		//还可设置边框宽度和颜色
		btn.layer.borderWidth = 1;
		btn.layer.borderColor = [UIColor darkGrayColor].CGColor;
		
*	点击tableview中的cell，取消蓝色选中框的方法:

		[tableView deselectRowAtIndexPath:indexPath animated:YES];
		
*	pushViewController但不显示tabbar的方法：
	
		在pushViewController前，将要push的view controller设置hidesBottomBarWhenPushed属性
 		citysCtrl.hidesBottomBarWhenPushed = YES;

*	xib里加入了一个scrollview，要求scrollview里的内容是很长的，可以滚动的。但是运行起来scrollview并没有滚动起来，怎么解决？
解决方法如下：

	在scrollview的inspector里做如下设置
	
	|Key Path|Type|Value|
	|--------|----|-----|
	|ContentSize|Size|{320,500}|
	




*	设置UItableViewCell的背景为透明的方法：

		-(void)tableView:(UITableView *)tableView willDisplayCell:(UITableViewCell *)cell forRowAtIndexPath:(NSIndexPath *)indexPath
		{
		UIView *backView = [[[UIViewalloc]initWithFrame:CGRectZero] autorelease];
    	backView.backgroundColor = [UIColorclearColor];
    	cell.backgroundView = backView;
		}




*	UILabel上的文字换行
	
		UILabel*label;

		//设置换行
		label.lineBreakMode = UILineBreakModeWordWrap; 
		label.numberOfLines = 0;

		换行符还是\n
		比如NSString * xstring=@"lineone\nlinetwo"
		记得要把label的高度设置的足够显示多行内容。















*	iphone中怎么获得application delegate的对象？
>ClassDelegate *a = (ClassDelegate *)[[UIApplication sharedApplication] delegate];



*	通过.plist文件加载数组

		NSString *path = [[NSBundlemainBundle] pathForResource:@"content_iPhone"ofType:@"plist"];
		NSArray *contentList = [NSArrayarrayWithContentsOfFile:path];



