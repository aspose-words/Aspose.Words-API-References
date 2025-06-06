---
title: AxisTickMark Enum
linktitle: AxisTickMark
articleTitle: AxisTickMark
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.AxisTickMark 枚举，用于自定义刻度线位置，增强图表的清晰度和视觉吸引力。
type: docs
weight: 850
url: /zh/net/aspose.words.drawing.charts/axistickmark/
---
## AxisTickMark enumeration

指定刻度线的可能位置。

```csharp
public enum AxisTickMark
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Cross | `0` | 指定刻度线应与轴相交。 |
| Inside | `1` | 指定刻度线应位于绘图区域内。 |
| Outside | `2` | 指定刻度线应位于绘图区域之外。 |
| None | `3` | 指定不应有刻度线。 |

## 例子

显示如何插入带有日期/时间值的图表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 添加一个自定义系列，其中包含 X 轴的日期/时间值以及 Y 轴的相应十进制值。
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// 设置 X 轴的下限和上限。
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// 将 X 轴的主单位设置为周，次单位设置为天。
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// 定义十进制值的 Y 轴属性。
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
