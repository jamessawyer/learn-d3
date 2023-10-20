本章主要绘制直方图，主要涉及的知识点：

1. 如何绘制直方图，散点图所需要的元素：
   1. `rect` 表示bar
   2. X轴 + Y轴
   3. `text` 元素添加x轴和y轴Label
   4. 使用 [d3.bin](https://d3js.org/d3-array/bin#bin) 对数据进行分类操作，将数据集装在不同的桶中进行统计
2. **绘制所有图形的基本步骤**
   1. 读取数据（`access data`） 数据源，x轴和y轴表示的数据（`Accessors`）
   2. 确定图形尺寸（`Create chart dimensions`）
      1. 图形的整体width,height,以及margins
      2. 真正绘制区域bounds
   3. 绘制画布（`Draw canvas`）
      1. 构建容器，一般就是 `svg` 根元素
      2. 构建绘制区域 一般使用 `g` 元素
   4. 创建比例尺 （`Create scales`）
      1. xScale
      2. yScale
      3. 数据映射的比例尺 `colorScale`
      4. 使用比例尺提供的 `.nice()` 函数对输出值进行美化
   5. 绘制数据 （`Draw data`）
      1. 提到 `enter()` 方法的含义
      2. `enter().append('xxx').merge()` 方法的含义，对数据进行合并
      3. `join()` 方法的作用，它是上面几个方法的一种简便写法，一般都会使用这个方法
   6. 绘制坐标系 (`Draw peripherals`)
      1. 还谈到了如何使用 `text` 给x轴和y轴绘制Labels，需要注意的是，它们都是相对于坐标轴的位置
   7. 设置交互（`Set up interactions`）
      1. 暂时没讲这个，第5章讲解



2023-10-18 17:06