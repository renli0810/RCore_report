# lab5
## ch8
1. 哇，逆天，不是说可以不用管之前的实验内容吗，结果sys_get_time()函数卡了我大半天。是的，需要实现sys_get_time(),其他之前的实验则不用实现。
2. 第二个需要注意的点是rust溢出问题，本以为rust能够在溢出的时候panic，但实际效果中并不会，可能是因为我多次强制类型转换了？（也有可能是因为release模式？），蛮痛苦的
3. 算法部分和题目要求一样，只需要注意need、available、allocation在加锁后的变化即可。

## 问答作业
1. 1. 分配的内存，打开的文件
   2. 需要一同回收，线程需要又进程分配资源，进程退出，所有子线程都需要退出。
2. 第二种可能会出错，并没有取消锁

## 荣誉准则
在完成本次实验的过程（含此前学习的过程）中，我未与其他人就（与本次实验相关的）做过交流。但我参考了以下资料 ，还在代码中对应的位置以注释形式记录了具体的参考来源及内容：
https://sjodqtoogh.feishu.cn/docx/ZoqBdmcmAoXi9yxZUkucMmxBnzg
我独立完成了本次实验除以上方面之外的所有工作，包括代码与文档。 我清楚地知道，从以上方面获得的信息在一定程度上降低了实验难度，可能会影响起评分。