# LittleElephantAndIntervalsDiv1

作者：梁浩

关键词：计数

## 题目简述

给M个球，起始时都为白色。有N次操作，每次会将一个区间内的球都染成白色或都染成黑色。问最终会有多少种可能的结果。
保证$$M\leq 1000, N\leq 50$$.

## 算法

对于每个位置，扫描一遍操作序列，找到最后一次修改这个位置的操作，并且给这个操作打上标记。最后统计有多少个操作被打上了标记，我们把这个数设为x，那么最终答案就是$$2^x$$。因为只要这些操作染的颜色不同，那么对应位置的颜色也一定不同；如果这些操作的颜色相同，那么最终的颜色也一定都相同。总时间复杂为$$O(N*M)$$
