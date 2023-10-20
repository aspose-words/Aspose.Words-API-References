---
title: AxisScaling.LogBase
linktitle: LogBase
articleTitle: LogBase
second_title: 用于 .NET 的 Aspose.Words
description: AxisScaling LogBase 财产. 获取或设置对数轴的对数底数 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/axisscaling/logbase/
---
## AxisScaling.LogBase property

获取或设置对数轴的对数底数。

```csharp
public double LogBase { get; set; }
```

## 评论

MS Office 2016 新图表不支持该属性。

浮点值的有效范围大于或等于 2 且小于或 等于 1000。该属性仅在以下情况下有效[`Type`](../type/)设置为 Logarithmic.

设置此属性会设置[`Type`](../type/)财产Logarithmic.

## 例子

显示如何将对数缩放应用于图表轴。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 为五个点插入一个带有 X/Y 坐标的系列。
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// X轴的缩放默认是线性的，
// 显示覆盖 X 值范围 (0, 1, 2, 3...) 的均匀递增值。
// 线性轴不适合我们的 Y 值
// 因为 Y 值较小的点将更难阅读。
// 以 20 为底的对数缩放 (1, 20, 400, 8000...)
// 将散布绘制的点，使我们能够更轻松地在图表上读取它们的值。
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### 也可以看看

* class [AxisScaling](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
