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