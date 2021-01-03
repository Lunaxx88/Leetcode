> Written with [StackEdit](https://stackedit.io/).
 ###  Unit2.面试方法纪要

#### 1. 代码风格
- 嵌套不可以超过三层；
- match number用常量表示；
eg:
if (grid[i][j] == 1){.....
}
Change to :
Define GridType.Wall, 定一个class；
grid[i][j] == GridType.Wall;
.....
- 访问数组确保下标没有越界
- 解耦合：劝分不劝和；

##### Code Quality：使用含义清晰的变量名命名，而不是用注释；
- 通过适当的子函数，并且加空行；

#### 2. 5道题
4+1；
1+3+1；
 
#### 3. 面试评价体系
1. Logicality:
- 是否能够想到一个work solution；
- 是否能够在面试官提示后优化自己的solution；
2. Code Quality, 
- 是否写完；
- 代码风格好不好；
	- 可读性
	- 变量名，函数名命名
	- 空格与空行的正确使用
- 异常检测;
- bug free;
3. Communication;
把面试官当做co-worker,而不是考官；
不要和面试官吵架；
先保证人之间的沟通是顺畅的；

#### 4.面试沟通法则
1. 做题前：沟通清楚（可能面试官要求的跟原来题目的要求不一样），得到面试官肯定，再写代码，写完解释；
- 不要闷头写
- 不要一边写一边解释太多->容易写不完

2. 可以要提示
- 但是先自己想一下，不然会让人觉得不会主动思考问题

3. 不要和面试官吵架

4. 会就会，不会就不会，不要遮遮掩掩，坦诚很重要
- 做过的题就说做过，不要故意说没有做过

#### 5. Others
https://coderpad.io/ 代码运行网站；

#### 6.Lintcode
- 算法能力
- BugFree：题目的提交次数 <=3;
- 题量

#### 7.面试算法和算法的区别
##### 算法面试考点：
最常考：
拓扑排序算法（Topological Sorting）-宽度优先;
二分法（Binary Search）；
哈希表（Hash Table）；
二叉查找树（Binary Search Tree）；
一般常考：
动态规划（Dynamic Programming）；
常考：
分治法（Divide&Conquer）；
堆（Heap）；
考考：
贪心法（Greedy）；
最小生成树算法（Minimum Spanning Tree）-两个贪心法 ；
字典树（Trie）；
并查集（Union Find）;

判断算法考不考：带名字的都不考；

快速排序，归并排序：能够背诵；

| 算法/数据结构 | 考察频率 | 难度 | 刷题数 | 性价比 |
|  ----  |  ----  | ----  | ----  | ----  |
|字符串/模拟法|高|低|20-50|中|
|排序算法|中|中|2-5|高|
|二分法|高|中|10-20|高|
|二叉树/链表|高|低|30-50|高|
|递归/DFS|高|高|20-40|中|
|BFS/拓扑排序|高|中|5-10|超高|
|堆（优先队列）|低|中|5-10|中|
|哈希表|高|中|10-30|高|
|双指针|高|中|10-20|高|
|动态规划|中|高|40-60|低|
|字典树/并查集|中|低|2-5|高|

#### 8.大厂题目
- Google：DP，红黑树 Red-Black Tree， 线段树 Segment Tree；
- Facebook；Amazon；Microsoft；中等难度；
- 其他大中小厂：常见题目；

#### 9.面试类型
- 算法;
- 系统设计System Design（互联网公司多）/ Architecture Design： 一般出现在后端中， API design，数据库;
- 面向对象设计 Objected Oriented Design（软件公司多）-JavaP6的课包含了;
- 行为面试 Behavior Question：跟产品了解，有故事；面试让对方感觉你是唯一；有什么想问的：能够参与到什么工作中，能够做什么准备; 
- 简历面试 Experience Interview;


