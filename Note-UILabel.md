# UILabel
<!-- 
# This file is created from ~/.marboo/source/media/bin/default.init.md
# 本文件由 ~/.marboo/source/media/bin/default.init.md 复制而来
-->

2013-03-12 16:17:49

*	UILabel上的文字换行
	
		UILabel*label;

		//设置换行
		label.lineBreakMode = UILineBreakModeWordWrap; 
		label.numberOfLines = 0;

		换行符还是\n
		比如NSString * xstring=@"lineone\nlinetwo"
		记得要把label的高度设置的足够显示多行内容。
