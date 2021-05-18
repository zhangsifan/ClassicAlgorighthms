# 目录

<table border=0.1 cellspacing=0 width="90%">
<tr>
    <td width="200">算法</td>
    <td width="200">内容</td>
    <td width="300">实现</td>
</tr>
<tr>
    <td rowspan=11><a href="#数据结构">数据结构</a></td>
    <td rowspan=4><a href="#表">表</a></td>	
    <td>单链表</td>
</tr>
<tr>
	<td>双向链表</td>
</tr>
<tr>
	<td>哈希表</td>
</tr>
<tr>
	<td>最小栈</td>
</tr>
<tr>
    <td rowspan=5><a href="#树">树</a></td>	
    <td>二叉树</td>
</tr>
<tr>
	<td>字典树</td>
</tr>
<tr>
	<td>红黑树</td>
</tr>
<tr>
	<td>二叉平衡树</td>
</tr>
<tr>
	<td>堆</td>
</tr>
<tr>
    <td rowspan=2><a href="#图">图</a></td>	
    <td>并查集</td>
</tr>
<tr>
	<td>无向图</td>
</tr>
<tr>
    <td rowspan=16><a href="#经典算法">经典算法</a></td> 
    <td rowspan=9><a href="#排序算法">排序算法</a></td> 
    <td>冒泡排序</td>
</tr>
<tr>
	<td>选择排序</td>
</tr>
<tr>
	<td>插入排序</td>
</tr>
<tr>
	<td>普通&nbsp;/&nbsp;3向切分&nbsp;快速排序</td>
</tr>
<tr>
	<td>递归&nbsp;/&nbsp;非递归&nbsp;归并排序</td>
</tr>
<tr>
	<td>计数 /&nbsp;桶排序</td>
</tr>
<tr>
	<td>堆排序</td>
</tr>
<tr>
	<td>希尔排序</td>
</tr>
<tr>
	<td>基数排序</td>
</tr>
<tr>
    <td rowspan=2><a href="#搜索算法">搜索算法</a></td>	
    <td>二分查找</td>
</tr>
<tr>
	<td>二分查找左右边界</td>
</tr>
<tr>
    <td rowspan=3><a href="#回溯算法">回溯算法</a></td>	
    <td>子集</td>
</tr>
<tr>
	<td>组合</td>
</tr>
<tr>
	<td>全排列</td>
</tr>
<tr>
    <td rowspan=2><a href="#位运算">位运算</a></td>	
    <td>二进制中1的数量</td>
</tr>
<tr>
    <td>翻转二进制表示</td>
</tr>
<tr>
	<td><a href="#LeetCode">LeetCode</a></td>	
	<td></td>	
	<td></td>
</tr>
<tr>
	<td><a href="#LeetCode">数据结构思维导图</a></td>	
	<td></td>	
	<td></td>
</tr>
<tr>
	<td><a href="#LeetCode">各排序算法时间复杂度</a></td>	
	<td></td>	
	<td></td>
</tr>
</table>

<hr/>

<h1 id="数据结构">数据结构</h1>

<h2>参考</h2>

* 《算法4》代码：https://algs4.cs.princeton.edu/code/

<h2>写在前面</h2>

数据结构是计算机的基础课。其底层存储只有2种类型，顺序存储和链式存储。

因此，我这里实现的数据结构，没有用到第三方包的实现，完全利用最原始的方法来实现常用的数据结构，以及基于其上的一些算法。

虽然整个项目是用python实现的，但中间未使用”奇技淫巧“，只要方法正确，可以很快速地扩展到其他语言。

<h2>缺失之处</h2>

参数校验：这是一个非常麻烦的工作，用户可能输入的情况千奇百怪，因此参数校验只做了最基础的部分。

可扩展性：每个文件内都有各自类的测试。并没有去实现一个模板支持各种情况。例如：堆中实现的是大根堆。若构造时传入比较函数，则可扩展为小根堆。

<h2 id = "表">表</h2>

* [单链表](/DataStructure/Table/SingleLinkedList.py)

  * 从传入的列表中构造单链表
  * 头插一个元素
  * 尾插一个元素
  * 向中间指定位置插入元素
  * 删除头部元素
  * 删除尾部元素
  * 删除指定中间位置的元素
  * 查找某个元素是否存在
  * 递归反转整个链表

* [双向链表](/DataStructure/Table/DeLinkedList.py)

  * 从传入的列表中构造双向链表
  * 头插一个元素
  * 尾插一个元素
  * 向中间指定位置插入元素
  * 删除头部元素
  * 删除尾部元素
  * 删除指定中间位置的元素
  * 查找某个元素是否存在

* [哈希表](/DataStructure/Table/HashTable.py)

  * 通过一个列表构造哈希表
  * 向哈希表中插入一个值
  * 从哈希表中删除一个值
  * 哈希表中查找一个值
  * 哈希函数，通过给定的值，计算出一个位置

* [最小栈](/DataStructure/Table/MinStack.py)

  * 从传入的列表中构造最小栈
  * 插入一个元素
  * 弹出一个元素
  * 取得最小元素
  * 清空所有元素

<h2 id = "树">树</h2>

* [二叉树](/DataStructure/Tree/BinaryTree.py)

  * 从先序列表和中序列表构造二叉树
  * 二叉树的先序递归遍历
  * 二叉树的中序递归遍历
  * 二叉树的后序递归遍历
  * 二叉树的先序非递归遍历
  * 二叉树的中序非递归遍历
  * 二叉树的后序非递归遍历
  * 二叉树的层序遍历

* [字典树](/DataStructure/Tree/TrieTree.py)

  * 通过strings_list构造一颗字典树
  * 增加一个串
  * 查找字典树中是否存在对应串
  * 查找与prefix具有相同前缀的串
  * 删除字典树中的串
  * 获取字典树中的串的数量
  * 清空所有元素
  * 遍历以node为结点的整个字典树

* [红黑树](/DataStructure/Tree/RedBlackTree.py)

  * 从一个值列表构造一颗红黑树
  * 递归向红黑树中插入一个结点
  * 删除红黑树中的最小值
  * 删除红黑树中的最大值
  * 删除红黑树中具体的key
  * 取得树中的最小结点
  * 取得树中的最大结点
  * 在红黑树中查询子节点
  * 将一个红色右链接的结点  旋转  成为一个红色左链接的结点
  * 将一个红色左链接的结点  旋转  成为一个红色右链接的结点
  * 将右、左子树的红色链接转上来
  * 将左、左子树的红色链接转上来
  * 删除以node为根的红黑树的最小结点
  * 删除以node为根的红黑树的最大结点
  * 删除以node为根的红黑树下键为key的结点
  * 获取以node为根的树下最小结点
  * 获取以node为根的树下最大结点
  * 对node结点进行平衡操作
  
* [二叉平衡树](/DataStructure/Tree/AvlTree.py)
  * TODO
  
* [堆](/DataStructure/Tree/Heap.py)

  * 通过数组构造一个堆
  * 向堆中插入一个元素
  * 取出堆顶元素
  * 判断堆是否是空的
  * 清空所有元素
  * 将数组变成一个堆
  * 堆中index结点上浮
  * 堆中index结点下沉

<h2 id = "图">图</h2>

* [并查集](/DataStructure/Graph/UnionFind.py)

  * 初始化结点
  * 采用quick-find方式实现union find
  * 采用quick-union方式实现union find
  * 采用加权quick-union方式实现union find
  * 判断两个结点是否连通
  * 连通结点组成的不同的连通分量数量

* [无向图](/DataStructure/Graph/UndirectedGraph.py)

  * 通过传入边的列表来构造图
  * 向图中插入一条边
  * 从图中删除一条边
  * 取得结点的度
  * 取得对应边的权重
  * 取得边的数量
  * 判断是否是连通图
  * 用prim算法寻找最小生成树
  * 清空图


<h1 id = "经典算法">经典算法</h1>

<h2 id = "排序算法">排序算法</h2>

* [冒泡排序](/Algorighms/Sort/BubbleSort.py)
* [选择排序](/Algorighms/Sort/SelectionSort.py)
* [插入排序](/Algorighms/Sort/InsertSort.py)
* [快速排序](/Algorighms/Sort/QuickSort.py)
* [归并排序](/Algorighms/Sort/MergeSort.py)
* [（计数）/ 桶排序](/Algorighms/Sort/BucketSort.py)
* [堆排序](/Algorighms/Sort/HeapSort.py)
* [希尔排序](/Algorighms/Sort/ShellSort.py)
* [基数排序](/Algorighms/Sort/RadixSort.py)

<h2 id = "搜索算法">搜索算法</h2>

* [二分查找](/Algorighms/Search/BinarySearch.py)
* [二分查找左右边界](/Algorighms/Search/BinarySearch.py)

<h2 id = "回溯算法">回溯算法</h2>

* [子集](/Algorighms/BackTrack/SubSet.py)
* [组合](/Algorighms/BackTrack/Combination.py)
* [全排列](/Algorighms/BackTrack/Permutations.py)

<h2 id = "位运算">位运算</h2>

* [二进制中1的数量](/Algorighms/Bin/NumberOf1.py)
* [翻转二进制表示](/Algorighms/Bin/ReverseBits.py)


<h1 id = "LeetCode">LeetCode</h1>

|题目|链接|
|:--|:--|
|1.两数之和.py|[1.两数之和.py](/LeetCode/1.两数之和.py)|
|2.两数相加.py|[2.两数相加.py](/LeetCode/2.两数相加.py)|
|3.无重复字符的最长子串.py|[3.无重复字符的最长子串.py](/LeetCode/3.无重复字符的最长子串.py)|
|4.寻找两个正序数组的中位数.py|[4.寻找两个正序数组的中位数.py](/LeetCode/4.寻找两个正序数组的中位数.py)|
|5.最长回文子串.py|[5.最长回文子串.py](/LeetCode/5.最长回文子串.py)|
|19.删除链表的倒数第-n-个结点.py|[19.删除链表的倒数第-n-个结点.py](/LeetCode/19.删除链表的倒数第-n-个结点.py)|
|22.括号生成.py|[22.括号生成.py](/LeetCode/22.括号生成.py)|
|25.k-个一组翻转链表.py|[25.k-个一组翻转链表.py](/LeetCode/25.k-个一组翻转链表.py)|
|26.删除有序数组中的重复项.py|[26.删除有序数组中的重复项.py](/LeetCode/26.删除有序数组中的重复项.py)|
|27.移除元素.py|[27.移除元素.py](/LeetCode/27.移除元素.py)|
|34.在排序数组中查找元素的第一个和最后一个位置.py|[34.在排序数组中查找元素的第一个和最后一个位置.py](/LeetCode/34.在排序数组中查找元素的第一个和最后一个位置.py)|
|40.组合总和-ii.py|[40.组合总和-ii.py](/LeetCode/40.组合总和-ii.py)|
|42.接雨水.py|[42.接雨水.py](/LeetCode/42.接雨水.py)|
|45.跳跃游戏-ii.py|[45.跳跃游戏-ii.py](/LeetCode/45.跳跃游戏-ii.py)|
|46.全排列.py|[46.全排列.py](/LeetCode/46.全排列.py)|
|47.全排列-ii.py|[47.全排列-ii.py](/LeetCode/47.全排列-ii.py)|
|51.n-皇后.py|[51.n-皇后.py](/LeetCode/51.n-皇后.py)|
|52.n皇后-ii.py|[52.n皇后-ii.py](/LeetCode/52.n皇后-ii.py)|
|53.最大子序和.py|[53.最大子序和.py](/LeetCode/53.最大子序和.py)|
|55.跳跃游戏.py|[55.跳跃游戏.py](/LeetCode/55.跳跃游戏.py)|
|64.最小路径和.py|[64.最小路径和.py](/LeetCode/64.最小路径和.py)|
|67.二进制求和.py|[67.二进制求和.py](/LeetCode/67.二进制求和.py)|
|69.x-的平方根.py|[69.x-的平方根.py](/LeetCode/69.x-的平方根.py)|
|70.爬楼梯.py|[70.爬楼梯.py](/LeetCode/70.爬楼梯.py)|
|72.编辑距离.py|[72.编辑距离.py](/LeetCode/72.编辑距离.py)|
|74.搜索二维矩阵.py|[74.搜索二维矩阵.py](/LeetCode/74.搜索二维矩阵.py)|
|75.颜色分类.py|[75.颜色分类.py](/LeetCode/75.颜色分类.py)|
|76.最小覆盖子串.py|[76.最小覆盖子串.py](/LeetCode/76.最小覆盖子串.py)|
|77.组合.py|[77.组合.py](/LeetCode/77.组合.py)|
|78.子集.py|[78.子集.py](/LeetCode/78.子集.py)|
|79.单词搜索.py|[79.单词搜索.py](/LeetCode/79.单词搜索.py)|
|81.搜索旋转排序数组-ii.py|[81.搜索旋转排序数组-ii.py](/LeetCode/81.搜索旋转排序数组-ii.py)|
|88.合并两个有序数组.py|[88.合并两个有序数组.py](/LeetCode/88.合并两个有序数组.py)|
|91.解码方法.py|[91.解码方法.py](/LeetCode/91.解码方法.py)|
|92.反转链表-ii.py|[92.反转链表-ii.py](/LeetCode/92.反转链表-ii.py)|
|95.不同的二叉搜索树-ii.py|[95.不同的二叉搜索树-ii.py](/LeetCode/95.不同的二叉搜索树-ii.py)|
|96.不同的二叉搜索树.py|[96.不同的二叉搜索树.py](/LeetCode/96.不同的二叉搜索树.py)|
|98.验证二叉搜索树.py|[98.验证二叉搜索树.py](/LeetCode/98.验证二叉搜索树.py)|
|101.对称二叉树.py|[101.对称二叉树.py](/LeetCode/101.对称二叉树.py)|
|102.二叉树的层序遍历.py|[102.二叉树的层序遍历.py](/LeetCode/102.二叉树的层序遍历.py)|
|103.二叉树的锯齿形层序遍历.py|[103.二叉树的锯齿形层序遍历.py](/LeetCode/103.二叉树的锯齿形层序遍历.py)|
|104.二叉树的最大深度.py|[104.二叉树的最大深度.py](/LeetCode/104.二叉树的最大深度.py)|
|105.从前序与中序遍历序列构造二叉树.py|[105.从前序与中序遍历序列构造二叉树.py](/LeetCode/105.从前序与中序遍历序列构造二叉树.py)|
|106.从中序与后序遍历序列构造二叉树.py|[106.从中序与后序遍历序列构造二叉树.py](/LeetCode/106.从中序与后序遍历序列构造二叉树.py)|
|107.二叉树的层序遍历-ii.py|[107.二叉树的层序遍历-ii.py](/LeetCode/107.二叉树的层序遍历-ii.py)|
|108.将有序数组转换为二叉搜索树.py|[108.将有序数组转换为二叉搜索树.py](/LeetCode/108.将有序数组转换为二叉搜索树.py)|
|110.平衡二叉树.py|[110.平衡二叉树.py](/LeetCode/110.平衡二叉树.py)|
|111.二叉树的最小深度.py|[111.二叉树的最小深度.py](/LeetCode/111.二叉树的最小深度.py)|
|114.二叉树展开为链表.py|[114.二叉树展开为链表.py](/LeetCode/114.二叉树展开为链表.py)|
|116.填充每个节点的下一个右侧节点指针.py|[116.填充每个节点的下一个右侧节点指针.py](/LeetCode/116.填充每个节点的下一个右侧节点指针.py)|
|121.买卖股票的最佳时机.py|[121.买卖股票的最佳时机.py](/LeetCode/121.买卖股票的最佳时机.py)|
|122.买卖股票的最佳时机-ii.py|[122.买卖股票的最佳时机-ii.py](/LeetCode/122.买卖股票的最佳时机-ii.py)|
|123.买卖股票的最佳时机-iii.py|[123.买卖股票的最佳时机-iii.py](/LeetCode/123.买卖股票的最佳时机-iii.py)|
|130.被围绕的区域.py|[130.被围绕的区域.py](/LeetCode/130.被围绕的区域.py)|
|135.分发糖果.py|[135.分发糖果.py](/LeetCode/135.分发糖果.py)|
|136.只出现一次的数字.py|[136.只出现一次的数字.py](/LeetCode/136.只出现一次的数字.py)|
|139.单词拆分.py|[139.单词拆分.py](/LeetCode/139.单词拆分.py)|
|141.环形链表.py|[141.环形链表.py](/LeetCode/141.环形链表.py)|
|142.环形链表-ii.py|[142.环形链表-ii.py](/LeetCode/142.环形链表-ii.py)|
|154.寻找旋转排序数组中的最小值-ii.py|[154.寻找旋转排序数组中的最小值-ii.py](/LeetCode/154.寻找旋转排序数组中的最小值-ii.py)|
|167.两数之和-ii-输入有序数组.py|[167.两数之和-ii-输入有序数组.py](/LeetCode/167.两数之和-ii-输入有序数组.py)|
|172.阶乘后的零.py|[172.阶乘后的零.py](/LeetCode/172.阶乘后的零.py)|
|188.买卖股票的最佳时机-iv.py|[188.买卖股票的最佳时机-iv.py](/LeetCode/188.买卖股票的最佳时机-iv.py)|
|190.颠倒二进制位.py|[190.颠倒二进制位.py](/LeetCode/190.颠倒二进制位.py)|
|191.位-1-的个数.py|[191.位-1-的个数.py](/LeetCode/191.位-1-的个数.py)|
|198.打家劫舍.py|[198.打家劫舍.py](/LeetCode/198.打家劫舍.py)|
|204.计数质数.py|[204.计数质数.py](/LeetCode/204.计数质数.py)|
|213.打家劫舍-ii.py|[213.打家劫舍-ii.py](/LeetCode/213.打家劫舍-ii.py)|
|215.数组中的第k个最大元素.py|[215.数组中的第k个最大元素.py](/LeetCode/215.数组中的第k个最大元素.py)|
|221.最大正方形.py|[221.最大正方形.py](/LeetCode/221.最大正方形.py)|
|226.翻转二叉树.py|[226.翻转二叉树.py](/LeetCode/226.翻转二叉树.py)|
|230.二叉搜索树中第k小的元素.py|[230.二叉搜索树中第k小的元素.py](/LeetCode/230.二叉搜索树中第k小的元素.py)|
|231.2-的幂.py|[231.2-的幂.py](/LeetCode/231.2-的幂.py)|
|234.回文链表.py|[234.回文链表.py](/LeetCode/234.回文链表.py)|
|236.二叉树的最近公共祖先.py|[236.二叉树的最近公共祖先.py](/LeetCode/236.二叉树的最近公共祖先.py)|
|257.二叉树的所有路径.py|[257.二叉树的所有路径.py](/LeetCode/257.二叉树的所有路径.py)|
|279.完全平方数.py|[279.完全平方数.py](/LeetCode/279.完全平方数.py)|
|283.移动零.py|[283.移动零.py](/LeetCode/283.移动零.py)|
|297.二叉树的序列化与反序列化.py|[297.二叉树的序列化与反序列化.py](/LeetCode/297.二叉树的序列化与反序列化.py)|
|300.最长递增子序列.py|[300.最长递增子序列.py](/LeetCode/300.最长递增子序列.py)|
|309.最佳买卖股票时机含冷冻期.py|[309.最佳买卖股票时机含冷冻期.py](/LeetCode/309.最佳买卖股票时机含冷冻期.py)|
|310.最小高度树.py|[310.最小高度树.py](/LeetCode/310.最小高度树.py)|
|316.去除重复字母.py|[316.去除重复字母.py](/LeetCode/316.去除重复字母.py)|
|322.零钱兑换.py|[322.零钱兑换.py](/LeetCode/322.零钱兑换.py)|
|326.3-的幂.py|[326.3-的幂.py](/LeetCode/326.3-的幂.py)|
|341.扁平化嵌套列表迭代器.py|[341.扁平化嵌套列表迭代器.py](/LeetCode/341.扁平化嵌套列表迭代器.py)|
|343.整数拆分.py|[343.整数拆分.py](/LeetCode/343.整数拆分.py)|
|344.反转字符串.py|[344.反转字符串.py](/LeetCode/344.反转字符串.py)|
|347.前-k-个高频元素.py|[347.前-k-个高频元素.py](/LeetCode/347.前-k-个高频元素.py)|
|376.摆动序列.py|[376.摆动序列.py](/LeetCode/376.摆动序列.py)|
|406.根据身高重建队列.py|[406.根据身高重建队列.py](/LeetCode/406.根据身高重建队列.py)|
|413.等差数列划分.py|[413.等差数列划分.py](/LeetCode/413.等差数列划分.py)|
|416.分割等和子集.py|[416.分割等和子集.py](/LeetCode/416.分割等和子集.py)|
|417.太平洋大西洋水流问题.py|[417.太平洋大西洋水流问题.py](/LeetCode/417.太平洋大西洋水流问题.py)|
|435.无重叠区间.py|[435.无重叠区间.py](/LeetCode/435.无重叠区间.py)|
|437.路径总和-iii.py|[437.路径总和-iii.py](/LeetCode/437.路径总和-iii.py)|
|450.删除二叉搜索树中的节点.py|[450.删除二叉搜索树中的节点.py](/LeetCode/450.删除二叉搜索树中的节点.py)|
|451.根据字符出现频率排序.py|[451.根据字符出现频率排序.py](/LeetCode/451.根据字符出现频率排序.py)|
|452.用最少数量的箭引爆气球.py|[452.用最少数量的箭引爆气球.py](/LeetCode/452.用最少数量的箭引爆气球.py)|
|455.分发饼干.py|[455.分发饼干.py](/LeetCode/455.分发饼干.py)|
|474.一和零.py|[474.一和零.py](/LeetCode/474.一和零.py)|
|494.目标和.py|[494.目标和.py](/LeetCode/494.目标和.py)|
|496.下一个更大元素-i.py|[496.下一个更大元素-i.py](/LeetCode/496.下一个更大元素-i.py)|
|504.七进制数.py|[504.七进制数.py](/LeetCode/504.七进制数.py)|
|516.最长回文子序列.py|[516.最长回文子序列.py](/LeetCode/516.最长回文子序列.py)|
|518.零钱兑换-ii.py|[518.零钱兑换-ii.py](/LeetCode/518.零钱兑换-ii.py)|
|524.通过删除字母匹配到字典里最长单词.py|[524.通过删除字母匹配到字典里最长单词.py](/LeetCode/524.通过删除字母匹配到字典里最长单词.py)|
|538.把二叉搜索树转换为累加树.py|[538.把二叉搜索树转换为累加树.py](/LeetCode/538.把二叉搜索树转换为累加树.py)|
|540.有序数组中的单一元素.py|[540.有序数组中的单一元素.py](/LeetCode/540.有序数组中的单一元素.py)|
|542.01-矩阵.py|[542.01-矩阵.py](/LeetCode/542.01-矩阵.py)|
|543.二叉树的直径.py|[543.二叉树的直径.py](/LeetCode/543.二叉树的直径.py)|
|547.省份数量.py|[547.省份数量.py](/LeetCode/547.省份数量.py)|
|567.字符串的排列.py|[567.字符串的排列.py](/LeetCode/567.字符串的排列.py)|
|583.两个字符串的删除操作.py|[583.两个字符串的删除操作.py](/LeetCode/583.两个字符串的删除操作.py)|
|605.种花问题.py|[605.种花问题.py](/LeetCode/605.种花问题.py)|
|633.平方数之和.py|[633.平方数之和.py](/LeetCode/633.平方数之和.py)|
|637.二叉树的层平均值.py|[637.二叉树的层平均值.py](/LeetCode/637.二叉树的层平均值.py)|
|650.只有两个键的键盘.py|[650.只有两个键的键盘.py](/LeetCode/650.只有两个键的键盘.py)|
|652.寻找重复的子树.py|[652.寻找重复的子树.py](/LeetCode/652.寻找重复的子树.py)|
|654.最大二叉树.py|[654.最大二叉树.py](/LeetCode/654.最大二叉树.py)|
|665.非递减数列.py|[665.非递减数列.py](/LeetCode/665.非递减数列.py)|
|680.验证回文字符串-ⅱ.py|[680.验证回文字符串-ⅱ.py](/LeetCode/680.验证回文字符串-ⅱ.py)|
|695.岛屿的最大面积.py|[695.岛屿的最大面积.py](/LeetCode/695.岛屿的最大面积.py)|
|700.二叉搜索树中的搜索.py|[700.二叉搜索树中的搜索.py](/LeetCode/700.二叉搜索树中的搜索.py)|
|701.二叉搜索树中的插入操作.py|[701.二叉搜索树中的插入操作.py](/LeetCode/701.二叉搜索树中的插入操作.py)|
|714.买卖股票的最佳时机含手续费.py|[714.买卖股票的最佳时机含手续费.py](/LeetCode/714.买卖股票的最佳时机含手续费.py)|
|752.打开转盘锁.py|[752.打开转盘锁.py](/LeetCode/752.打开转盘锁.py)|
|763.划分字母区间.py|[763.划分字母区间.py](/LeetCode/763.划分字母区间.py)|
|875.爱吃香蕉的珂珂.py|[875.爱吃香蕉的珂珂.py](/LeetCode/875.爱吃香蕉的珂珂.py)|
|876.链表的中间结点.py|[876.链表的中间结点.py](/LeetCode/876.链表的中间结点.py)|
|934.最短的桥.py|[934.最短的桥.py](/LeetCode/934.最短的桥.py)|
|1011.在-d-天内送达包裹的能力.py|[1011.在-d-天内送达包裹的能力.py](/LeetCode/1011.在-d-天内送达包裹的能力.py)|
|1081.不同字符的最小子序列.py|[1081.不同字符的最小子序列.py](/LeetCode/1081.不同字符的最小子序列.py)|
|1110.删点成林.py|[1110.删点成林.py](/LeetCode/1110.删点成林.py)|
|1143.最长公共子序列.py|[1143.最长公共子序列.py](/LeetCode/1143.最长公共子序列.py)|
|1670.设计前中后队列.py|[1670.设计前中后队列.py](/LeetCode/1670.设计前中后队列.py)|

<h1 id = "数据结构思维导图">数据结构思维导图</h1>

![Image text](images/DataStructure.jpeg)

<h1 id = "各排序算法时间复杂度">各排序算法时间复杂度</h1>

![Image text](images/SortAlgorithms.png)