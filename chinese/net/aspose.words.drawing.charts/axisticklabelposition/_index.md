---
title: AxisTickLabelPosition Enum
linktitle: AxisTickLabelPosition
articleTitle: AxisTickLabelPosition
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.AxisTickLabelPosition 枚举，它定义了最佳刻度标签位置，以增强图表清晰度和呈现效果。
type: docs
weight: 830
url: /zh/net/aspose.words.drawing.charts/axisticklabelposition/
---
## AxisTickLabelPosition enumeration

指定刻度标签的可能位置。

```csharp
public enum AxisTickLabelPosition
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| High | `0` | 指定轴标签应位于垂直轴的高端。 |
| Low | `1` | 指定轴标签应位于垂直轴的低端。 |
| NextToAxis | `2` | 指定轴标签应位于轴旁边。 |
| None | `3` | 指定不绘制轴标签。 |
| Default | `2` | 指定刻度标签位置的默认值。 |

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
