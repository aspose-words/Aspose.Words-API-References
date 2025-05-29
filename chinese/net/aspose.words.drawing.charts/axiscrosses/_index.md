---
title: AxisCrosses Enum
linktitle: AxisCrosses
articleTitle: AxisCrosses
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.AxisCrosses 枚举以定义轴交叉点，轻松增强您的图表功能。
type: docs
weight: 780
url: /zh/net/aspose.words.drawing.charts/axiscrosses/
---
## AxisCrosses enumeration

指定轴的可能交叉点。

```csharp
public enum AxisCrosses
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Automatic | `0` | 分类轴与数值轴的零点相交（如果可能），或者如果最小值大于零，则与最小值相交 ，如果最大值小于零，则与最大值相交 |
| Maximum | `1` | 垂直轴与轴的最大值相交。 |
| Minimum | `2` | 垂直轴与轴的最小值相交。 |
| Custom | `3` | 垂直轴与轴的指定值相交。 |

## 例子

展示如何插入图表并修改其轴的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 插入一个图表系列，其中 X 轴为类别，Y 轴为相应的数值。
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// 图表轴有各种可以改变其外观的选项，
// 例如它们的方向、主/次单位刻度和刻度标记。
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// 柱状图没有 Z 轴。
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
