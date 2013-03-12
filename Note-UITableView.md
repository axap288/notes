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
		
		
*	UITableView效果集

	[KNPathTableViewController](https://github.com/kentnguyen/KNPathTableViewController)

	[ADLivelyTableView](https://github.com/applidium/ADLivelyTableView)

	[JTRevealSidebarDemo](https://github.com/mystcolor/JTRevealSidebarDemo)

	[ViewDeck](https://github.com/Inferis/ViewDeck)

	[TISwipeableTableView](https://github.com/thermogl/TISwipeableTableView)

	[ZKRevealingTableViewCell](https://github.com/alexzielenski/ZKRevealingTableViewCell)

	[JTGestureBasedTableViewDemo](https://github.com/mystcolor/JTGestureBasedTableViewDemo)

	[PSCollectionView](https://github.com/ptshih/PSCollectionView)

	[UITableViewTricks](https://github.com/bharath2020/UITableViewTricks)

	[JTGestureBasedTableViewDemo](https://github.com/mystcolor/JTGestureBasedTableViewDemo)
	
