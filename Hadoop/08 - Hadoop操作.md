
---

### 1. 启动

- 麻烦，但能精确的控制每一个集群
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201534478.png)

- 一键启动
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201535752.png)

- - jps的意思是查看java进程
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201539072.png)

==- 下一次启动的时候，使用start-all.sh来一键启动==

**如何保证集群启动是正常的？**

如果发现一个角色过一会没了（进程闪退），用第二种方法看日志排查，通常是配置有问题
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201541757.png)

- 官方针对集群给出了两个web页面

输入nodeX:9870
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201543862.png)

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201546600.png)

- yarn的界面
node1:8088
显示当前在我们的集群当中，有哪些程序正在执行

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201549650.png)


### 2. HDFS操作（文件系统-存储/上传/下载）

- 两种操作方式
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201521898.png)



![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201556998.png)

也可通过文件UI界面进行操作
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201559126.png)

- 总结：
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201559237.png)

- 计算+资源管理系统

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201600750.png)


resourse manager是yarn的主角色，程序运行找资源

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201604155.png)
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201606876.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201606498.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201609981.png)

- MR不适合处理小数据