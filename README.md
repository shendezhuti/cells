# cellMachine：learn data and representation separate 

# 细胞自动机：学习数据和表现分离

- 死亡：如果活着的邻居的数量<2或>3，则死亡
- 新生：如果正好有三个邻居活着，则新生
- 其他情况保持原状



# 大致关系

- Field相当于一个容器，有place、get、neibor函数。并且存储的是一个个的cell。
- view不去管cell，view只做一件事情->paint，一旦view需要画了，它就从Field去拿数据。
- cell只知道自己怎么画出来。
- Field知道view吗？Filed不知道view！ Field是DATA，只做好管理数据的工作，view相当于是Presentation。
- 最后Field里面的数据都弄好了，我们再由“第三方”即 cellMachine，cellMachine对Field做完操作后，就可以对View发出命令：你现在给我repaint更新下。
- 不去精心设计哪个局部需要更新
- 这样简化了程序逻辑
- 是在计算机运算速度提高的基础上实现的



# 数据与表现分离

- 程序的业务逻辑与表现无关
- 表现可以是图形的也可以是文本的
- 表现可以是当地的也可以是远程的



# 责任驱动的设计

将程序要实现的功能分配到合适的类/对象中去是设计中非常重要的环节



# 网格化

图形界面本身有更高的解析度

但是将画面网格化之后，数据就更容易处理
