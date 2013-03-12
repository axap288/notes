#NSArray

数组内容写入配置文件


	-(void)readWritePlist:(BOOL)readonly
	{

     //取得文档路径
     NSArray *paths = NSSearchPathForDirectoriesInDomains
     (NSDocumentDirectory, NSUserDomainMask, YES);
     NSString *documentsDirectory = [paths objectAtIndex:0];
    
     //生成文件名
     //documents directory:
     NSString *fullFileName = [NSString stringWithFormat:@"%@/arraydata.plist", documentsDirectory];
     NSLog(@"fullFileName: %@",fullFileName);
    
     //创建一数组
     NSMutableArray *array = [[NSMutableArray alloc] init];
     [array addObject:@"One"];
     [array addObject:@"Two"];
     [array addObject:@"Three"];
    
     //将数组内容写到文件内
     [array writeToFile:fullFileName atomically:NO];
         
     //retrieve the array contents.
     NSMutableArray *array2 = [[NSMutableArray alloc] initWithContentsOfFile:fullFileName];
    
     NSLog(@"readWritePlist: %@",array2);
    
     [array2 release];    
	}
	
