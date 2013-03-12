UIButton
-----
*	设置圆角button的代码

		UIButton *btn = [[UIButton alloc]initWithFrame:btnFrame];
		// 设置圆角半径
		btn.layer.masksToBounds = YES;
		btn.layer.cornerRadius = 4;
		//还可设置边框宽度和颜色
		btn.layer.borderWidth = 1;
		btn.layer.borderColor = [UIColor darkGrayColor].CGColor;
		
*	UIButton上的文字左对齐
> Btn.contentHorizontalAlignment =UIControlContentHorizontalAlignmentLeft;


*	左边距调整
> Btn.contentEdgeInsets =UIEdgeInsetsMake(0,10,0,0);