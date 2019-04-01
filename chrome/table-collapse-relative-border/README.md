## 问题现象
Table 边框无法正常绘制
或Table内部布局边框重叠

## 问题成因

### Table内部布局重叠（problem1）

1. table元素的 CSS 写了 border-collapse: separate;border-spacing: 0; 模拟
   collapse效果
2. 使用了colspan属性
3. td的position是relative


### 边框无法正常绘制（problem2）

1. table元素的 CSS 写了 border-collapse: collapse， 这个属性表示表格的单元格
     (<td> 和<th>)的 border 会 collapse （重叠），即拥有和 margin collapse 一样
     的现象: 两条相邻的 border 会合并成一条。
2. 使用了colspan属性
3. td的position是relative

