
---

### 1. 角色及其职责

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201717009.png)

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201718642.png)

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201719108.png)
 ==内存断电就消失，用磁盘文件保证数据安全==


- datanode决定存储能力
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201720698.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201721340.png)


#### 总结

内存+硬盘：架构师的切入点

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201721882.png)
- 第3点：namenode块的存储信息在断点后就不存储了，重启以后由datanode由其汇报
- 因此也需要大量内存
- 单点故障：一个软件有多个不同的模块组成，当中某一个局部出问题导致整体出问题，就是单点故障
- 因此namenode就是单点故障
- 查找文件必须通过namenode




![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201726716.png)



---

### 2. HDFS写流程数据（上传文件）

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201728127.png)


#### （1）主要概念：

- 数据复制与传输问题
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201730038.png)

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201732128.png)



- 数据安全问题
- 两两之间校验

假设机器1给2传送A B C三个符号，那么就要响应 A B C文件对应的响应符号，如果缺了一个，那么上一个节点就会知道哪个没接收到，就会重新传输
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201735078.png)


- 数据存储与备份问题
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201736412.png)


![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201736472.png)
- 机架：不同柜子
- 如果没有机架概念，也有解决策略


#### （2）传输流程：

- 假设有一个客户端想要创建一个请求

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201739667.png)

- 整个数据流分为一股一股的水流
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201744963.png)
![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201744534.png)

![image.png](https://peiyihan-1324725457.cos.ap-beijing.myqcloud.com/Obsidian/202406201745867.png)
- 如果传输过程种发生中断了怎么办呢？
- 在传递过程中，只要最小副本数=1，只要有一个副本上传成功，就算是成功，把这个1返回给namenode；中间失败的节点，由这个成功的副本接着复制












---

### 




