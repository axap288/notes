# NSString
<!-- 
# This file is created from ~/.marboo/source/media/bin/default.init.md
# 本文件由 ~/.marboo/source/media/bin/default.init.md 复制而来
-->

2013-03-12 16:21:13

*	获取当前日期字符串：

		-(NSString*)getCurrentDateString {
		NSDateFormatter *format = [[[NSDateFormatteralloc] init] autorelease];
		[format setDateFormat:@"dd/MM/yyyy HH:mm"];
		NSDate *now = [[[NSDatealloc] init] autorelease];
		return [NSStringstringWithFormat:@"Last updated: %@",[format stringFromDate:now]];
		}



1，把一个整数，转换成一个NSString
>[NSString stringWithFormat:@"%d",3];

2，比较两个NSString是否相等
>[@"test" isEqualToString:@"test"];

3，@"abcdefg"，截取第两个字符开始的三个字符

>[@"abcdefg" substringWithRange:NSMakeRange(1, 3)]

5，NSString , NSMutableString的区别

>NSString, 不可修改字串
>NSMutableString，可修改字串 

6，计算一个字串在指定宽度，指定字体情况下，需要渲染的实际像素高度

>[@"abcdefg" sizeWithFont:[UIFont systemFontOfSize:12] constrainedToSize:CGSizeMake(100, INT32_MAX)].height

7，用HTTP协议，获取www.baidu.com网站的HTML数据

>[NSString stringWithContentsOfURL:[NSURL URLWithString:@"http://www.baidu.com"]]