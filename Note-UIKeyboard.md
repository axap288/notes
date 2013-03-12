# UIKeyboard
<!-- 
# This file is created from ~/.marboo/source/media/bin/default.init.md
# 本文件由 ~/.marboo/source/media/bin/default.init.md 复制而来
-->

2013-03-12 16:20:07

*   iPhone键盘改变颜色

	只有这2种数字键盘才有效果：
	**UIKeyboardTypeNumberPad**，**UIKeyboardTypePhonePad**
**keyboardAppearance ＝ UIKeyboardAppearanceAlert**
	
	代码如下：

 			NSArray *ws = [[UIApplication sharedApplication] windows];
				for(UIView *w in ws){
					NSArray *vs = [w subviews];
						for(UIView *v in vs){
							if([[NSString stringWithUTF8String:object_getClassName(v)] isEqualToString:@"UIKeyboard"]){
							v.backgroundColor = [UIColor redColor];
							}
						}
				}