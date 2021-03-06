# Week 08 学习总结

## 字符串算法
### 朴素的字符串匹配算法
没有预处理阶段；
1. 滑动窗口总是后移 1 位；
2. 对模式中的字符的比较顺序不限定，可以从前到后，也可以从后到前；
3. 匹配阶段需要 O((n - m + 1)m) 的时间复杂度；
4. 需要 2n 次的字符比较；

### Knuth-Morris-Pratt 字符串匹配算法（即 KMP 算法）
KMP 算法的主要特点是：
1. 需要对模式字符串做预处理；
2. 预处理阶段需要额外的 O(m) 空间和复杂度；
3. 匹阶段与字符集的大小无关；
4. 匹配阶段至多执行 2n - 1 次字符比较；
5. 对模式中字符的比较顺序时从左到右；