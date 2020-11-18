# 135. 分发糖果
## 题目

老师想给孩子们分发糖果，有 N 个孩子站成了一条直线，老师会根据每个孩子的表现，预先给他们评分。

你需要按照以下要求，帮助老师给这些孩子分发糖果：

每个孩子至少分配到 1 个糖果。
相邻的孩子中，评分高的孩子必须获得更多的糖果。
那么这样下来，老师至少需要准备多少颗糖果呢？

示例 1:
<pre>
输入: [1,0,2]
输出: 5
解释: 你可以分别给这三个孩子分发 2、1、2 颗糖果。
</pre>
示例 2:
<pre>
输入: [1,2,2]
输出: 4
解释: 你可以分别给这三个孩子分发 1、2、1 颗糖果。
     第三个孩子只得到 1 颗糖果，这已满足上述两个条件。
</pre>

## 思路
- 新建一个糖果数组，默认给每个学生 1 个糖果
- 从左向右遍历，当右边孩子评分高于左边孩子时，右边孩子糖果数=左边孩子糖果数+1
- 从右向左遍历，当右边孩子评分低于左边孩子 && 右边孩子糖果数大于等于左边孩子糖果数时，左边孩子糖果数=右边孩子糖果数+1
- 对糖果数组进行求和