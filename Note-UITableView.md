UITableView
----
*	设置UItableViewCell的背景为透明的方法：

		-(void)tableView:(UITableView *)tableView willDisplayCell:(UITableViewCell *)cell forRowAtIndexPath:(NSIndexPath *)indexPath
		{
		UIView *backView = [[[UIViewalloc]initWithFrame:CGRectZero] autorelease];
    	backView.backgroundColor = [UIColorclearColor];
    	cell.backgroundView = backView;
		}
*	点击tableview中的cell，取消蓝色选中框的方法:

		[tableView deselectRowAtIndexPath:indexPath animated:YES];