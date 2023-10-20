本章主要绘制折线图，主要涉及的知识点：

1. 如何绘制折线图，折线图所需要的元素
   1. 线条
   2. X轴 + Y轴
2. 如何确定绘制边界
3. 比例尺的使用 - 输入(`domain`) & 输出(`range`)
   1. `scaleLinear()`
   2. `scaleTime()`
4. 如何绘制折线 - `d3.line().x(d => xScale(xAccessor(d))).y(d => yScale(yAccessor(d)))`
5. 如何绘制X,Y轴
   1. **需要注意的是d3的axis生成器知道如何相对于axis线放置tick marks & tick labels，但是它不知道轴本身应该放到那里**
6. 如何使用d3提供的 `call()` 方法调用函数
   1. 它的好处是，不会中断selection，这样便可以继续进行链式调用
7. d3的一些工具函数
   1. `d3.extend(array, xAccessor)` 获取数据的最小值和最大值区间范围
   2. `d3.timeParse('%Y-%m-%d')` 对时间进行格式化