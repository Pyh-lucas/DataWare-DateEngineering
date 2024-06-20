#文件系统 #linux

----
### 文件系统

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172111586.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172112176.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172114584.png)

- linux命令行
- pwd 现在在哪里
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172120194.png)

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172121845.png)
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172122280.png)

- 参考资料
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172126613.png)


----

### linux命令

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172127194.png)

- ls
- ll 是ls -l的快捷命令
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172129494.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172132171.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172223995.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172231258.png)

用这个直接改名，并不移动
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172233845.png)
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172233966.png)


- tail -f 可用来查看数据的采集和收集功能，不需要的时候采用ctrl+c结束
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172234198.png)


- 可以管道套管道
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172237172.png)
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172240271.png)



![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172240591.png)

- 解包的时候也可以通过-C制定解压的目录

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172242166.png)
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172247544.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172248603.png)

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172249470.png)

.tar.gz代表了又打包又压缩，也可简写为.tgz

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172251716.png)


### 时间/系统命令

- 排查内存是否沾满？CPU等资源是否不够了？

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406172253155.png)

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406180900654.png)


 - 使用 -h命令，输出人性化human，以mb等为单位的磁盘使用情况
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406180908013.png)

- jps只能查看java的进程
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406180911583.png)

ps -ef 精准查看进程
ps -ef | grep sshd 配合管道搜索某个进程
kill -9 []某个进程的进程号：杀死某个进程


