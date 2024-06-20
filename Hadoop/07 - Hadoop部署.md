#hadoop

[[06 - Hadoop简介]]

---

### 01 整体概述

- NN/DN/SNN
- RM/NM

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181047919.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181047796.png)


- 逻辑上分离，物理上在一起？
	- 两个集群上互相没有依赖（不是必须你启动/干活，我才能启动/干活），但是物理上我们的进程（一个个框）又布置在一台机器上

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181048215.png)


- MR是计算框架，一个程序

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181049443.png)

---

### 02 分布式模式安装部署（暂时不重要）

 ![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181101229.png)

当你到公司中，给你1000台服务器，搭建hadoop集群和其他软件：需要了解软件和硬件
e.g.
- 某个软件工作需要大内存，安装在一台服务器
- 进程相互冲突，避开

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181101161.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181107894.png)

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181231670.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181233916.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181453627.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406181454868.png)
