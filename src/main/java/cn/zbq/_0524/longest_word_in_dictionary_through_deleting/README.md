# 524. 通过删除字母匹配到字典里最长单词

## 题目
给定一个字符串和一个字符串字典，找到字典里面最长的字符串，该字符串可以通过删除给定字符串的某些字符来得到。如果答案不止一个，返回长度最长且字典顺序最小的字符串。如果答案不存在，则返回空字符串。

- 所有输入的字符串长度不会超过 1000。

示例 1:

```
输入:
s = "abpcplea", d = ["ale","apple","monkey","plea"]
输出:
"apple"
```

示例 2:

```
输入:
s = "abpcplea", d = ["a","b","c"]
输出:
"a"
```

说明:

- 所有输入的字符串只包含小写字母。
- 字典的大小不会超过 1000。

## 思路
该字符串可以通过删除给定字符串的某些字符来得到

这是题目中的原话,言外之意,**只能**从给定的字符串中**删除**,而**不能移动**前后的顺序


- 如果为否,进一步判断是否相等,如果相等则判断字符顺序,小于则更新符合条件的字符串为当前串
- 首先我们需要一个方法来判断字符串a是否为字符串b的子串
- 对给定的字典进行遍历,判断字典中的字符串是否为给定字符串的子串
- 如果是子串,进一步判断是否大于上一个符合条件的字符串,如果是将符合条件的串更新为当前字符串