# 归并排序
- 概述
	- 以归并操作为基础的排序算法，底层算法设计为分治法。
	- 所谓分治法，就是讲问题分解为多个子问题递归求解，再将子问题答案合并。
- 算法实现
	- 将待排序序列分解为两个，四个，，，n个子部分。
	- 两两合并，并内部排序。
- 算法分析
	- 这个算法描述比较简单，然而实现起来略有难度，递归迭代法均可解。
	- 复杂度

				| 排序名称 | 最好情况 | 最坏情况 | 平均情况 |
				| :---: | :---: | :---: | :---: |
				| 归并排序 | O(nlog2n) | O(nlog2n) | O(nlog2n) |
	- 稳定性
		- 算法稳定。
	- 优先选择
		- 从空间复杂度来考虑：首选堆排序，其次是快速排序，最后是归并排序。
		- 从稳定性来考虑，应选取归并排序，因为堆排序和快速排序都是不稳定的。
		- 从平均情况下的排序速度考虑，应该选择快速排序。