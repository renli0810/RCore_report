# lab4
## ch6
1. 将ch5的内容基本移植了过来，修改了一定的布局。
2. 感觉这章好难啊，基本都是参照答案写的。
3. linkat的实现较为简单，首先在根目录里面搜索，得到索引节点，然后索引节点找到block节点，然后再根目录上加入新条目，最后对block节点的link加1即可。但这个最难的地方就是各种各样函数的使用，看得人是头发昏。
4. unlinkat有点麻烦，首先和linkat一样，找到索引节点和block节点，由于可能要删除该文件，因此要把其他目录或者文件保存下来，然后清空该目录，然后再把其他目录或者文件加入该目录，然后就是对于该文件link的判断了，如果是最后一个就要删除该文件，和linkat一样，难点在于各种各样函数的使用。
5. stat就比较简单，但难点在于把记录信息放在那里，一开始放哪都不合适，最后看了答案，惊为天人，醍醐灌顶，放在File trait里面，就会方便很多。

## 简答
1. root_inode起到根目录查询的作用，所有文件的查询操作都需要从根目录开始，从而获得对于的inode，如果损坏，就会无法根据文件名查找文件
2. 在https://missing-semester-cn.github.io/课程中有很多使用管道符的例子：cat lab1.md | wc -l
3. 共享内存，主要思路为使用一个临时文件作为通信区，不同进程只需要访问该文件就可以进行通信，严格来说只需要互斥写就可以。
   
## 荣誉准则
在完成本次实验的过程（含此前学习的过程）中，我未与其他人就（与本次实验相关的）做过交流。但我参考了以下资料 ，还在代码中对应的位置以注释形式记录了具体的参考来源及内容：
https://sjodqtoogh.feishu.cn/docx/ZoqBdmcmAoXi9yxZUkucMmxBnzg
我独立完成了本次实验除以上方面之外的所有工作，包括代码与文档。 我清楚地知道，从以上方面获得的信息在一定程度上降低了实验难度，可能会影响起评分。