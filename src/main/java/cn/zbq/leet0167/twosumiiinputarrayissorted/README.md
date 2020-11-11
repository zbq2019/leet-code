# 167. 两数之和 II - 输入有序数组

## 题目
给定一个已按照升序排列 的有序数组，找到两个数使得它们相加之和等于目标数。

函数应该返回这两个下标值 index1 和 index2，其中 index1 必须小于 index2。

**说明:**

- 返回的下标值（index1 和 index2）不是从零开始的。
- 你可以假设每个输入只对应唯一的答案，而且你不可以重复使用相同的元素。

示例:

<pre>
输入: numbers = [2, 7, 11, 15], target = 9
输出: [1,2]
解释: 2 与 7 之和等于目标数 9 。因此 index1 = 1, index2 = 2 。
</pre>

## 思路
- 数组是有序数组，可以采用方向相反的两个指针来寻找这两个数字，一个初始指向最左侧，一个初始指向最右侧
- 对数组进行遍历
    - 两数之和大于目标值，左侧指针向右侧移动
    - 两数之和小于目标值，右侧指针向左移动
    - 两数之和等于目标值，即我们需要的结果

