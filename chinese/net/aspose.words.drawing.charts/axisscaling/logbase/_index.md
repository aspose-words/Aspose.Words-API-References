---
title: AxisScaling.LogBase
linktitle: LogBase
articleTitle: LogBase
second_title: Aspose.Words for .NET
description: 调整 AxisScaling LogBase 属性的对数底数，实现更精确的数据可视化并提升图表准确性。立即优化您的图表！
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

浮点值的有效范围是大于或等于 2 且小于或等于 1000。该属性仅在以下情况下有效[`Type`](../type/)设置为 Logarithmic。

设置此属性将设置[`Type`](../type/)财产Logarithmic.

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

// X 轴的缩放默认是线性的，
// 显示覆盖我们的 X 值范围（0、1、2、3……）的均匀递增值。
// 线性轴对于我们的 Y 值来说并不理想
// 因为 Y 值较小的点将更难读取。
// 以 20 为底的对数缩放（1、20、400、8000……）
// 将分散绘制的点，使我们能够更轻松地在图表上读取它们的值。
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### 也可以看看

* class [AxisScaling](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
