# UIView
<!-- 
# This file is created from ~/.marboo/source/media/bin/default.init.md
# 本文件由 ~/.marboo/source/media/bin/default.init.md 复制而来
-->

2013-03-12 16:22:51

*	给窗口添加阴影

    	self.view.layer.shadowColor = [UIColorblackColor].CGColor;
    	self.view.layer.shadowOpacity = 0.4f;
    	self.view.layer.shadowOffset = CGSizeMake(-12.0, 1.0f);
    	self.view.layer.shadowRadius = 7.0f;
    	self.view.layer.masksToBounds = NO;
    	selfview.layer.shadowPath = [UIBezierPath bezierPathWithRect:self.view.bounds].CGPath;
