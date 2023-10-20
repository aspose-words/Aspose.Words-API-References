---
title: AxisScaling Class
linktitle: AxisScaling
articleTitle: AxisScaling
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.Charts.AxisScaling 班级. 表示轴的缩放选项 在 C#.
type: docs
weight: 570
url: /zh/net/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class

表示轴的缩放选项。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class AxisScaling
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [AxisScaling](axisscaling/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [LogBase](../../aspose.words.drawing.charts/axisscaling/logbase/) { get; set; } | 获取或设置对数轴的对数底。 |
| [Maximum](../../aspose.words.drawing.charts/axisscaling/maximum/) { get; set; } | 获取或设置轴的最大值。 |
| [Minimum](../../aspose.words.drawing.charts/axisscaling/minimum/) { get; set; } | 获取或设置轴的最小值。 |
| [Type](../../aspose.words.drawing.charts/axisscaling/type/) { get; set; } | 获取或设置轴的缩放类型。 |

## 例子

展示如何将对数缩放应用于图表轴。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 插入五个点的 X/Y 坐标系列。
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// X轴的缩放默认是线性的，
// 显示覆盖 X 值范围（0、1、2、3...）的均匀递增值。
// 线性轴对于我们的 Y 值来说并不理想
// 因为 Y 值较小的点将更难读取。
// 以 20 为底的对数缩放 (1, 20, 400, 8000...)
// 将分散绘制的点，使我们能够更轻松地在图表上读取它们的值。
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
