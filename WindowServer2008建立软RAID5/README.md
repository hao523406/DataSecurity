# WindowServer2008建立软RAID 5实验

## 建立 RAID5

1. 虚拟机已经安装好WindowServer2008，虚拟机设置添加至少3个磁盘（因为RAID5至少需要3个磁盘）。

    

2. 将磁盘设为联机并进行初始化（选择MBR与其他磁盘一致），再转化为动态磁盘。

    !["转换为动态磁盘"](img/转换为动态磁盘.png)

  

3. 新建RAID-5卷。

    !["新建RAID-5卷-1"](img/新建RAID-5卷-1.png)
    
    !["新建RAID-5卷-2"](img/新建RAID-5卷-2.png)
    
    !["新建RAID-5卷-3"](img/新建RAID-5卷-3.png)



4. 新建测试文件。
	
	!["新建测试文件"](img/新建测试文件.png)
	



## RADI5的丢失与修复

1. 关闭虚拟机，移除一个磁盘，并添加一个新的磁盘作为修复的磁盘。启动虚拟机，并初始化这个磁盘。

    !["新增修复磁盘"](img/新增修复磁盘.png)



2. 发现移除的磁盘当然丢失了，并且RAID5已被损坏。但是保存的文件依然完好无损。
	
	!["RAID5丢失"](img/RAID5丢失.png)
	
	!["测试文件完好"](img/测试文件完好.png)
	
	
	
3. RAID5的修复：点击修复卷，选择新增的磁盘，进行修复。
	!["RAID5修复-1"](img/RAID5修复-1.png)
	
	!["RAID5修复-2"](img/RAID5修复-2.png)
	
	!["RAID5修复-3"](img/RAID5修复-3.png)
	
	!["RAID5修复-4"](img/RAID5修复-4.png)

