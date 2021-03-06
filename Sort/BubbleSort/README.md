# 冒泡排序
- 前言
	- 如果说各种各样的编程语言是五花八门的招式，那么数据结构和算法就是程序员的内功了，这也是为什么各种招聘面试永远不会冷落这些的原因。
	- 而排序作为数据结构一个重要组成是非常重要的。
- 排序
	- 将一组无序的数据整理成为有序的序列的过程就是排序。
- 排序分类
	- 一般而言，排序分为内部排序和外部排序。
		- 若整个排序过程不需要访问外存便能够完成，这类排序称为内部排序。
		- 若数据量很大，排序不可能在内存中完成，这类排序称为外部排序。
	- 导图如下
	- ![](http://g.recordit.co/trYo9qaS2b.gif)

- 冒泡排序
	- 冒泡排序是一种交换排序，交换排序的基本思想是：两两比较待排序的关键字，并交换不满足次序要求的那对数，直到整个序列都满足次序要求为止。
	- 什么是冒泡排序
		- 以升序为例，对n个数据，共进行n轮排序，每一轮两两比较相邻元素，将小的放到前面大的放到后面，每一轮结果是将当前最大的元素移动到序列最后。
		- 由于每一轮排序当前最大的元素到达序列的最底部，越小的元素慢慢浮动到序列的顶部，故名冒泡排序。
- 代码实现
	- 这个排序实现并不是很难，我用python实现如代码中的bubbleSort函数。
	- 但是这里列举一下，冒泡排序的算法复杂度。
	
		| 排序名称 | 最好情况 | 最坏情况 | 平均情况 |
		| :---: | :---: | :---: | :---: |
		| 冒泡排序 | O(n) | O(n^2) | O(n^2) |
	- 也就是说，这个算法是可以优化的，一旦序列基本有序，只需要进行少数轮次排序就可以实现，后面的轮次是多余的，这也是很多面试官喜欢问到的。
	- 优化后的代码如函数bubbleSortOptimized函数所示，只有添加一个flag监控该趟是否交换，一旦某一趟排序没有交换，就认为排序可以结束了。
	- 任何时候，在空间复杂度没有太大优化空间时，优化时间复杂度是一个永恒不变的话题。