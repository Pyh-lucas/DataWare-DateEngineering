
### 1. 文件系统&分布式文件系统

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201612884.png)
- 作为用户只需要关注抽象出来的树形结构结课，底层的位置和数据不需要关注，由文件系统完成



传统的单机文件系统
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201613155.png)


- 元数据和数据的概念
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201614220.png)

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201615774.png)

- 1台机器放不下

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201615040.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201616900.png)
- 在数据量大的情况下，数据移动过来进行计算就已经很复杂了
- 其次，如果能数据不动而把程序发过去就好了，但是2实现不了

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201617738.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201617985.png)


---

一款成熟的分布式存储系统应该包含的属性：
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201619053.png)

- 分布式存储
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201620049.png)


- 元数据记录
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201621573.png)


- 数据切块存储
- 数据在物理上存储的机器不同
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201623528.png)


- 一份数据放在多个集群上面
- 一个地方找不到，可以找其他设备上的
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201624754.png)


**==分布式文件存储的优点==**
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201626850.png)


---

### 2. HDFS简介与设计目标

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201627629.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201628511.png)

- HDFS client是用户，构成一主多从的分布式架构
- 虽然底层运行在不同机器上，但对外提供一个访问入口（方便管理），由namenode来管理
- 入口就是目录树结构，用户接受起来和传统系统体感差不多，但是实际上放在多台不同的机器上，而且是分块存储，落在每台机器的磁盘上


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201633641.png)



![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201633628.png)
- 延迟高，但是保证了吞吐量

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201635170.png)

- 一次写入，多次读取：设计者认为，大数据一旦产生，后续就很少修改了，那么索性就不支持文件修改了


### 3. 应用场景

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201639044.png)

### 4. 重要特性

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201639507.png)
- rack机柜，机房中计算机构成的机架；
- 主从：一个namenode，多个datanode
- 数据是小方框/分布存储；replication冗余存储
- namenode中记录元数据，维护元数据和树结构
- 拥有统一的目录树结构

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201642424.png)



![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201643980.png)
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201645024.png)
- 1+2副本 
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201645782.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201646396.png)

- namespace就是具有层次型的组织结构
- namenode之所以和datanode名字上区分，就是因为namenode要管理namespace，datanode就是存储data的
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201647196.png)



![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201650534.png)


